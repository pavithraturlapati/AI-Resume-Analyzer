AI Resume Analyzer Using Gemini And Python

Introduction
Welcome to the AI Resume Analyzer - your intelligent assistant for optimizing resumes and boosting job application success! This beginner-friendly project demonstrates how to leverage Large Language Models (LLMs) with prompt engineering techniques to automatically analyze and improve resume quality.

Instead of manually reviewing and improving resumes, this system allows you to:

Get expert analysis of resume strengths and weaknesses
Identify skill gaps and areas for improvement
Receive ATS optimization suggestions for better screening results
Generate professional improvements with actionable feedback
Process multiple formats (PDF and text files)
Boost job readiness with data-driven recommendations
Perfect for beginners learning AI integration, Prompt Engineering, and building practical career development tools!

What This Project Does
Reads resume content from PDF or text files automatically
Extracts text from PDF documents using pypdf library
Generates comprehensive resume analysis with structured feedback
Demonstrates how role-based prompting → expert-level analysis
Handles errors gracefully with comprehensive exception handling
Provides a clean CLI interface for easy interaction
Uses Google's Gemini LLM for professional resume evaluation
The tool generates three powerful analysis sections:

Key Strengths Analysis
Identifies standout achievements and metrics
Highlights relevant technical skills
Recognizes quantifiable impact statements
Perfect for understanding your competitive advantages
Improvement Areas
Points out weak language and passive voice
Suggests stronger action verbs
Identifies missing context in experiences
Recommends technical depth enhancements
Great for targeted resume refinement

ATS Compatibility Analysis
Evaluates keyword density for applicant tracking systems
Checks formatting compatibility
Suggests standard header usage
Provides customization strategies for specific jobs
Perfect for passing automated screening

Professional Resume Rewrite
Generates improved version of your resume
Implements best practices automatically
Enhances action-oriented language
Strengthens technical descriptions

Learning Outcomes
After completing this project, you will understand:
How to integrate Gemini LLM APIs using Python
How role-based system instructions influence AI behavior
How to implement structured prompt design for organized outputs
How to handle PDF parsing with pypdf library
How to process multi-format file input (PDF and text)
How to implement robust error handling for file operations
How to structure modular, maintainable code
How to manage API keys securely with environment variables
Context injection techniques for dynamic prompts
This project strengthens both AI integration skills and practical application development best practices.


Architecture & Sequence Flow
User -> CLI Interface -> File Reader (PDF/Text Parser) -> Text Extraction -> Structured Prompt Builder -> Gemini LLM API (with Role Instructions) -> Response Processor -> Formatted Analysis + Improved Resume Display
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

Prompt Engineering Used
We have used following prompt techniques to ensure AI behaves reliably. Here is the breakdown.

Role-Based System Instructions
The application uses system instructions to establish AI's expertise:

system_instructions = "You are an expert resume writing assistant. Please analyze the following resume:"
Why Role-Based Prompting?

Positions AI as a domain expert (resume writing)
Ensures professional tone and vocabulary
Improves analysis depth and quality
Provides consistent perspective across analyses
Activates relevant knowledge domains in the model
Structured Prompting with Numbered Requirements
The prompt includes explicit numbered sections for organized output:

user_prompt = f"""
    Improve the following resume professionaly.
    Also provide:
    1. Key strengths and skills highlighted in the resume.
    2. Areas for improvement in terms of content, structure, and formatting.
    3. ATS (Applicant Tracking System) compatibility analysis and suggestions.

    Resume content:
    {content}
    """
Key characteristics:

Numbered items (1, 2, 3) ensure organized, multi-faceted output
Clear section headers separate instructions from data
Explicit deliverables prevent incomplete responses
Comprehensive coverage of analysis dimensions
Context Injection Pattern
Dynamically embeds resume content into prompt template:

f"""Resume content:
{content}
"""
Benefits:

Separates structure from data for reusability
Clear data boundaries with section headers
Dynamic content insertion without hardcoding
Maintainable prompt templates
Task-Specific Prompt Design
The prompt is optimized for resume analysis:

"Improve the following resume professionaly."
Key characteristics:

Action-oriented verb ("Improve", "Analyze")
Professional context specification
Multiple analysis dimensions
Specific domain focus (ATS, structure, content)
Temperature Control for Creativity
Uses higher temperature (1.0) for creative improvements:

TEMPERATURE = 1
Benefits:

More creative rewording and suggestions
Diverse phrasings for improvements
Natural language variations
Balanced between creativity and coherence

Sample Output

--- Welcome to your AI Resume Analyzer! ---
Analyzing resume from file: data/My_Resume.pdf
Creating Gen AI client...
Analyzing resume... Please wait.

------------------------------------------------------------
This analysis provides a professionally rewritten version of the resume, followed by an evaluation of strengths, areas for improvement, and ATS compatibility.

---

# REWRITTEN RESUME

**Christa Frank**
**Senior Machine Learning Engineer**
Chicago, Illinois, US | 202-555-0120
info@resumekraft.com | linkedin.com/resumekraft | ResumeKraft.com

### **PROFESSIONAL SUMMARY**
Innovative Senior Machine Learning Engineer with over 4 years of experience specializing in NLP, Conversational AI, and end-to-end ML lifecycles. Proven track record in designing and deploying scalable AI solutions using RASA, TensorFlow, and Azure ML Studio. Expert in bridging the gap between technical execution and business strategy to solve complex real-world problems.

