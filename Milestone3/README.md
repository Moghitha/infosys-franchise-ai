# FranchiseOps AI – Milestone 3

**Infosys Springboard Internship 7.0 – Batch 4**

**Project:** FranchiseOps AI  
**Technologies:** Python, FastAPI, SQLite, FAISS, BM25, RAG, Google Colab

---

## 1. Project Overview

FranchiseOps AI is an AI-powered franchise management platform designed to help franchise businesses monitor outlet performance, manage daily operations, analyse business data and make informed decisions.

The platform integrates six intelligent agents, an AI Copilot, a Retrieval-Augmented Generation (RAG) knowledge base, role-based access control and interactive dashboards.

Milestone 3 focuses on expanding the knowledge base, improving the AI Copilot, enhancing agent simulators and integrating the previous milestone features into the final application.

## 2. Objectives

- Build a knowledge base containing 150+ websites and PDF documents.
- Implement RAG using FAISS and BM25 for document retrieval.
- Teach the AI Copilot at least 50 questions it could not previously answer.
- Improve Copilot intents, synonyms and response accuracy.
- Enhance all six agent simulators.
- Integrate login, profile, role-based access control and Admin functionality.
- Test the complete application and document the results.

## 3. Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Backend | FastAPI |
| Database | SQLite |
| Frontend | HTML, CSS, JavaScript |
| AI Knowledge Retrieval | RAG |
| Vector Search | FAISS |
| Keyword Search | BM25 |
| Development Environment | Google Colab |
| Version Control | Git and GitHub |

## 4. Application Modules

The application consists of the following modules:

### 4.1 AI Copilot
- Answers business-related questions.
- Retrieves numerical information from the database using SQL.
- Uses RAG to answer knowledge-based questions from documents.
- Supports question variations and synonyms.
- Provides source citations for knowledge-based answers.
- Uses an appropriate fallback when information is unavailable.

### 4.2 Intelligent Agents

The application includes six agents:

1. **Inventory Agent** – Monitors stock availability, replenishment and inventory risks.
2. **Workforce Agent** – Analyses employee availability, staffing and workforce risks.
3. **P&L Agent** – Helps analyse revenue, expenses and profitability.
4. **Marketing Agent** – Evaluates campaign performance and marketing ROI.
5. **Sentiment Agent** – Analyses customer feedback and satisfaction.
6. **Audit Agent** – Monitors outlet compliance and audit findings.

### 4.3 RAG Knowledge Base

The RAG module retrieves relevant information from collected websites and PDF documents to provide context-based answers.

The knowledge base covers:

- Franchise operations and agreements
- Staffing and labour regulations
- Food safety, FSSAI and HACCP
- Customer service
- Inventory and supply chain
- Marketing and ROI
- Outlet audits
- Finance and GST

**RAG implementation:**

- Website crawling and PDF collection
- Document extraction and text processing
- Text chunking
- FAISS vector indexing
- BM25 keyword indexing
- Hybrid document retrieval
- Source-based answer generation

**System Check results (14 November 2026):**
- Knowledge base chunks indexed: 35,626
- Chunks imported from Google Drive: 35,551
- Knowledge base status: OK
- Google Drive RAG output: OK

Number of unique successfully collected source documents: [Enter verified count; requirement is 150+].

### 4.4 Copilot Teaching

The Teach Copilot module allows administrators to add questions, approved answers and keywords.

The prepared `taught_questions.csv` contains 67 question-and-answer entries.

The CSV structure includes:

- Index
- Question
- Answer
- Keywords

The questions cover franchise operations, inventory, workforce, marketing, customer service, audits, food safety, finance and RAG-related topics.

Verified number of questions successfully taught in the application: [Enter Admin → Teach Copilot counter].

### 4.5 Agent Simulators

The six agent simulators are enhanced to support operational scenario analysis.

The improvements include:

- Inventory: Demand seasonality, supplier delays and stock-out probability.
- Workforce: Employee attrition, hiring lead time and overtime costs.
- P&L: Price elasticity, wage inflation and profitability scenarios.
- Marketing: Diminishing returns, campaign fatigue and ROI ranges.
- Sentiment: Impact of complaint resolution on customer satisfaction.
- Audit: Probability of audit failure and compliance improvement.

Each simulator should display assumptions, 10th–90th percentile ranges, use a reproducible random seed, read starting values from the database and avoid modifying live data.

## 5. Authentication and Role-Based Access Control

The final application includes:

- Login and authentication
- User profile
- Role-based permissions
- Admin dashboard
- Access restrictions
- Unauthorized access responses (HTTP 403)

## 6. Project Structure

Milestone3/

