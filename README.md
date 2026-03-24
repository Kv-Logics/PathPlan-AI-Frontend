PathPlan AI: Agentic Career Decision Engine
===========================================

PathPlan AI is a sophisticated multi-agent system designed to move beyond static career roadmaps. By simulating a "debate" between specialized AI agents, it analyzes a user's current capabilities against real-world market readiness to generate adaptive, ethically-grounded career paths.

🚀 Core Features
----------------

*   **Explainable Agent Reasoning**: Every career decision and roadmap milestone is the result of a traceable debate between agents, ensuring you see the "why" behind every suggestion.
    
*   **Multi-Agent Orchestration**: Utilizes a specialized team of agents, including a **Capability Agent** for profile scoring and a **Planner Agent** for roadmap generation.
    
*   **Professional Presence Analysis**: Integrated agents fetch and analyze GitHub and LinkedIn data to provide a holistic view of your professional standing.
    
*   **Ethical Realism Engine**: Automatically detects and corrects unrealistic career timelines or "hype-based" goals.
    
*   **Adaptive Roadmaps**: Generates dynamic learning paths that evolve based on market trends and personal readiness.
    

🛠️ Tech Stack
--------------

### Frontend

*   **Framework**: Next.js 16 (App Router)
    
*   **Styling**: Tailwind CSS 4
    
*   **Language**: TypeScript
    
*   **State Management**: React 19
    

### Backend

*   **Framework**: FastAPI (Python)
    
*   **AI Engine**: LangChain / Groq (LLM Orchestration)
    
*   **PDF Processing**: PyMuPDF / LangChain Community
    
*   **Environment**: Render (Production Deployment)
    

🧠 How It Works: The Agentic Workflow
-------------------------------------

PathPlan AI operates through a structured pipeline where specialized agents collaborate to refine your career strategy:

1.  **Ingestion & Parsing**: The ResumeParserAgent extracts structured signals from uploaded PDF resumes.
    
2.  **Capability Scoring**: The CapabilityAgent evaluates your skills against the target role, providing readiness scores and identifying gaps.
    
3.  **Presence Insight**: The ProfessionalPresenceAgent (supported by GitHub and LinkedIn fetchers) reviews your online footprint to gauge market visibility.
    
4.  **Strategic Debate**: An Orchestrator facilitates a "debate" between the **Planner Agent** and the **Learning Agent** to determine the most realistic path forward.
    
5.  **Roadmap Generation**: The final RoutePlannerAgent produces a chronological, month-by-month execution plan.
    

💻 Getting Started
------------------

### Prerequisites

*   Node.js 18+
    
*   Python 3.10+
    
*   API Keys for LLM providers (e.g., Groq)
    

### Installation

**1\. Backend Setup**

Bash

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   cd PathPlanAI-backend  python -m venv venv  source venv/bin/activate  # Windows: venv\Scripts\activate  pip install -r requirements.txt  uvicorn app.main:app --reload   `

**2\. Frontend Setup**

Bash

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   cd pathplan-ai-frontend  npm install  npm run dev   `

📡 API Architecture
-------------------

The frontend communicates with a centralized FastAPI backend hosted on Render. Key endpoints include:

*   POST /upload-resume: Processes PDF files and returns capability signals.
    
*   POST /planner/: Initiates the multi-agent debate to generate a roadmap.
    
*   POST /professional-insight: Triggers GitHub and LinkedIn analysis.
    
*   POST /opportunities: Matches user capabilities with market trends.
    

🛡️ Design Principles
---------------------

*   **Deterministic Logic**: While powered by LLMs, agent behavior is guided by strict system prompts to ensure professional accuracy.
    
*   **Rejection-Aware**: The system models "silence" and "rejection" as feedback loops to refine your career strategy.
    
*   **User-Centric**: Designed for students and professionals navigating high-stakes career transitions.
