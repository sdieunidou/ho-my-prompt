# PHP/Symfony Prompts Repository

A centralized repository containing code review prompts for PHP/Symfony projects. This repository serves as the data source for the PHP/Symfony Prompts UI application.

## 📋 Overview

This repository contains:
- **`manifest.json`**: The main manifest file that catalogs all available prompts and categories
- **`prompts/`**: Individual Markdown files containing the full prompt content

The UI application fetches data from this repository to provide an interactive interface for browsing and using code review prompts.

## 📁 Repository Structure

```
ho-my-prompt/
├── manifest.json        # Main manifest file
├── prompts/            # Prompt Markdown files
│   ├── sql-injection.md
│   ├── xss-check.md
│   └── ...
├── LICENSE
└── README.md
```

## 📝 Manifest Structure

The `manifest.json` file follows this structure:

```json
{
  "version": "1.0.0",
  "lastUpdated": "2024-01-15",
  "categories": [
    {
      "id": "security",
      "name": "Security",
      "icon": "shield",
      "description": "Security verification prompts"
    }
  ],
  "prompts": [
    {
      "id": "sql-injection",
      "title": "SQL Injection Check",
      "description": "Analyze code to detect SQL injection vulnerabilities...",
      "category": "security",
      "tags": ["SQL", "Doctrine", "Injection"],
      "contentUrl": "https://raw.githubusercontent.com/your-username/ho-my-prompt/main/prompts/sql-injection.md",
      "difficulty": "intermediate"
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
| `icon` | string | Icon name (code, shield, zap, file, database, settings, layers, bug) |
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

Each prompt is stored as a Markdown file (`.md`) in the `prompts/` directory. The file should contain the complete prompt text that users will copy:

```markdown
# Prompt Title

Analyze the following code for [objective description]...

## Instructions
1. First instruction
2. Second instruction

## Code Example to Analyze
[PHP/Symfony code to analyze]

## Points to Check
- Point 1
- Point 2
- Point 3
```

## 🚀 Adding a New Prompt

1. **Create the prompt file**: Add a new `.md` file in the `prompts/` directory
   ```bash
   prompts/my-new-prompt.md
   ```

2. **Update manifest.json**: Add an entry to the `prompts` array:
   ```json
   {
     "id": "my-new-prompt",
     "title": "My New Prompt",
     "description": "Brief description of what this prompt does",
     "category": "security",
     "tags": ["tag1", "tag2"],
     "contentUrl": "https://raw.githubusercontent.com/your-username/ho-my-prompt/main/prompts/my-new-prompt.md",
     "difficulty": "intermediate"
   }
   ```

3. **Update version**: Increment the `version` field and update `lastUpdated` date in `manifest.json`

4. **Commit and push**: Commit your changes and push to the repository

## 🏷️ Available Category Icons

The following icons are available for categories:
- `code` - Code-related prompts
- `shield` - Security prompts
- `zap` - Performance prompts
- `file` - File handling prompts
- `database` - Database-related prompts
- `settings` - Configuration prompts
- `layers` - Architecture prompts
- `bug` - Bug detection prompts

## 🔗 Integration with UI

The UI application fetches the `manifest.json` file from this repository and uses it to:
- Display available categories and prompts
- Fetch individual prompt content from the `contentUrl`
- Enable search and filtering functionality

To point the UI to this repository, configure the `MANIFEST_URL` in the UI application:
```typescript
const MANIFEST_URL = "https://raw.githubusercontent.com/your-username/ho-my-prompt/main/manifest.json";
```

## 📄 License

MIT

