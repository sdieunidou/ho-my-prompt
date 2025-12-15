# PHP/Symfony Prompts Repository

A centralized repository containing consolidated code review prompts for PHP/Symfony projects. This repository serves as the data source for the PHP/Symfony Prompts UI application.

## 📋 Overview

This repository contains:
- **`manifest.json`**: The main manifest file that catalogs all available prompts
- **`prompts/`**: Consolidated "Master Prompts" covering major review areas

The UI application fetches data from this repository to provide an interactive interface for browsing and using code review prompts.

## 📁 Repository Structure

```
ho-my-prompt/
├── manifest.json            # Main manifest file (v2.0)
├── prompts/                
│   ├── architecture-general.md  # SOLID, Design Patterns
│   ├── architecture-ddd.md      # Hexagonal/DDD specific
│   ├── symfony-ecosystem.md     # Symfony Standards
│   ├── performance-doctrine.md  # SQL & Performance
│   ├── security-audit.md        # OWASP & Security
│   ├── modern-php.md            # PHP 8.2+ Upgrade
│   ├── clean-code.md            # Readability
│   └── testing-strategy.md      # QA & Tests
├── LICENSE
└── README.md
```

## 📝 Manifest Structure

The `manifest.json` file follows this structure:

```json
{
  "version": "2.0.0",
  "lastUpdated": "2024-12-15",
  "categories": [
    {
      "id": "architecture",
      "name": "Architecture",
      "icon": "layers",
      "description": "Design Patterns, SOLID et Structure"
    }
  ],
  "prompts": [
    {
      "id": "architecture-general",
      "title": "Audit Architecture & SOLID",
      "description": "Analyse structurelle globale...",
      "category": "architecture",
      "tags": ["SOLID", "Architecture"],
      "contentUrl": "https://raw.githubusercontent.com/sdieunidou/ho-my-prompt/main/prompts/architecture-general.md",
      "difficulty": "advanced"
    }
  ]
}
```

### Manifest Fields

#### Categories
| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique category identifier |
| `name` | string | Display name of the category |
| `icon` | string | Icon name (layers, code, zap, shield, file, bug) |
| `description` | string | Category description |

#### Prompts
| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique prompt identifier |
| `title` | string | Prompt title |
| `description` | string | Short description |
| `category` | string | Parent category ID |
| `tags` | string[] | Tags for filtering |
| `contentUrl` | string | URL to the Markdown file containing the full prompt |
| `difficulty` | string | Difficulty level (beginner, intermediate, advanced) |

## ✍️ Prompt File Format

Each prompt is stored as a "Master Prompt" designed to cover a full topic in one go.

```markdown
# Prompt Title

Act as an expert...

## Objective
High level goal...

## Axes of Analysis
1. **Topic 1**
   - Details...
2. **Topic 2**
   - Details...

## Expected Format
- **Summary**
- **Critical Issues**

## Code to Analyze
[Insert code here]
```

## 🚀 Adding a New Prompt

1. **Create the prompt file**: Add a new `.md` file in the `prompts/` directory
2. **Update manifest.json**: Add an entry to the `prompts` array
3. **Update version**: Increment the `version` field
4. **Commit and push**

## 🔗 Integration with UI

To point the UI to this repository, configure the `MANIFEST_URL` in the UI application:
```typescript
const MANIFEST_URL = "https://raw.githubusercontent.com/sdieunidou/ho-my-prompt/main/manifest.json";
```

## 📄 License

MIT
