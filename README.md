# RVCE Major Project Report - LaTeX Template

This repository contains a modular, production-ready LaTeX template for the VIII Semester Major Project Report at RV College of Engineering (RVCE).

## Prerequisites

You can use this template either locally on your computer or online using Overleaf.

**Option 1: Local Environment (Recommended for privacy and speed)**
* A LaTeX distribution: [MiKTeX](https://miktex.org/) (Windows) or [TeX Live](https://tug.org/texlive/) (Linux/Windows) or [MacTeX](https://www.tug.org/mactex/) (macOS).
* An editor: [Visual Studio Code](https://code.visualstudio.com/) with the **LaTeX Workshop** extension.

**Option 2: Overleaf (Easiest setup)**
* An account on [Overleaf](https://www.overleaf.com/).
* Simply compress this entire folder into a `.zip` file and upload it as a new project on Overleaf.

## Project Structure

The project is broken down into manageable files so you don't have to navigate a single massive document:

```text
project-report-template/
├── main.tex                 # The root file (compile this file)
├── config/                  
│   ├── metadata.tex         # EDIT THIS FIRST: Contains all your names, USNs, and titles
│   └── settings.tex         # DO NOT EDIT: Contains margin, font, and style rules
├── frontmatter/             # Cover pages, certificates, declarations, abstract
├── chapters/                # Your actual report content (Introduction, Theory, etc.)
├── backmatter/              # References and Appendices
└── assets/                  # Folder for all your images, logos, and QR codes

```

## Step-by-Step Instructions

### Step 1: Update Your Project Metadata

To prevent repetitive typing, all student names, guide details, and project titles are centralized.

1. Open `config/metadata.tex`.
2. Fill in your specific Project Title, Branch, Academic Year, Student Names, USNs, and Guide details.
3. These variables will automatically populate the cover pages, certificate, and declaration.

### Step 2: Add Required Assets

The template requires a few images to compile correctly without placeholder errors.

1. Place your department's/college's logo in `assets/logos/` and name it `rsst_logo.png` (or update the filename in the `.tex` files).
2. Generate a QR code for your project (as per guidelines) and place it in `assets/images/` as `qrcode.png`. Update the reference in `frontmatter/01_external_cover.tex`.

### Step 3: Edit the Frontmatter

1. Open the files in the `frontmatter/` folder one by one.
2. `05_acknowledgement.tex`: Type your acknowledgements.
3. `06_abstract.tex`: Write your 3-paragraph abstract.
4. `07_publications.tex`: Add your publication details if any.

*Note on Watermarks:* The certificate and declaration files use a faded background logo. If the logo is not perfectly centered, you can adjust the `\\raisebox{...}` and `\\hspace{...}` values in `03_certificate.tex` and `04_declaration.tex`.

### Step 4: Write Your Chapters

1. Add your content to the files in the `chapters/` directory.
2. Use `\\chapter{Title}`, `\\section{Title}`, and `\\subsection{Title}` to structure your text.
3. To add more chapters, create new `.tex` files (e.g., `03_methodology.tex`) and include them in `main.tex` using `\\include{chapters/03_methodology}`.

### Step 5: Manage References

1. Open `backmatter/references.bib`.
2. Add your citations in BibTeX format. You can easily get BibTeX citations from Google Scholar by clicking the "Cite" button.
3. Cite them in your chapters using `\\cite{citation_key}`.

### Step 6: Plagiarism Report

1. Add your plagiarism/AI report screenshots to `backmatter/appendices.tex`.

## Compilation Instructions

**If using VS Code locally:**

1. Open `main.tex` and make it the active tab.
2. Press `Ctrl + Alt + B` (Windows/Linux) or `Cmd + Option + B` (Mac) to build.
3. **Important:** Because of the bibliography and table of contents, LaTeX must compile multiple times. If your citations show up as `[?]`, force a full build recipe:
* Press `Ctrl + Shift + P` -> `LaTeX Workshop: Build with recipe` -> Select `pdflatex -> bibtex -> pdflatex x2`.



**If using Overleaf:**

1. Overleaf handles multiple compilations automatically. Just click the green **Recompile** button.