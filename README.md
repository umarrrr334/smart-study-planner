Multi-Agent AI Study Assistant
A Streamlit study workspace powered by multiple AI agents. It helps learners create personalized roadmaps, discover resources, generate quizzes, ask a tutor, and query uploaded study documents with local vector search.
Features
Personalized student analysis based on topic, goal, current level, time, and learning style
AI-generated learning roadmap with downloadable Markdown output
Resource finder for curated study materials
Quiz generator with difficulty, focus area, and question count controls
AI tutor for follow-up explanations and concept support
Document Q&A for PDF and text uploads using ChromaDB
Local hash-based document embeddings, so document search does not require OpenAI embeddings
Groq and OpenAI provider support
Tech Stack
Python
Streamlit
Phidata agents
Groq / OpenAI model SDKs
LangChain document loaders and text splitters
ChromaDB vector store
DuckDuckGo/DDGS search tools
Project Structure
.
├── app.py
├── agent_handler.py
├── study_agents.py
├── rag_helper.py
├── config.py
├── prompts.yaml
├── requirements.txt
├── .env.example
├── Dockerfile
├── docker-compose.yml
└── ARCHITECTURE.md
Getting Started
1. Clone the repository
git clone https://github.com/your-username/multi-agent-ai-study-assistant.git
cd multi-agent-ai-study-assistant
2. Create a virtual environment
Windows:
python -m venv .venv
.\.venv\Scripts\activate
macOS/Linux:
python3 -m venv .venv
source .venv/bin/activate
3. Install dependencies
pip install -r requirements.txt
4. Configure API keys
Copy the example environment file:
cp .env.example .env
Windows PowerShell:
Copy-Item .env.example .env
Add at least one provider key:
GROQ_API_KEY=your_groq_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
Do not commit .env. It is intentionally ignored.
5. Run the app
streamlit run app.py
Open:
http://localhost:8501
Push to GitHub
The project is configured to ignore local-only folders and files such as .venv/, node_modules/, .env, caches, logs, uploaded documents, and ChromaDB data.
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-username/your-repo-name.git
git push -u origin main
Docker
docker compose up --build
Make sure your environment variables are available through .env or your shell.
