# 🎓 Study Buddy AI

An intelligent quiz generation application powered by LLMs that creates personalized quizzes on any topic. Built with Streamlit and deployed using modern DevOps practices.

## ✨ What It Does

Study Buddy AI helps you learn by generating custom quizzes tailored to your needs. Just pick a topic, choose your difficulty level, and get instant practice questions. It's like having a personal tutor that never runs out of questions!

**Features:**
- Generate multiple-choice questions or fill-in-the-blank exercises
- Choose from Easy, Medium, or Hard difficulty levels
- Instant feedback on your answers
- Export your results as CSV files
- Clean, intuitive interface

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **LLM Integration**: LangChain + Groq (Llama 3.1)
- **Containerization**: Docker
- **CI/CD**: Jenkins
- **Orchestration**: Kubernetes
- **GitOps**: ArgoCD

## 🚀 Quick Start

### Running Locally

1. Clone the repository:
```bash
git clone https://github.com/sanjay-suthraye/STUDY-BUDDY-AI.git
cd STUDY-BUDDY-AI
```

2. Install dependencies:
```bash
pip install -e .
```

3. Set up your environment variables:
```bash
# Create a .env file
echo "GROQ_API_KEY=your_api_key_here" > .env
```

4. Run the application:
```bash
streamlit run application.py
```

### Using Docker

```bash
docker build -t study-buddy .
docker run -p 8501:8501 -e GROQ_API_KEY=your_api_key study-buddy
```

## 📁 Project Structure

```
├── src/
│   ├── generator/       # Quiz generation logic
│   ├── llm/            # LLM client setup
│   ├── models/         # Pydantic schemas
│   ├── prompts/        # Prompt templates
│   └── utils/          # Helper functions
├── manifests/          # Kubernetes deployment files
├── application.py      # Main Streamlit app
├── Dockerfile
└── Jenkinsfile        # CI/CD pipeline
```

## 🔧 How It Works

1. **Question Generation**: Uses LLM with structured prompts to generate valid quiz questions
2. **Validation**: Pydantic models ensure questions meet quality standards
3. **User Interface**: Streamlit provides a smooth quiz-taking experience
4. **Results**: Automatic grading with detailed feedback and export options

## 📊 DevOps Pipeline

The project includes a complete CI/CD setup:
- **Jenkins** builds and pushes Docker images
- **Kubernetes** manages deployments with 2 replicas
- **ArgoCD** handles GitOps-based continuous deployment
- Automated version tagging and manifest updates

## 🎯 Use Cases

- Students preparing for exams
- Teachers creating practice materials
- Self-learners testing their knowledge
- Quick revision on any topic

## 👤 Author

**Sanjay** 

*Built with curiosity and a love for learning* 📚

## 📝 License

This project is open source and available for educational purposes.

---

*Questions? Suggestions? Feel free to open an issue or reach out!*
