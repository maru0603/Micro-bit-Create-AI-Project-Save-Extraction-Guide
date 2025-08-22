# Micro\:bit Create AI – Project Save & Extraction Guide

A hands-on documentation on how to save, re-import, and extract source files (like `main.py` and `dataset.json`) when working with the **micro\:bit Create AI** platform. This guide explains the role of the `.hex` project file, how it differs from traditional MakeCode files, and how to manage your code and dataset effectively.

---

❓ **Problem We’re Trying to Solve**

Working with AI on the BBC micro\:bit through Create AI often confuses beginners when it comes to saving and retrieving project files. Common issues include:

* Projects are saved as **`.hex` files** (compiled + bundled) instead of `.mkcd` or `.zip`.
* Many assume `.hex` is only for flashing the device, not realizing it also stores the dataset and code.
* Difficulty extracting or recovering project files after download.
* Lack of clear documentation on how to re-import `.hex` back into Create AI for continued editing.

This guide bridges that gap by showing how `.hex` works as both a program **and** a project container.

---

📊 **Why This Matters**

* **Beginners** often lose access to their training data (`dataset.json`) because they only save `.hex`.
* **Educators** need a clear workflow to help students save and reload projects across sessions.
* **Developers** may want to extract raw files (`main.py`, `main.ts`, `pxt.json`) for version control.

---

🌟 **Core Philosophy**

* **Accessible** – Save and restore projects without technical confusion.
* **Reliable** – Ensure datasets and code aren’t lost after flashing.
* **Practical** – Use `.hex` both as executable and backup project file.
* **Transparent** – Understand what’s inside a `.hex` and when to use `.mkcd`.

---

🎯 **Key Features of Create AI Save System**

* **Save as `.hex`**

  * Contains code, dataset, actions, and compiled firmware.
  * Can be flashed directly to micro\:bit.
  * Can be re-imported into Create AI to restore project.

* **Re-import Project**

  * Drag `.hex` into Create AI’s homepage → Explorer restores `main.py`, `dataset.json`, etc.

* **Cross-Compatibility**

  * `.hex` can also be opened in **Microsoft MakeCode**, but dataset editing is limited there.

---

👥 **User Workflows**

**Student Workflow**

1. Train an AI model (actions, samples).
2. Click **Download (hex)**.
3. Next session → Import `.hex` back into Create AI → continue editing.

**Educator Workflow**

* Collect `.hex` files from students.
* Re-import into Create AI for review, debugging, or showcasing.

**Developer Workflow**

* Re-import `.hex` into Create AI.
* Use Explorer panel to copy/export raw files (`main.py`, `dataset.json`).
* Commit them into GitHub for version tracking.

---

🏗️ **Technical Architecture of Save/Load**

* **`.hex` file**: Combines

  * Program firmware
  * Project metadata (`pxt.json`)
  * AI dataset (`dataset.json`)
  * Source code (`main.py`, `main.ts`)

* **Import pipeline**:

  * Create AI reads `.hex`
  * Extracts embedded project bundle
  * Restores Explorer file structure

---

🚀 **Getting Started**

**To Save Project**

1. In Create AI editor → Click purple **Download**.
2. Save `.hex` to your computer.

**To Re-import Project**

1. Open [MakeCode Create AI](https://makecode.microbit.org/ai).
2. Click **Import → Import File**.
3. Choose the `.hex` you saved.
4. Your project Explorer will reappear with `main.py`, `dataset.json`, etc.

---

📱 **Example User Journeys**

* **Maru the Student**: Trains toy movement AI → saves `.hex` → reopens it next week to continue.
* **Teacher**: Collects 20 `.hex` projects from class → imports them into Create AI for grading.
* **Hobbyist**: Saves `.hex` → re-imports to export `dataset.json` → uploads it to GitHub.

---

🔮 **Future Roadmap**

* **Direct `.zip` export** option to download raw files instantly.
* **Integration with GitHub** inside Create AI for versioned storage.
* **Dataset visualizer** to preview `dataset.json` before flashing.

---

📈 **Success Metrics**

* **Recovery Rate** – % of projects successfully re-imported from `.hex`.
* **Classroom Adoption** – Number of educators using `.hex` workflow for students.
* **Data Safety** – Reduced cases of lost `dataset.json` or project files.

---

🤝 **Contributing**

* Share tips for managing Create AI `.hex` files.
* Suggest tooling to auto-extract raw files for GitHub workflows.

---

📄 **License**

This workflow guide is released under **Creative Commons Attribution (CC BY 4.0)** for free use in classrooms and workshops.
