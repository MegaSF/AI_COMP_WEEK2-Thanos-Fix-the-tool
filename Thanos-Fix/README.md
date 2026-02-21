# 🫰 Thanos Fix

> *"Dread it. Run from it. Destiny arrives all the same."*

A productivity tool that encourages fixing code issues quickly. If problems aren't resolved in time, half your codebase turns to dust. **Perfectly balanced, as all things should be.**

---

## 📦 Installation

No installation required — this is a conceptual tool specification designed to work with AI coding assistants.

Simply include `THANOS-FIX.md` in your project and invoke the tool through your AI assistant.

---

## 🚀 Quick Start

### 1. Basic Usage

Ask your AI assistant to run the Thanos fix:

```
Scan the project for issues and apply the Thanos fix workflow.
```

### 2. With Parameters

```json
{
  "name": "thanos-fix",
  "parameters": {
    "target_path": "./src",
    "timeout_minutes": 15,
    "delete_mode": "lines",
    "dry_run": true
  }
}
```

---

## ⚙️ Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target_path` | string | *required* | Path to the folder/project to snap |
| `timeout_minutes` | number | `30` | Time before the snap occurs |
| `delete_mode` | string | `"files"` | What to delete: `"files"`, `"lines"`, or `"both"` |
| `spare_patterns` | array | `[]` | Glob patterns for files that survive |
| `dry_run` | boolean | `true` | Preview without deleting (safety first!) |
| `dramatic_mode` | boolean | `true` | Print Thanos quotes during execution |

---

## 🎯 Delete Modes

### `"files"` Mode
Randomly selects 50% of files for deletion.

```
📁 project/
├── ✅ index.js      (survived)
├── 💨 utils.js      (dusted)
├── ✅ config.json   (survived)
└── 💨 helpers.js    (dusted)
```

### `"lines"` Mode
Randomly deletes 50% of code lines/functions within files.

```javascript
// ✅ Survived
export function addTask(tasks, title) { ... }

// 🫰 dusted by Thanos
// export function removeTask(tasks, id) { ... }

// ✅ Survived
export function completeTask(tasks, id) { ... }
```

### `"both"` Mode
Combines file and line deletion for maximum chaos.

---

## 🛡️ Safety Features

| Feature | Description |
|---------|-------------|
| `dry_run: true` | Default behavior — preview only, no actual deletion |
| `.thanos-backup` | Auto-created backup folder before snapping |
| `.gitignore` respect | Won't delete ignored files |
| Unsaved protection | Skips files with unsaved changes |
| System exclusions | Ignores `node_modules`, `.git`, etc. |

---

## 🎭 Dramatic Mode Quotes

When `dramatic_mode: true`, you'll see:

- *"Fun isn't something one considers when balancing the codebase. But this... does put a smile on my face."*
- *"You should have fixed the bugs."*
- *"I am inevitable."*
- *"Perfectly balanced, as all things should be."*
- *"A small price to pay for salvation."*
- *"The hardest choices require the strongest wills."*

---

## ⚠️ Error Codes

| Error | Meaning |
|-------|---------|
| `REALITY_STONE_MISSING` | Target path does not exist |
| `SOUL_STONE_DENIED` | Insufficient permissions |
| `TIME_STONE_PARADOX` | Negative timeout value |
| `MIND_STONE_CONFLICT` | Conflicting spare patterns |

---

## 🔄 Reversal (The Blip)

Made a mistake? Bring everything back:

### Option 1: Git Restore
```bash
git checkout -- .
```

### Option 2: Backup Restore
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

## 📋 Example Workflow

1. **Scan for issues**
   ```
   AI scans codebase for bugs, missing tests, lint errors
   ```

2. **Start countdown**
   ```
   ⏱️ 30 minutes to fix issues...
   ⏱️ 15 minutes remaining...
   ⏱️ 5 minutes remaining...
   ```

3. **The Snap** (if issues remain)
   ```
   🫰 *snap*
   💨 50% of code turns to dust
   ```

4. **Report**
   ```json
   {
     "snapped": true,
     "survivors": ["file1.js", "file2.js"],
     "dusted": ["file3.js", "file4.js"]
   }
   ```

---

## 🎮 Pro Tips

1. **Always start with `dry_run: true`** to preview what would be deleted
2. **Use `spare_patterns`** to protect critical files like `.env`, `package.json`
3. **Commit your code** before running with `dry_run: false`
4. **Set shorter timeouts** for more pressure (and more fun)

---

## ⚠️ Disclaimer

This tool is for **entertainment and productivity motivation purposes only**.

Not responsible for:
- Production incidents
- Lost code
- Existential dread
- Questioning the meaning of your codebase

*Tony Stark died for this.*

---

## 📜 License

MIT License — Use at your own risk.

*"I am... inevitable."* — Thanos, probably looking at your spaghetti code