### **TECHNICAL SKILLS**
*   **Languages & Frameworks:** Python (Expert), Django, Flask, RASA, NLTK, TensorFlow, Keras.
*   **ML/Data Science:** Deep Learning (ANN), Natural Language Processing (NLP), Sentiment Analysis, Data Wrangling, Data Mining, Sales Forecasting, Exploratory Data Analysis (EDA).
*   **Cloud & Tools:** Azure Machine Learning Studio, AWS (ECS), Docker, Git, Bitbucket, Jupyter Notebook, Google Collab.
*   **Databases:** MySQL, MongoDB, Microsoft SQL Server.

### **PROFESSIONAL EXPERIENCE**

**Graymatrix Solutions Pvt. Ltd.** | *System Analyst* | Sep 2021 – Present
*   **Lead AI Architect:** Consult on and manage the development of healthcare, mental health, and financial assistant chatbots, optimizing conversation flows for improved user retention.
*   **NLP Research:** Conducted advanced research on intent detection and Named Entity Recognition (NER) to increase chatbot response accuracy by refining linguistic models.
*   **Production Deployment:** Developed and deployed AI solutions for sales forecasting, sentiment analysis, and language detection using Azure Machine Learning Studio.
*   **QA & Training:** Led User Acceptance Testing (UAT) and conducted on-site client training to ensure seamless integration and adoption of AI tools.

**Passive Referral** | *Machine Learning Engineer* | Mar 2020 – Aug 2021
*   **End-to-End Bot Development:** Engineered real-time conversational bots from scratch, handling the full lifecycle from requirement gathering to testing and AWS deployment.
*   **Model Optimization:** Developed and trained machine learning models for context recognition using TensorFlow, improving the relevance of voice and text-based interactions.
*   **Data Engineering:** Managed data labeling pipelines and iterative feature engineering to improve model performance over time.

**Henry Harvin Education** | *Machine Learning Intern* | Jun 2019 – Nov 2019
*   **Team Leadership:** Mentored a team of interns through the full ML development cycle, from data ingestion to model deployment.
*   **Text Classification:** Built domain-specific text classifiers and developed a news content-based clustering system using Keras and Decision Trees.

### **KEY PROJECTS**

**Conversational HR Bot (RASA, MongoDB, Docker)**
*   Developed an automated pre-screening bot to shortlist candidates, integrating sentiment analysis to evaluate candidate engagement.
*   Engineered a credential validation module and centralized data tracking using MySQL and MongoDB.

**Resume Parser (NLTK, Tesseract OCR, AWS)**
*   Designed an OCR-based parser to extract keywords from candidate resumes, significantly reducing manual screening time for HR departments.
*   Architecture included deployment via Docker on AWS ECS.

### **CERTIFICATIONS**
*   **TensorFlow for AI, Machine Learning, and Deep Learning** – DeepLearning.AI (Coursera)
*   **A Crash Course in Data Science** – Johns Hopkins University (Coursera)
*   **AI For Everyone** – DeepLearning.AI (Coursera)

---

# ANALYSIS & FEEDBACK

### 1. Key Strengths and Skills
*   **Specialization in Conversational AI:** The resume highlights a clear niche (Chatbots, RASA, NLP), which is highly valuable in the current market.
*   **Full-Stack ML Capability:** Demonstrates experience from data wrangling and model training to deployment (Docker, AWS, Azure).
*   **Strong Toolset:** Proficiency in industry-standard libraries like TensorFlow, Keras, and NLTK is clearly visible.
*   **Leadership:** Mentions of "Managing development processes" and "Leading teams" suggest seniority beyond just coding.

### 2. Areas for Improvement
*   **Quantifiable Achievements:** The original resume lacks metrics. *Suggestion:* Instead of "Improving existing flows," use "Improved conversation accuracy by 15% through intent refinement."
*   **Typos and Formatting:** The original text had several "encoding" errors (e.g., "de ned" instead of "defined," "Arti cial" instead of "Artificial"). These must be fixed to look professional.
*   **Redundancy:** The project section repeated the title "Machine Learning Engineer" four times. This has been streamlined in the rewrite.
*   **Summary Statement:** The original summary was passive ("seeks opportunities"). It should be a "Value Proposition" stating what you bring to the company.

### 3. ATS (Applicant Tracking System) Analysis
*   **Keyword Optimization:** The resume is rich in high-value keywords (NLP, RASA, TensorFlow, Azure, Docker). This will help it rank well for ML roles.
*   **Formatting:** 
    *   **The Good:** The structure is logical and uses standard headings.
    *   **The Bad:** Avoid multi-column layouts or complex tables, as some older ATS scanners read left-to-right across columns, scrambling the text.
    *   **Suggestion:** Use a clean, single-column layout (as provided in the rewrite). Ensure the font is a standard web-safe font like Arial, Calibri, or Roboto.
*   **File Type:** Always save and upload as a PDF unless a Word Doc is specifically requested, but ensure the PDF is "searchable" (not a flat image).

### 4. Grammar and Action Verbs
*   **Action Verbs:** I replaced passive phrases like "I was responsible for" with strong action verbs like **Engineered**, **Architected**, **Optimized**, and **Mentored**. This makes the candidate appear more proactive and authoritative.
------------------------------------------------------------


Future Enhancements

Web Interface with Streamlit
Advanced Analytics
Job Matching Features
Multi-Format Support
Batch Processing
Output Management
Multi-Language Support
Career Development Tools
Enterprise Features
Advanced AI Features
Multiple resume format generation
