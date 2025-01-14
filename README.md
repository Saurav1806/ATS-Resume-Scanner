#Resume Analysis with Gemini AI

This Python script analyzes a resume (PDF format) against a job description using Google Generative AI (Gemini AI). It extracts the first page of the resume as an image, processes it, and generates a detailed analysis including strengths, weaknesses, missing skills, and acceptance probability. The final output is saved as a Word document.
Features

- Processes resumes in **PDF** format.
- Generates analysis on:
  - Strengths and weaknesses.
  - Missing skills or certifications based on the job description.
  - Suggestions for improvement.
  - Acceptance probability in ATS (Applicant Tracking System).
- Saves the analysis in a structured Word document.
  
#Requirements

- Python 3.7 or higher.
- Poppler (required for pdf2image library to process PDFs).

  
Python Libraries
The script uses the following libraries:
- os (built-in)
- io (built-in)
- base64 (built-in)
- docx (install via python-docx)
- google.generativeai
- pdf2image

  
#Installation
1. **Install Python Dependencies**
Run the following command to install the required Python libraries:
pip install python-docx pdf2image google-generativeai
2. **Install Poppler**
Windows
- Download the latest Poppler binary for Windows from Poppler for Windows.
- Extract the downloaded zip file to a directory (e.g., C:\poppler).
- Add the Poppler `bin` directory (e.g., C:\poppler\bin) to your system's `PATH`.
Linux
- Use your package manager to install Poppler:
  sudo apt update
  sudo apt install poppler-utils
macOS
- Install using Homebrew:
  brew install poppler

  
Usage
1. **Add Your Generative AI API Key**
Open the script and add your API key in the following line:
genai.configure(api_key="YOUR_API_KEY_HERE")
2. **Run the Script**
Run the script from your terminal or command prompt:
python script_name.py
3. **Input Details**
- Provide the full path to the resume file (PDF).
- Enter the job description for analysis.
4. **Output**
- The analysis will be saved as a Word document in the same directory as the input file, with `_output` appended to the original file name.
Output Example
The Word document includes:
1. Overall Analysis: Highlights strengths and weaknesses of the resume.
2. Missing Skills and Certifications: Lists the skills required but missing.
3. Improvement Suggestions: Actionable tips to optimize the resume.
4. ATS Acceptance Probability: Likelihood of the resume being accepted by an ATS system.
Troubleshooting

### Common Errors
1. **FileNotFoundError**:
   - Ensure the provided file path is correct and the file exists.
2. **Poppler Not Found**:
   - Make sure Poppler is installed and added to the system `PATH`.
3. **Google Generative AI Key Issues**:
   - Check if the API key is correct and has sufficient permissions.
   
Logs
The script prints status messages (e.g., "Processing resume...") for better debugging.

Additional Notes
- The script processes only the **first page** of the resume for analysis.
- Ensure that the API key for Google Generative AI has appropriate quotas and permissions.

  
License
This script is open-source and provided under the MIT License. Feel free to modify and enhance it.
