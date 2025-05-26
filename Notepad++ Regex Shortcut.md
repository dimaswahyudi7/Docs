# 📌 Notepad++ Regex Shortcut: Replace First Semicolon with " #"

This is a quick reference for converting the **first semicolon** (`;`) on each line of a text file into a **space + hash** (` #`), using Notepad++ and regular expressions.

---

## 🔍 Find & Replace Settings

* **Find what:**

  ```regex
  ^([^;]*);
  ```

  * `^` asserts start of line.
  * `([^;]*)` captures everything up to the first semicolon.
  * `;` matches the first semicolon.

* **Replace with:**

  ```text
  $1 #
  ```

  * `$1` re-inserts the captured group (text before `;`).
  * ` #` adds a space and hash in place of the semicolon.

* **Search Mode:** Regular expression

* **Apply to:** Entire document or selection

---

## 📝 Example

| **Input Line**           | **After Replace**         |
| ------------------------ | ------------------------- |
| `154.81.156.54;100;...`  | `154.81.156.54 #100;...`  |
| `206.168.34.169;100;...` | `206.168.34.169 #100;...` |

---

> 💡 **Tip:** This trick is useful when you need to insert a comment marker (`#`) after the first field in semicolon‑delimited data (e.g. CSV exported with `;`) without touching subsequent semicolons.

---

*Documented by [Dimas Wahyudi](https://github.com/dimaswahyudi7)*

---

## 📚 Documentation Index

Add additional manuals and guides here as your needs grow. Create new Markdown files under a `/docs` folder and link them below:

* **Regex Shortcuts**: `docs/regex-shortcuts.md` — Notepad++ regex tips (this document).
* **PowerShell Scripts**: `docs/powershell-scripts.md` — Scripts for IoC validation, VirusTotal checks, etc.
* **Excel Tips**: `docs/excel-csv-conversion.md` — How to export/import CSV with comma delimiters.
* **Repository Structure**: `docs/repo-structure.md` — Guidelines for organizing IoC Collections repo.

You can add more entries as you document new workflows or tools.([https://github.com/dimaswahyudi7](https://github.com/dimaswahyudi7))\*
