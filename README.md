# NexusForge Framework README

## Overview

NexusForge is a sophisticated AI development framework designed to streamline the software development lifecycle using multi-agent orchestration and Retrieval-Augmented Generation (RAG). It leverages specialized agents, contextual retrieval, and advanced LLM capabilities to enhance productivity, consistency, and collaboration across all phases of project development.

---

## Features

### Core Architecture
1. **Multi-Agent Orchestration Layer**  
   NexusForge employs the CrewAI framework to coordinate specialized agents:
   - **Project Lead Agent**: Oversees workflow and decision-making.
   - **Business Analyst Agent**: Converts business requirements into actionable user stories.
   - **Designer Agent**: Creates architectural plans, UI/UX designs, and system documentation.
   - **Developer Agent**: Implements code based on design specifications.
   - **Tester Agent**: Designs test plans, executes tests, and ensures quality assurance.

2. **Retrieval-Augmented Generation (RAG)**  
   RAG enhances agent capabilities by retrieving relevant context for tasks:
   - Document ingestion with PDF parsing and text chunking.
   - Semantic search using vector databases for artifact retrieval.
   - Augmented generation with context-enriched prompts.

---

### Technical Highlights
- **Frontend**: Built with Streamlit for an intuitive user interface.
- **Backend**:
  - Python-based core logic.
  - CrewAI for agent orchestration.
  - LangChain for LLM integration.
  - LiteLLM for model abstraction.
- **AI/LLM**:
  - Powered by Gemini 1.5 Flash for contextual generation.
  - ChatLiteLLM wrapper for seamless communication.
- **Data Management**:
  - Custom DatabaseManager for artifact storage and retrieval.
  - Vector database indexing for semantic search.

---

## Workflow Breakdown

### Document Ingestion
1. Upload PDF requirements or enter text directly.  
2. Documents are parsed, chunked, and embedded into the vector database.  
3. Metadata extraction enhances searchability.

### Phase-Specific RAG Processing
1. **Requirements Phase**:  
   Business Analyst retrieves project initialization documents and generates user stories.  
2. **Design Phase**:  
   Designer retrieves user stories and generates architectural plans and system designs.  
3. **Development Phase**:  
   Developer retrieves design documents to generate implementation code.  
4. **Testing Phase**:  
   Tester retrieves user stories, design documents, and implementation artifacts to create test plans.

### Knowledge Refinement
- Progressive artifact refinement cycles incorporate user feedback.  
- Cross-phase knowledge transfer ensures consistency across requirements, design, implementation, and testing.

---

## Installation

### Prerequisites
- Python >= 3.8
- Pip package manager
- Streamlit installed (`pip install streamlit`)
- LangChain library (`pip install langchain`)
- PyPDF2 library (`pip install pypdf2`)
- Vector database (e.g., Pinecone or Weaviate)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/nexusforge.git
   cd nexusforge
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   streamlit run app.py
   ```

---

## Usage

### Uploading Documents
1. Navigate to the "Document Upload" section in the UI.  
2. Upload PDF files or enter text directly into the input field.

### Managing Agents
1. Select the agent role (e.g., Business Analyst, Designer).  
2. Provide task-specific inputs (e.g., requirements or user stories).  

### Generating Artifacts
1. Agents will retrieve relevant context from the vector database.  
2. Generated artifacts are displayed in structured formats (e.g., JSON, diagrams).

---

## Advanced Features

### Context-Aware Chat System
- Project Manager queries trigger retrieval of relevant artifacts.
- Project Lead agent provides accurate responses using retrieved context.

### Progressive Knowledge Refinement
- User feedback enhances artifact quality over multiple refinement cycles.

### Cross-Phase Knowledge Transfer
- Ensures consistency across all phases of development by tracing requirements through design, implementation, and testing.

---

## Challenges Addressed

1. **Context Window Limitations**: Intelligent chunking prioritizes relevant content for large projects.
2. **Knowledge Consistency**: Centralized artifact storage ensures agents work with consistent information.
3. **Retrieval Relevance**: Metadata enrichment optimizes semantic search accuracy.
4. **User Experience Transparency**: Clear UI displays which documents influence current generation.

---

## Contributing

We welcome contributions to NexusForge! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push to your branch (`git push origin feature-name`).
5. Open a pull request describing your changes.



Happy coding! 🚀
