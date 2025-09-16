# learn-genai
Notes about getting started with Generative AI

## Repository Structure

This repository contains organized learning and project materials using Quarto documents:

### Learning Documents (l-0 to l-9)
- `l-0/` through `l-9/`: Learning-focused documents
- Each folder contains an `index.qmd` file with skeleton content

### Project Documents (p-0 to p-9)  
- `p-0/` through `p-9/`: Project-focused documents
- Each folder contains an `index.qmd` file with skeleton content

## Automatic PDF Generation

This repository includes a GitHub Actions workflow that automatically:

1. **Triggers** on any push to main/master when `.qmd` files are modified
2. **Detects** which Quarto files have changed using git diff
3. **Compiles** only the changed `.qmd` files to PDF format
4. **Commits** the generated PDFs back to the repository

### How to Use

1. Edit any `.qmd` file in the l-* or p-* folders
2. Commit and push your changes
3. The GitHub Action will automatically compile the changed files to PDF
4. The PDFs will be committed back to the same folders

### Manual Compilation

If you have Quarto installed locally, you can also compile documents manually:

```bash
# Compile a single document
quarto render l-0/index.qmd --to pdf

# Compile all documents
find . -name "*.qmd" -exec quarto render {} --to pdf \;
```
