# Resume_Parser-Python-version


#  Resume Parser & Formatter with Gemini LLM

This Python-based application extracts, parses, and reformats resumes (PDF or DOCX) into a standardized, company-branded Word format using Google Gemini LLM and `python-docx`.


---

## Features

- Extracts text from PDF and DOCX files
- Uses Gemini API to parse structured resume data (name, contact, skills, experience, etc.)
-  Generates clean, company-standardized Word documents with:
  - Logo header
  - Footer contact details
  - Candidate strengths summary
  - Skill matrix (up to 10 rows)
  - Proper section formatting (bold, underline, line spacing, etc.)
-  Supports both raw skill list and detailed skill matrix

---

## Project Structure

```
resume_parser/
│
├── resume_parser.py         # Main script: extract, parse, and generate docx
├── requirements.txt         # Required dependencies
├── logo.png                 # (Optional) Logo to appear on top-right of resume
├── parsed_resume.json       # Output: structured JSON (optional)
├── .env                     # Contains your Gemini API key
└── resume_format_trials/    # Output directory for formatted resumes
```

---

## Setup Instructions

### 1. Clone this repository

```bash
git clone https://github.com/yourusername/resume-parser-llm.git](https://github.com/Quadrant-AI/Resume_Parser-Python-version.git

cd Resume_Parser-Python-version
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Setup Gemini API Key

Create a `.env` file with your [Google Gemini API key](https://makersuite.google.com/app/apikey):

```
GEMINI_API_KEY=your_api_key_here
```

### 4. Add Your Resume Files

Place `.pdf` or `.docx` resume files into any folder. Then update `resume_path` in `resume_parser.py`.

---

##  How to Run

```bash
python resume_parser.py
```

The script will:
- Extract text
- Use LLM to parse details into structured JSON
- Generate a formatted Word document in the `resume_format_trials/` folder

 Output file name: `First_Last_resume.docx` (cleaned safely from the name field)

---

## Technologies Used

- `python-docx` for document creation
- `PyMuPDF` for PDF text extraction
- `Google Generative AI` (Gemini) for parsing unstructured text
- `dotenv` for managing API keys

---

## Limitations

- LLM parsing depends on resume clarity and formatting
- Does not yet extract embedded images, shapes, or graphs
- No GUI or web interface yet (CLI only)

---

## TODO (Pull Requests Welcome)

- [ ] Add Gradio or Streamlit UI
- [ ] Upload multiple resumes in bulk
- [ ] Add CSV export of parsed metadata
- [ ] Extract hyperlinks (LinkedIn, GitHub) even if inside headers/footers

---

## License

MIT License – Use freely for personal and commercial use.

---

## Author

Developed by [Your Name]  
For support or suggestions: your.email@example.com
