# 🧰 Activity 2: VS Code Extension Tour & Productivity Ecosystem
### Portfolio Building Studio (`B25CS0311` / `B25GE0101`) — 3rd Semester B.Tech (CSIT)

[![Course](https://img.shields.io/badge/Course-B25CS0311%20Portfolio%20Building-blue.svg)](https://github.com/KudoKode)
[![Student](https://img.shields.io/badge/Student-Abhishek%20Maurya-green.svg)](https://github.com/KudoKode)
[![SRN](https://img.shields.io/badge/SRN-R25EJ004-orange.svg)](https://github.com/KudoKode)
[![Institution](https://img.shields.io/badge/University-REVA%20University-red.svg)](https://www.reva.edu.in)
[![Status](https://img.shields.io/badge/Status-Completed%20%26%20Verified-brightgreen.svg)](README.md)

---

## 🎯 1. Objective & Scope

To explore, configure, and evaluate five core Visual Studio Code extensions—**Python**, **Java Extension Pack**, **Prettier**, **GitLens**, and **Live Share**—analyzing how language servers, automated formatters, VCS telemetry, and real-time collaborative environments transform the modern software engineering workflow.

---

## 📦 2. Installed Extensions & Verification Matrix

| Extension | Publisher | Category | Primary Feature Explored | Verification File | Status |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **Python** | Microsoft | Language Server / Tooling | IntelliSense, virtual environment detection, direct terminal execution | [`test.py`](test.py) | ✅ Verified |
| **Java Extension Pack** | Microsoft | Language Runtime | JDT Language Server, Codelens `Run \| Debug` integration | [`Test.java`](Test.java) | ✅ Verified |
| **Prettier** | Esben Petersen | Code Formatter | AST-driven automated code formatting, Format-on-Save | [`sample_unformatted.html`](sample_unformatted.html) ➔ [`sample_formatted.html`](sample_formatted.html) | ✅ Verified |
| **GitLens** | GitKraken | Version Control Telemetry | Inline commit blame annotations, commit graph, file history timeline | `.git` repo history | ✅ Verified |
| **Live Share** | Microsoft | Collaborative Coding | Simultaneous multi-cursor pair programming, shared terminal | Paired with `@hkarun311-source` | ✅ Verified |

---

## 📊 3. Part B: Comparative Evaluation Matrix

| Dimension | Python (Microsoft) | Java Extension Pack | Prettier Formatter | GitLens Supercharged | Live Share |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Primary Focus** | Syntax, Linting & Debugging | Compile, Run & Test Runner | Code aesthetics & consistency | Git history & blame context | Synchronous pair programming |
| **Trigger Mechanism** | File activation (`.py`) | File activation (`.java`) | On Save (`Ctrl+S`) or manual (`Shift+Alt+F`) | Inline on cursor line | Active session invite link |
| **Typing Impact** | Autocomplete suggestions, docstrings | Strong static type checks, import cleanup | Automatic indentation & quotes normalization | Passive line-end telemetry | Live remote cursor presence |
| **Scope** | Language-specific | Language-specific | Universal (HTML, JS, CSS, JSON) | Universal (any Git repo) | Universal (any workspace) |
| **Resource Footprint** | Moderate (Pylance daemon) | Heavy (Java Language Server) | Negligible (Fast AST parser) | Low–Moderate (Background git index) | Low (WebRTC / Cloud relay) |

---

## 💬 4. Model Answers to Part B Reflection Questions

### Q1: Which extension changed your day-to-day typing/editing experience the most?
> **Answer:** **Prettier**. By configuring `"editor.formatOnSave": true` in [`.vscode/settings.json`](.vscode/settings.json), the mental overhead of manually indenting tags, aligning brackets, and managing trailing commas was completely eliminated. Developers can write code quickly without obsessing over formatting aesthetics, knowing that the Abstract Syntax Tree (AST) will standardize the entire file cleanly on every save.

### Q2: Which extension is about the code itself (correctness/formatting) vs. about collaboration/history?
> **Answer:**
> - **Code Correctness & Formatting:** **Python**, **Java Extension Pack**, and **Prettier** operate directly on the source text—enforcing type rules, identifying syntax bugs before runtime, and maintaining architectural cleanliness.
> - **Collaboration & History:** **GitLens** and **Live Share** operate on team meta-layers. GitLens exposes *who* wrote each line and *why* (via commit messages and git blame), while Live Share enables *real-time pair programming* without physical co-location.

### Q3: Which extension would you keep enabled for every project, and which only for specific languages?
> **Answer:**
> - **Keep Globally Enabled (All Projects):** **Prettier** and **GitLens**. Regardless of whether the project is C, Web, Python, or Markdown, automated formatting and commit blame context are universally valuable across all engineering disciplines.
> - **Enable Language-Specifically:** **Python** and **Java Extension Pack**. The Java Language Server and Pylance spin up heavy background processes (consuming 300MB–800MB of RAM). They should be activated only in dedicated language workspaces to ensure the editor remains lightweight.

### Q4: How did Live Share change the feeling of pair programming compared to screen sharing?
> **Answer:** Traditional screen sharing is passive and restrictive: one developer drives while the other watches, creating spectator fatigue and friction when navigating between related files. In contrast, **Live Share** provides bidirectional autonomy. Both engineers have independent cursors, can work in different files simultaneously, explore local definitions independently, and share terminal outputs directly—turning pair programming into a collaborative sprint rather than an observer session.

---

## 🖥️ 5. Terminal Execution Verification

### Python Verification ([`test.py`](test.py))
```powershell
PS C:\Users\Abhilasha Maurya\Documents\GitHub\Activity-2-VSCode-Extension-Tour> python test.py
=======================================================
[*] Hello from Python! VS Code Python Extension Active.
[*] IntelliSense, Linter, and Python Debugger Verified.
=======================================================
```

### Prettier Formatting Diff Demonstration
**Before Formatting ([`sample_unformatted.html`](sample_unformatted.html)):**
```html
<!DOCTYPE html><html><head><title>Unformatted Sample</title><style>
body{background:#111;color:#fff;}h1{font-size:2rem;margin-bottom:10px}
p{line-height:1.5}
</style></head><body><div><h1>Messy HTML for Prettier Tour</h1>
<p>This file has deliberately inconsistent indentation and minified tags to demonstrate Prettier's AST-based code formatting.</p>
<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li>
</ul></div></body></html>
```

**After Prettier Format-On-Save ([`sample_formatted.html`](sample_formatted.html)):**
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Formatted Sample</title>
    <style>
      body {
        background: #111;
        color: #fff;
      }
      h1 {
        font-size: 2rem;
        margin-bottom: 10px;
      }
      p {
        line-height: 1.5;
      }
    </style>
  </head>
  <body>
    <div>
      <h1>Messy HTML for Prettier Tour</h1>
      <p>
        This file has deliberately inconsistent indentation and minified tags to
        demonstrate Prettier's AST-based code formatting.
      </p>
      <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
      </ul>
    </div>
  </body>
</html>
```

---

## 📑 6. Quick-Reference Cheat Sheet (VS Code Extensions)

| Category | Command / Shortcut | Description / Action |
| :--- | :--- | :--- |
| **Extensions View** | `Ctrl + Shift + X` | Open Extensions marketplace panel |
| **Format Document** | `Shift + Alt + F` | Reformat current file using Prettier rules |
| **Format Selection**| `Ctrl + K, Ctrl + F` | Format only highlighted text block |
| **Run Python File** | `Run ▷` button or `Ctrl + F5` | Execute active Python script in integrated terminal |
| **Select Interpreter**| `Ctrl + Shift + P` ➔ `Python: Select Interpreter` | Switch between Python versions or active virtualenvs |
| **Java Run / Debug** | Click Codelens above `main()` | Compile and execute class without manual command lines |
| **GitLens Line Blame**| Line cursor hover | View author, date, and commit hash for the current line |
| **GitLens Graph** | Activity Bar ➔ GitLens ➔ Commit Graph | Visualize Git branches, heads, and merge commits |
| **Live Share Start** | Status Bar ➔ Live Share ➔ Start | Generate read/write collaboration invite URL |
| **Live Share Join**  | Status Bar ➔ Live Share ➔ Join | Paste partner link to join active collaborative session |

---

## 🤝 7. Collaborative Pair Details

- **Host Engineer:** Abhishek Maurya (`R25EJ004` / [@KudoKode](https://github.com/KudoKode))
- **Guest / Peer Engineer:** Arun H Kalamuddi (`R25EJ013` / [@hkarun311-source](https://github.com/hkarun311-source))
- **Pairing Activity:** Live Share session co-authoring C functions and verifying GitLens blame attribution in `R25EJ004-portfolio`.

---

*Submitted for Portfolio Building Studio (`B25CS0311`), REVA University, Bengaluru.*
