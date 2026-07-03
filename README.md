# 🧠 AI Resume Analyzer Using Gemini & Python

## Introduction

Welcome to the **AI Resume Analyzer** — your intelligent assistant for optimizing resumes and boosting job application success.

This beginner-friendly project demonstrates how to leverage Large Language Models (LLMs) with prompt engineering techniques to automatically analyze and improve resume quality.

Instead of manually reviewing and improving resumes, this system allows you to:

- Get expert analysis of resume strengths and weaknesses
- Identify skill gaps and areas for improvement
- Receive ATS optimization suggestions for better screening results
- Generate professional improvements with actionable feedback
- Process multiple formats (PDF and text files)
- Boost job readiness with data-driven recommendations

Perfect for beginners learning AI integration, Prompt Engineering, and building practical career development tools!

---

## 🔍 What This Project Does

- Reads resume content from PDF or text files automatically
- Extracts text from PDF documents using the `pypdf` library
- Generates comprehensive resume analysis with structured feedback
- Demonstrates how role-based prompting leads to expert-level analysis
- Handles errors gracefully with comprehensive exception handling
- Provides a clean CLI interface for easy interaction
- Uses Google's Gemini LLM for professional resume evaluation

The tool generates four powerful analysis sections:

**Key Strengths Analysis**
- Identifies standout achievements and metrics
- Highlights relevant technical skills
- Recognizes quantifiable impact statements

**Improvement Areas**
- Points out weak language and passive voice
- Suggests stronger action verbs
- Identifies missing context in experiences

**ATS Compatibility Analysis**
- Evaluates keyword density for applicant tracking systems
- Checks formatting compatibility
- Suggests standard header usage

**Professional Resume Rewrite**
- Generates improved version of your resume
- Implements best practices automatically
- Enhances action-oriented language

---

## 🏗️ Architecture & Sequence Flow

```text
User
   ↓
CLI Interface
   ↓
File Reader
   ↓
Text Extraction
   ↓
Prompt Builder
   ↓
Gemini LLM API
   ↓
Response Processor
   ↓
Formatted Output
```

**Detailed Flow**

1. **Application starts** — User launches the CLI application
2. **File type detection** — System identifies PDF or text format
3. **Content extraction** — `pypdf` extracts text from PDF or reads text file
4. **Prompt construction** — Structured prompt with numbered requirements
5. **API client initialization** — Gemini client is created with API key
6. **System instruction setup** — Model is positioned as expert resume assistant
7. **Content generation** — Prompt is sent to Gemini API with `temperature=1.0`
8. **Response processing** — API response is formatted with sections
9. **Error handling** — Catches file, parsing, and API errors gracefully
10. **Output display** — Complete analysis with improved resume printed to console

---

## 🧪 Prompt Engineering Used

**Role-Based System Instructions**

```python
system_instructions = (
    "You are an expert resume writing assistant. "
    "Please analyze the following resume:"
)
```

**Structured Prompting with Numbered Requirements**

```python
user_prompt = f"""
Improve the following resume professionally.

Also provide:
1. Key strengths and skills highlighted in the resume.
2. Areas for improvement in terms of content, structure, and formatting.
3. ATS compatibility analysis and suggestions.

Resume content:
{content}
"""
```

**Context Injection Pattern** — Dynamically embeds resume content into the prompt template for reusability and maintainability.

**Temperature Control** — Uses higher temperature (`1.0`) for more creative improvements and diverse phrasings.

---

## 📄 Sample Output

```text
--- Welcome to your AI Resume Analyzer! ---

Analyzing resume from file: data/My_Resume.pdf
Creating Gen AI client...
Analyzing resume... Please wait.

------------------------------------------------------------

This analysis provides a professionally rewritten version
of the resume, followed by an evaluation of strengths,
areas for improvement, and ATS compatibility.

REWRITTEN RESUME

Christa Frank
Senior Machine Learning Engineer
Chicago, Illinois, US | 202-555-0120

PROFESSIONAL SUMMARY

Innovative Senior Machine Learning Engineer with over
4 years of experience specializing in NLP,
Conversational AI, and end-to-end ML lifecycles.

TECHNICAL SKILLS

- Languages: Python, Django, Flask, RASA, NLTK,
  TensorFlow, Keras
- ML/Data Science: Deep Learning, NLP,
  Sentiment Analysis, Data Wrangling
- Cloud & Tools: Azure ML Studio, AWS (ECS),
  Docker, Git, Jupyter Notebook
- Databases: MySQL, MongoDB, Microsoft SQL Server

ANALYSIS & FEEDBACK

1. Key Strengths and Skills
   - Specialization in Conversational AI
   - Full-Stack ML Capability
   - Strong Toolset with TensorFlow and Keras

2. Areas for Improvement
   - Add quantifiable achievements
   - Fix typos and encoding errors
   - Rewrite summary as a value proposition

3. ATS Compatibility Analysis
   - Rich in high-value keywords
   - Use clean single-column layout
   - Save and upload as searchable PDF

4. Grammar and Action Verbs
   - Replaced passive phrases with strong action verbs

------------------------------------------------------------
```

## 🎓 Learning Outcomes

After completing this project, you will understand:

- How to integrate Gemini LLM APIs using Python
- How role-based system instructions influence AI behavior
- How to implement structured prompt design for organized outputs
- How to handle PDF parsing with `pypdf`
- How to process multi-format file input
- How to implement robust error handling
- How to structure modular and maintainable code
- How to manage API keys securely using environment variables
