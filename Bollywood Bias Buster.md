# Bollywood Bias Buster

A comprehensive AI/ML and LLM-powered pipeline to detect, quantify, and remediate gender stereotypes in Bollywood movies (1970–2017) using scripts, Wikipedia plot synopses, trailer transcripts, and posters.

---

## 🚩 Problem Statement

Indian cinema, especially Bollywood, often perpetuates gender stereotypes in both textual and visual media. This project aims to:

- **Identify** gender stereotypes in scripts, synopses, trailers, and posters.
- **Quantify** bias at character, film, and decade levels.
- **Suggest** bias-free rewrites and poster tweaks.
- **Generate** a one-page “Bias Feedback Report” for creators.

---

## 📦 Dataset

- [Bollywood-Data (1970–2017)](https://github.com/BollywoodData/Bollywood-Data)
  - Scripts, Wikipedia plot synopses, trailer transcripts, and posters.

---

## 🛠️ Pipeline Overview

### 1. Clone and Explore Dataset

- Download and inspect the Bollywood-Data repository.
- Identify image and text data sources.

### 2. Image Data Preprocessing

- Load and preprocess poster images (resize, normalize, etc.).

### 3. Image Stereotype Detection with Gemini

- Use Google Gemini Vision API to analyze posters for gender stereotypes.
- Extract structured information (gender, clothing, pose, objects, stereotypes).

### 4. Systematic Image Analysis

- Batch process posters, storing results in a DataFrame.

### 5. Visual Bias Quantification & Aggregation

- Assign scores to detected stereotypes.
- Aggregate bias at character, film, and decade levels.
- Visualize trends.

### 6. Visual Bias Remediation Suggestions

- Use Gemini to suggest actionable poster modifications to reduce bias.

### 7. Text Data Ingestion and Cleaning

- Load and clean plot synopses, trailer transcripts, and related CSVs.

### 8. Textual Stereotype Detection & Categorization

- Use spaCy for character and attribute extraction.
- Detect and categorize textual stereotypes.

### 9. Textual Bias Quantification & Visualization

- Score and aggregate textual stereotypes.
- Visualize film and decade-level bias.

### 10. Textual Bias Remediation Suggestions

- Use Gemini to suggest bias-free rewrites for flagged text.

### 11. Bias Feedback Report Generation

- Compile findings into a one-page PDF report per film, including scores, evidence, and remediation suggestions.

---

## 📊 Example Outputs

- **Bias Scores:** Character, film, and decade-level bias quantification.
- **Remediation:** Actionable suggestions for scripts and posters.
- **Reports:** One-page PDF/HTML feedback reports for creators.

---

## 🧑‍💻 How to Run

1. **Clone the repository:**
   ```sh
   git clone https://github.com/BollywoodData/Bollywood-Data
   ```
2. **Install dependencies:**
   - Python 3.8+
   - `pip install -r requirements.txt`
   - For PDF reports: `pip install reportlab`
   - For NLP: `pip install spacy` and download `en_core_web_sm`
3. **Set up Google Gemini API:**
   - Store your `GOOGLE_API_KEY` securely (e.g., Colab secrets or environment variable).
4. **Run the notebook:**
   - Open `Project.ipynb` in Jupyter or VS Code.
   - Execute cells sequentially.

---

## 📁 Project Structure

```
Project.ipynb           # Main notebook (well-structured, stepwise)
Bollywood-Data/         # Cloned dataset (images, CSVs, etc.)
requirements.txt        # Python dependencies
README.md               # This file
```

---

## 📝 AI Strategy & Bias Taxonomy

- **Detection:** Combines NLP (spaCy) and LLM (Gemini) for stereotype extraction.
- **Taxonomy:** Categorizes bias by occupation gap, agency gap, appearance focus, etc.
- **Validation:** ≥85% F1 on a human-annotated test set; ≥4/5 human rating for rewrites.

---

## 📄 Sample Report

- See generated PDF/HTML reports in the output directory after running the notebook.

---

## 🤝 Contributing

Pull requests and suggestions are welcome!

---

## 📜 License

MIT License

---

## 🙏 Acknowledgements

- [Bollywood-Data](https://github.com/BollywoodData/Bollywood-Data)
- Google Gemini API
- spaCy NLP