- `FranchiseOpsAI_RAG_Builder_FINAL.ipynb` – RAG knowledge-base construction.
- `FranchiseOps_AI_v5.ipynb` – Final integrated application.
- `taught_questions.csv` – Prepared Copilot questions and answers.
- `README.md` – Project documentation.
- `Presentation.pptx` – Project presentation.
- `Presentation.pdf` – PDF version of the presentation.
- `screenshots/` – Project implementation and testing evidence.

*Use the actual filenames of your notebooks and presentation files.*

## 7. Execution Instructions

### Step 1: Open the RAG Builder Notebook

Open `FranchiseOpsAI_RAG_Builder_FINAL.ipynb` in Google Colab.

### Step 2: Build the Knowledge Base

Run the notebook cells to collect websites and PDFs, extract text, generate chunks and build the FAISS and BM25 indexes.

The generated files are stored in the Google Drive `FranchiseOps_AI` folder.

### Step 3: Run the Final Application

Open `FranchiseOps_AI_v5.ipynb` in Google Colab.

Enable Google Drive persistence and run the notebook cells.

### Step 4: Verify RAG Integration

Open the running application and navigate to:

**Admin → System check → Knowledge base (RAG)**

Verify the indexed chunks and Google Drive import status.

### Step 5: Test the AI Copilot

Ask knowledge-based questions and verify that answers contain relevant information and source citations.

### Step 6: Test Other Modules

Verify authentication, role-based access, the six agents, simulators and Copilot functionality.

## 8. Testing and Validation

The following tests should be performed:

- Verify that the RAG knowledge base loads successfully.
- Test at least 10 knowledge-based questions.
- Verify source citations and retrieved documents.
- Verify the taught question counter reaches 50/50.
- Test SQL-based Copilot questions.
- Test all six agent simulators.
- Verify role-based access and unauthorized 403 responses.
- Check that simulators do not modify live database values.

## 9. Screenshots and Evidence

The following screenshots are included as implementation evidence:

1. **RAG Builder**
   - `screenshots/rag_builder/source_collection.png`
   - `screenshots/rag_builder/chunk_generation.png`

2. **Admin → Teach Copilot**
   - `screenshots/copilot/taught_questions_50_50.png`

3. **Copilot Response with Source Citations**
   - `screenshots/copilot/copilot_rag_response.png`

4. **Agent Simulator Before and After Improvements**
   - `screenshots/simulators/inventory_before_after.png`
   - `screenshots/simulators/workforce_before_after.png`
   - `screenshots/simulators/pnl_before_after.png`
   - `screenshots/simulators/marketing_before_after.png`
   - `screenshots/simulators/sentiment_before_after.png`
   - `screenshots/simulators/audit_before_after.png`

5. **Admin → Copilot Insights**
   - `screenshots/copilot/copilot_insights.png`

6. **Admin → System Check and RAG Integration**
   - `screenshots/system/system_check.png`
   - `screenshots/system/google_drive_rag_status.png`

7. **User Authentication and Role-Based Access Control**
   - `screenshots/authentication/login.png`
   - `screenshots/authentication/role_access.png`
   - `screenshots/authentication/unauthorized_403.png`

## 10. Security and Repository Guidelines

- Do not upload API keys, passwords, authentication tokens or other secrets.
- Do not upload database files (`.db`).
- Clear notebook outputs containing sensitive information before committing.
- Use public websites and documents for knowledge-base collection.
- Protect user and customer information.
- Maintain appropriate role-based access restrictions.

## 11. Conclusion

FranchiseOps AI combines intelligent agents, database-driven Copilot functionality and document-based knowledge retrieval to support franchise operations.

Milestone 3 extends the platform with an expanded knowledge base, improved Copilot responses, enhanced agent simulators and integrated access management.

The project aims to provide a centralized and intelligent platform for monitoring franchise operations and supporting better business decisions.

## 12. Team Members and Contributions

The FranchiseOps AI project was developed collaboratively by a team of five members, with each member contributing to different modules and implementation activities.

| Sl. No. | Team Member Name | Contribution / Responsibilities |
|---|---|---|
| 1 | [Aditya Kumar] | [RBAC integration and login functionality] |
| 2 | [Kaushik B] | [Simulator modifications] |
| 3 | [Moghitha B] | [AI Copilot enhancement and addition of 67 questions] |
| 4 | [Mrunali Karmore] | [RAG (Retrieval-Augmented Generation) implementation] |
| 5 | [Yedururi Venkata Sai Sujitha] | [PPT Presentation] |

All team members contributed to the development, integration, testing and documentation of the FranchiseOps AI platform.
