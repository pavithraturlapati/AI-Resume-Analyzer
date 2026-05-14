AI Resume Analyzer Using Gemini And Python
INTRODUCTION
Welcome to the AI Resume Analyzer - your intelligent assistant for optimizing resumes and boosting job application success. This beginner-friendly project demonstrates how to leverage Large Language Models (LLMs) with prompt engineering techniques to automatically analyze and improve resume quality.
Instead of manually reviewing and improving resumes, this system allows you to:

Get expert analysis of resume strengths and weaknesses
Identify skill gaps and areas for improvement
Receive ATS optimization suggestions for better screening results
Generate professional improvements with actionable feedback
Process multiple formats (PDF and text files)
Boost job readiness with data-driven recommendations

Perfect for beginners learning AI integration, Prompt Engineering, and building practical career development tools!
WHAT THIS PROJECT DOES

Reads resume content from PDF or text files automatically
Extracts text from PDF documents using pypdf library
Generates comprehensive resume analysis with structured feedback
Demonstrates how role-based prompting leads to expert-level analysis
Handles errors gracefully with comprehensive exception handling
Provides a clean CLI interface for easy interaction
Uses Google's Gemini LLM for professional resume evaluation

The tool generates three powerful analysis sections:
Key Strengths Analysis

Identifies standout achievements and metrics
Highlights relevant technical skills
Recognizes quantifiable impact statements

Improvement Areas

Points out weak language and passive voice
Suggests stronger action verbs
Identifies missing context in experiences

ATS Compatibility Analysis

Evaluates keyword density for applicant tracking systems
Checks formatting compatibility
Suggests standard header usage

Professional Resume Rewrite

Generates improved version of your resume
Implements best practices automatically
Enhances action-oriented language

ARCHITECTURE AND SEQUENCE FLOW
User -> CLI Interface -> File Reader -> Text Extraction -> Prompt Builder -> Gemini LLM API -> Response Processor -> Formatted Output
Detailed Flow:

Application starts - User launches the CLI application
File type detection - System identifies PDF or text format
Content extraction - pypdf extracts text from PDF or reads text file
Prompt construction - Structured prompt with numbered requirements
API client initialization - Gemini client is created with API key
System instruction setup - Model is positioned as expert resume assistant
Content generation - Prompt is sent to Gemini API with temperature=1.0
Response processing - API response is formatted with sections
Error handling - Catches file, parsing, and API errors gracefully
Output display - Complete analysis with improved resume printed to console

PROMPT ENGINEERING USED
Role-Based System Instructions
system_instructions = "You are an expert resume writing assistant. Please analyze the following resume:"
Structured Prompting with Numbered Requirements
user_prompt = f"""
    Improve the following resume professionally.
    Also provide:
    1. Key strengths and skills highlighted in the resume.
    2. Areas for improvement in terms of content, structure, and formatting.
    3. ATS compatibility analysis and suggestions.

    Resume content:
    {content}
    """
Context Injection Pattern - Dynamically embeds resume content into the prompt template for reusability and maintainability.
Temperature Control - Uses higher temperature (1.0) for more creative improvements and diverse phrasings.
SAMPLE OUTPUT
--- Welcome to your AI Resume Analyzer! ---
Analyzing resume from file: data/My_Resume.pdf
Creating Gen AI client...
Analyzing resume... Please wait.

------------------------------------------------------------
This analysis provides a professionally rewritten version of the resume,
followed by an evaluation of strengths, areas for improvement, and ATS compatibility.

REWRITTEN RESUME

Christa Frank
Senior Machine Learning Engineer
Chicago, Illinois, US | 202-555-0120

PROFESSIONAL SUMMARY
Innovative Senior Machine Learning Engineer with over 4 years of experience
specializing in NLP, Conversational AI, and end-to-end ML lifecycles.

TECHNICAL SKILLS
- Languages: Python, Django, Flask, RASA, NLTK, TensorFlow, Keras
- ML/Data Science: Deep Learning, NLP, Sentiment Analysis, Data Wrangling
- Cloud & Tools: Azure ML Studio, AWS (ECS), Docker, Git, Jupyter Notebook
- Databases: MySQL, MongoDB, Microsoft SQL Server

ANALYSIS & FEEDBACK

1. Key Strengths and Skills
- Specialization in Conversational AI (Chatbots, RASA, NLP)
- Full-Stack ML Capability from data wrangling to deployment
- Strong Toolset with TensorFlow, Keras, and NLTK

2. Areas for Improvement
- Add quantifiable achievements (e.g. "Improved accuracy by 15%")
- Fix typos and encoding errors from the original
- Rewrite summary as a value proposition

3. ATS Compatibility Analysis
- Rich in high-value keywords (NLP, RASA, TensorFlow, Azure, Docker)
- Use a clean single-column layout for better ATS parsing
- Save and upload as a searchable PDF

4. Grammar and Action Verbs
- Replaced passive phrases with strong action verbs:
  Engineered, Architected, Optimized, Mentored
------------------------------------------------------------
LEARNING OUTCOMES
After completing this project, you will understand:

How to integrate Gemini LLM APIs using Python
How role-based system instructions influence AI behavior
How to implement structured prompt design for organized outputs
How to handle PDF parsing with pypdf library
How to process multi-format file input (PDF and text)
How to implement robust error handling for file operations
How to structure modular, maintainable code
How to manage API keys securely with environment variables

FUTURE ENHANCEMENTS

Web Interface with Streamlit
Advanced Analytics
Job Matching Features
Multi-Format Support
Batch Processing
Output Management
Multi-Language Support
Career Development Tools
Enterprise Features
Multiple Resume Format Generation
