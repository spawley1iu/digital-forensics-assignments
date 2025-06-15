# Digital Forensics Assignments

This repository contains all of my Digital Forensics class work: source files, evidence, analysis scripts, polished reports, and daily activity logs.

---

## 📁 Repository Structure

```text
digital-forensics-assignments/       ← root directory
├── README.md                       ← project overview (this file)
├── .gitignore                      ← files/folders to ignore in Git
├── LICENSE.md                      ← project license
├── assignments/                    ← working files, scripts, raw data
│   ├── assignment-01/
│   │   ├── writeup.md              ← draft analysis and methodology
│   │   ├── evidence-images/        ← raw screenshots, captures, disk images
│   │   └── script-01.py            ← processing or parsing scripts
│   └── assignment-02/ …
├── reports/                        ← polished, exportable deliverables (PDF, HTML)
│   ├── assignment-01-report.pdf
│   └── assignment-02-report.pdf
├── logs/                           ← daily activity logs (YYYY-MM-DD.md)
│   ├── 2025-06-16.md
│   └── 2025-06-17.md
└── templates/                      ← reusable markdown/LaTeX/HTML templates
    ├── writeup-template.md
    └── html-report-template.html
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/digital-forensics-assignments.git
cd digital-forensics-assignments
```

### 2. Create a new assignment folder

For each new lab or case study:

```bash
mkdir -p assignments/assignment-03
cp templates/writeup-template.md assignments/assignment-03/writeup.md
```

### 3. Log your daily progress

At the end of each session, add a timestamped note:

```bash
cd logs
echo "- $(date +"%H:%M"): Investigated $TARGET_IMAGE using Autopsy." \
  >> $(date +"%Y-%m-%d").md
```

### 4. Produce a final report

Use the HTML template to render polished reports:

```bash
pandoc assignments/assignment-03/writeup.md \
  --template=templates/html-report-template.html \
  -o reports/assignment-03-report.html
```

> Tip: Adjust the template’s `<head>` to include Bootstrap’s CDN for styling.

---

## 🛠️ Tools & Dependencies

* **Autopsy**, **FTK Imager**, **Binwalk**, **Volatility**
* **Python 3.x** (with `pytsk3`, `pandas`, `matplotlib`)
* **Pandoc** (for Markdown → HTML/PDF)

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE.md](LICENSE.md) for details.

---

*Last updated: 2025-06-15*
