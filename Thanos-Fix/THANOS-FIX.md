# 🫰 Thanos Fix

> *"I am inevitable."* — Your codebase, probably

## Tool Specification

```yaml
name: thanos-fix
version: 1.0.0
author: The Mad Titan
```

## Description

A tool to encourage getting problems in code solved quickly and efficiently. If a certain amount of time has passed and nothing has been fixed, randomly delete half of the project. Perfectly balanced, as all things should be.

## Parameters

| Parameter | Type | Required | Default | Description |
|-----------|------|----------|---------|-------------|
| `target_path` | string | Yes | - | The path to the folder/project to snap |
| `timeout_minutes` | number | No | 30 | Time before the snap occurs |
| `delete_mode` | string | No | `"files"` | What to delete: `"files"`, `"lines"`, or `"both"` |
| `spare_patterns` | array | No | `[]` | Glob patterns for files that survive (e.g., `["*.env", "package.json"]`) |
| `dry_run` | boolean | No | `true` | Preview the snap without actually deleting (safety first!) |
| `dramatic_mode` | boolean | No | `true` | Print Thanos quotes during execution |

## Usage Example

```json
{
  "name": "thanos-fix",
  "parameters": {
    "target_path": "./src",
    "timeout_minutes": 15,
    "delete_mode": "files",
    "spare_patterns": [".env", "package-lock.json"],
    "dry_run": false,
    "dramatic_mode": true
  }
}
```

## Behavior

1. **Initialization**: Tool starts a countdown timer
2. **Warning Phase**: Periodic warnings as deadline approaches
3. **The Snap**: If issues aren't resolved:
   - Randomly selects 50% of eligible files/lines
   - Deletes them with extreme prejudice
   - Logs what was "dusted" for potential recovery

## Output

```json
{
  "snapped": true,
  "survivors": ["file1.ts", "file2.ts"],
  "dusted": ["file3.ts", "file4.ts"],
  "total_files_before": 100,
  "total_files_after": 50,
  "thanos_quote": "I used the stones to destroy the stones."
}
```

## Thanos Quotes (for `dramatic_mode`)

- *"Fun isn't something one considers when balancing the codebase. But this... does put a smile on my face."*
- *"You should have fixed the bugs."*
- *"I am inevitable."*
- *"Perfectly balanced, as all things should be."*
- *"A small price to pay for salvation."*
- *"The hardest choices require the strongest wills."*
- *"Dread it. Run from it. Destiny arrives all the same."*

## Safety Features

⚠️ **IMPORTANT**: This tool is for entertainment purposes only!

- `dry_run` defaults to `true` — opt-in to actual deletion
- Creates a `.thanos-backup` folder before snapping
- Respects `.gitignore` patterns by default
- Won't delete files with unsaved changes
- Excludes `node_modules`, `.git`, and other system folders

## Error Handling

| Error | Description |
|-------|-------------|
| `REALITY_STONE_MISSING` | Target path does not exist |
| `SOUL_STONE_DENIED` | Insufficient permissions |
| `TIME_STONE_PARADOX` | Negative timeout value |
| `MIND_STONE_CONFLICT` | Conflicting spare patterns |

## Reversal (The Blip)

If you regret the snap:

```json
{
  "name": "thanos-fix-undo",
  "parameters": {
    "backup_path": "./.thanos-backup",
    "restore_all": true
  }
}
```

---

*Disclaimer: Not responsible for any production incidents, lost code, or existential dread. Use at your own risk. Tony Stark died for this.*