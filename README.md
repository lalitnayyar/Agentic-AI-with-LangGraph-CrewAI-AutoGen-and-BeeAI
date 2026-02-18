# Agentic AI with LangGraph, CrewAI, AutoGen, and BeeAI

A comprehensive learning repository featuring interactive Jupyter notebooks that demonstrate multi-agent AI systems, tool integration, and advanced LLM orchestration techniques using CrewAI, LangChain, and LangGraph.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Quick Start](#quick-start)
- [Notebooks Overview](#notebooks-overview)
  - [CrewAI-101](#crewai-101)
  - [AI0322EN: Beginner to Intermediate](#ai0322en-beginner-to-intermediate)
  - [AI0324EN: Advanced Topics](#ai0324en-advanced-topics)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [Contributing](#contributing)

---

## 🎯 Project Overview

This repository contains a curated collection of Jupyter notebooks exploring **Agentic AI** - systems where autonomous AI agents collaborate to solve complex problems. The notebooks progress from beginner fundamentals to advanced techniques, covering:

- **Multi-Agent Orchestration**: CrewAI framework for coordinating multiple AI agents
- **Tool Calling & Function Execution**: LangChain tool integration
- **Graph-Based Workflows**: LangGraph for complex decision trees
- **Real-time Data Integration**: API integrations with web search, web scraping
- **Domain-Specific Applications**: Math assistance, content creation, meal planning, visualization

---

## 📁 Repository Structure

```
crewai/
├── README.md                                    # This file
├── .env                                         # Environment variables (API keys)
├── CrewAI-101-v1.ipynb                         # Main CrewAI introduction
│
├── AI0322EN/                                    # Beginner to Intermediate (LangChain focus)
│   ├── AI-Math-Assistant Tool Calling.ipynb    # Custom tool creation for math operations
│   ├── Build Interactive LLM Agents with Tools.ipynb  # Multi-tool agent systems
│   ├── LLM-Powered Data Science LCEL.ipynb    # LangChain Expression Language patterns
│   ├── Manual Tool-Calling Agent.ipynb         # Low-level tool invocation
│   ├── Text-to-chart Visualization Agent.ipynb # LLM-powered chart generation
│   ├── classification-dataset.csv[.1, .2]     # Sample datasets
│   └── regression-dataset.csv[.1, .2]         # Sample datasets
│
└── AI0324EN/                                    # Advanced (LangGraph & CrewAI focus)
    ├── Build LangGraph Design Patterns Orchestration Evaluation.ipynb
    ├── Create a Structured Meal Grocery Planner with CrewAI (1).ipynb
    ├── Create a Structured Meal Grocery Planner with CrewAI (2).ipynb
    └── Create a Structured Meal Grocery Planner with CrewAI.ipynb
```

---

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- Jupyter Notebook or VS Code with Jupyter extension
- API Keys:
  - OpenAI API key (for GPT-3.5/GPT-4)
  - Serper API key (for web search)
  - IBM Watsonx credentials (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/lalitnayyar/Agentic-AI-with-LangGraph-CrewAI-AutoGen-and-BeeAI.git
   cd crewai
   ```

2. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your API keys:
   # OPENAI_API_KEY=your_key_here
   # SERPER_API_KEY=your_key_here
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   # or manually:
   pip install langchain langchain-community langchain-openai crewai crewai-tools
   ```

4. **Start Jupyter**
   ```bash
   jupyter notebook
   # or use VS Code's Jupyter extension
   ```

---

## 📚 Notebooks Overview

### **CrewAI-101-v1.ipynb** ⭐ START HERE
**Level**: Beginner | **Duration**: ~45 minutes

**Objective**: Learn the fundamentals of multi-agent systems using CrewAI.

**Key Concepts**:
- Agent roles, goals, and backstories
- Task definitions and delegation
- Tool integration (SerperDevTool for web search)
- Sequential workflow orchestration
- Creating an intelligent content pipeline

**Architecture**:
```
Research Analyst → Gathers information from web
        ↓
Technology Content Strategist → Transforms into blog posts
        ↓
Social Media Strategist → Creates social snippets
```

**Functionality**:
- **Research Agent**: Uses SerperDevTool to search the web for latest breakthroughs
- **Writer Agent**: Converts research into well-structured 4-paragraph blog posts
- **Social Agent**: Summarizes content into engaging social media posts
- **Crew Orchestration**: Sequential process that chains outputs to inputs

**Topics Covered**:
- Creating agents with roles and tools
- Defining tasks with expected outputs
- Building crews with process models
- Executing multi-agent workflows
- Handling tool responses

**Exercises**:
1. Define a Social Media Strategist agent
2. Create a task for social media content generation
3. Build a complete 3-agent crew
4. Execute the crew with custom topics

**Output Example**:
```
Topic: Latest Generative AI Breakthroughs
Research Agent Output: [Latest AI news and trends]
Writer Agent Output: [4-paragraph technical blog post]
Social Agent Output: [2-3 engaging Twitter/LinkedIn posts]
```

---

### **AI0322EN/: Beginner to Intermediate (LangChain Foundation)**

#### 1. **AI-Math-Assistant Tool Calling.ipynb**
**Level**: Beginner | **Duration**: ~45 minutes

**Objective**: Build an AI math assistant that understands natural language math queries.

**Key Concepts**:
- Creating custom tools with `@tool` decorator
- Tool schemas and descriptions
- Agent initialization and tool binding
- Multi-step problem solving
- Error handling in tool execution

**Features**:
- Custom math tools: addition, subtraction, multiplication, division
- Natural language math processing
- Sequential operation handling ("add 25 and 15, then multiply by 2")
- Wikipedia tool integration for factual lookups
- Power calculation tool (exercise)

**Functionality**:
- Parse complex math queries into steps
- Execute each step with appropriate tools
- Return final results in natural language
- Handle edge cases and validation

**Topics Covered**:
- Tool creation patterns
- Tool orchestration with agents
- Agent chain-of-thought reasoning
- Built-in LangChain tools
- Custom tool implementation

**Hands-On Exercises**:
1. Create a power/exponent tool
2. Integrate with existing math tools
3. Test complex nested operations
4. Add input validation

**Example Usage**:
```python
Agent Input: "What is 50 multiplied by 3 minus 25?"
Output: "The result is 125"

Agent Input: "Add 100 and 200, divide by 6"
Output: "The result is 50"
```

---

#### 2. **Build Interactive LLM Agents with Tools.ipynb**
**Level**: Beginner to Intermediate | **Duration**: ~60 minutes

**Objective**: Design sophisticated agent systems with multiple specialized tools.

**Key Concepts**:
- Tool chains and workflows
- Agent memory and context
- Multi-tool orchestration
- Response formatting
- Agent introspection

**Features**:
- Multiple tool categories (math, web, computation)
- Tool selection logic
- Fallback mechanisms
- Response post-processing
- Interactive agent loops

**Functionality**:
- Agents evaluate queries and select appropriate tools
- Chain multiple tools for complex tasks
- Maintain conversation context
- Format outputs for different audiences
- Debug tool selection process

**Topics Covered**:
- AgentType and agent options
- Tool binding patterns
- Memory management
- Prompt engineering for agents
- Tool response interpretation

**Use Cases**:
- Question-answering systems
- Data analysis workflows
- Research assistants
- Customer service bots

---

#### 3. **LLM-Powered Data Science LCEL.ipynb**
**Level**: Intermediate | **Duration**: ~60 minutes

**Objective**: Master LangChain Expression Language (LCEL) for composable AI pipelines.

**Key Concepts**:
- LCEL syntax and operators
- Pipe operators for chaining
- Prompt templates
- Output parsing
- Streaming and async patterns

**Features**:
- Modular component design
- Type-safe pipelines
- Error handling in chains
- Performance optimization
- Parallel processing

**Functionality**:
- Build reusable chain components
- Compose complex workflows
- Parse structured outputs
- Handle streaming responses
- Parallelize operations

**Topics Covered**:
- LCEL fundamentals
- Prompt- Model-Parser pattern
- Custom components
- Running chains
- Debugging chains

**Data Science Applications**:
- ETL pipeline automation
- Data quality validation
- Feature engineering
- Statistical analysis workflows
- Report generation

---

#### 4. **Manual Tool-Calling Agent.ipynb**
**Level**: Intermediate | **Duration**: ~75 minutes

**Objective**: Implement low-level tool calling for fine-grained control.

**Key Concepts**:
- Message passing protocols
- Tool schemas (OpenAI format)
- Manual tool invocation
- Agent state management
- Decision logic implementation

**Features**:
- Explicit message construction
- Direct tool invocation
- State tracking
- Custom decision logic
- Detailed logging

**Functionality**:
- Build agents from scratch
- Implement custom tool selection logic
- Handle tool response parsing
- Manage conversation state
- Create specialized workflows

**Topics Covered**:
- OpenAI API tool calling format
- Message role types
- Tool response integration
- Loop control flow
- Termination conditions

**Advanced Patterns**:
- Custom routing logic
- Stateful agents
- Tool prioritization
- Graceful degradation

**Example Workflow**:
```
Initialize conversation → Send query → LLM selects tool →
Parse tool call → Execute tool → Integrate result →
Continue or terminate
```

---

#### 5. **Text-to-chart in Jupyter Visualization Agent.ipynb**
**Level**: Intermediate | **Duration**: ~45 minutes

**Objective**: Create an AI agent that generates charts from natural language descriptions.

**Key Concepts**:
- Code generation from text
- Matplotlib/Plotly integration
- Error recovery
- Visual validation
- Interactive refinement

**Features**:
- Natural language chart descriptions
- Automatic chart code generation
- Multiple chart types (bar, line, scatter, pie)
- Styling and customization
- Error detection and fixing

**Functionality**:
- Accept chart requirements in plain English
- Generate Python plotting code
- Execute and render visualizations
- Handle missing data
- Refine charts based on feedback

**Topics Covered**:
- Code generation prompts
- Visualization libraries
- Error handling in code execution
- Interactive refinement loops
- Output validation

**Chart Types Supported**:
- Bar charts (horizontal, vertical, grouped)
- Line plots (single, multiple series)
- Scatter plots (2D, 3D)
- Pie charts
- Histograms and distributions
- Heatmaps

**Example**:
```
Input: "Create a bar chart comparing Q1, Q2, Q3 sales by region"
Output: [Automatically generated and rendered chart]
```

---

### **AI0324EN/: Advanced Topics (LangGraph & CrewAI Patterns)**

#### 1. **Build LangGraph Design Patterns Orchestration Evaluation.ipynb**
**Level**: Advanced | **Duration**: ~90 minutes

**Objective**: Master LangGraph for complex workflow orchestration.

**Key Concepts**:
- Graph-based agent architecture
- State management in graphs
- Node and edge operations
- Conditional routing
- Cycle handling and persistence

**Features**:
- Complex decision trees
- Parallel branching
- Conditional logic
- State accumulation
- Visualization of workflows

**Functionality**:
- Define workflow as computational graph
- Implement conditional branches
- Handle loops and cycles
- Manage complex state
- Evaluate patterns and design choices

**Topics Covered**:
- StateGraph construction
- Node definitions
- Edge conditions
- State updates
- Graph execution
- Error handling in graphs

**Design Patterns Covered**:
1. **Sequential Processing**: Linear workflow
2. **Conditional Routing**: Branch based on state
3. **Parallel Processing**: Execute multiple paths
4. **Looping**: Iterate until condition met
5. **Error Recovery**: Handle failures gracefully

**Advanced Topics**:
- Human-in-the-loop workflows
- Tool and resource allocation
- Performance optimization
- Fault tolerance
- Checkpointing and recovery

**Real-World Scenarios**:
- Insurance claim processing
- Customer onboarding workflows
- Content approval pipelines
- Data validation chains

---

#### 2. **Create a Structured Meal Grocery Planner with CrewAI.ipynb** (Versions 1, 2)
**Level**: Advanced | **Duration**: ~90 minutes each

**Objective**: Build a practical multi-agent system for meal planning and grocery management.

**Key Concepts**:
- Domain-specific agent design
- Structured output parsing
- Agent collaboration patterns
- External API integration
- User preference handling

**Features**:
- Meal preference analysis
- Nutritional requirement checking
- Grocery list generation
- Budget optimization
- Recipe recommendations
- Dietary restriction handling

**Agents Involved**:
1. **Nutritionist Agent**: Analyzes dietary needs and preferences
2. **Chef Agent**: Creates meal plans with recipes
3. **Groceries Agent**: Compiles shopping lists with quantities
4. **Budget Agent**: Optimizes costs and finds alternatives

**Functionality**:
- Accept user preferences (dietary, cuisines, allergies, budget)
- Generate weekly meal plans
- Provide recipes with instructions
- Create organized shopping lists
- Calculate nutritional info
- Suggest budget-friendly alternatives

**Topics Covered**:
- Agent specialization and focus
- Structured output with Pydantic
- State passing between agents
- Tool integration (recipe APIs, nutrition databases)
- Preference learning

**Output Structure**:
```
Meal Plan:
├── Monday: [Breakfast] [Lunch] [Dinner]
├── Tuesday: [Breakfast] [Lunch] [Dinner]
└── ...

Grocery List:
├── Vegetables: [items with quantities]
├── Proteins: [items with quantities]
├── Pantry: [items with quantities]
└── ...

Nutritional Summary:
├── Total Calories: 2000/day
├── Protein: 75g/day
├── Carbs: 250g/day
└── Fat: 65g/day
```

**Use Cases**:
- Personal meal planning
- Dietary compliance assistance
- Budget meal planning
- Allergy-aware cooking
- Nutritional goal achievement

**Advanced Features** (Version 2):
- Multi-week planning
- Seasonal ingredient optimization
- Restaurant recommendation
- Meal prep instructions
- Smart shopping (aggregate at stores)

---

## 🛠️ Technologies Used

### Core Frameworks
- **CrewAI** (v1.9.3): Multi-agent orchestration
- **LangChain** (v0.3.20): LLM chains and tools
- **LangGraph**: Graph-based workflow orchestration
- **LangChain Community** (v0.3.19): Third-party integrations

### LLMs
- **OpenAI GPT-4o**: Primary language model
- **OpenAI GPT-3.5-turbo**: Lightweight alternative
- **IBM Watsonx**: Enterprise LLM option

### APIs & Tools
- **Serper API**: Real-time web search
- **Wikipedia API**: Information retrieval
- **Matplotlib/Plotly**: Data visualization
- **Pydantic**: Data validation

### Python Libraries
- `langchain` - LLM orchestration
- `langchain-community` - Tool integrations
- `langchain-openai` - OpenAI integration
- `crewai` - Multi-agent framework
- `crewai-tools` - Pre-built agent tools
- `python-dotenv` - Environment management
- `pandas` - Data manipulation
- `matplotlib` / `plotly` - Visualization

---

## ✨ Features

### 1. **Progressive Learning Path**
- Start with CrewAI-101 fundamentals
- Progress through LangChain basics
- Master advanced LangGraph patterns
- Apply to real-world scenarios

### 2. **Hands-On Exercises**
- Every notebook includes practical exercises
- Progressive difficulty levels
- Solution guidance provided
- Real datasets included

### 3. **Real-World Applications**
- Content creation pipeline
- Math assistance system
- Data visualization
- Meal planning service
- Business workflows

### 4. **Production-Ready Patterns**
- Error handling strategies
- Logging and monitoring
- Performance optimization
- Scalability considerations

### 5. **Tool Integration Examples**
- Web search integration
- Database connectivity
- API consumption
- Custom tool creation

---

## 📥 Installation & Setup

### Environment Variables

Create a `.env` file in the root directory:

```env
# OpenAI Configuration
OPENAI_API_KEY=sk-...
OPENAI_MODEL=gpt-4o

# Serper Web Search
SERPER_API_KEY=your_serper_key

# IBM Watsonx (Optional)
WATSONX_API_KEY=...
WATSONX_PROJECT_ID=...

# Other APIs
WIKIPEDIA_API_KEY=...
```

### Dependencies Installation

```bash
# Install all dependencies
pip install -r requirements.txt

# Or install individually
pip install langchain==0.3.20
pip install langchain-community==0.3.19
pip install langchain-openai==0.3.16
pip install crewai==1.9.3
pip install crewai-tools==1.9.3
pip install openai==1.107.2
pip install python-dotenv
pip install pandas matplotlib plotly
pip install jupyter jupyterlab ipywidgets
```

### Verify Installation

```python
# Run this in a Jupyter cell to verify
import langchain
import crewai
import langgraph
print(f"LangChain: {langchain.__version__}")
print(f"CrewAI: {crewai.__version__}")
print("✅ All libraries imported successfully!")
```

---

## 📖 Usage Guide

### Running Individual Notebooks

1. **Open Jupyter**
   ```bash
   jupyter notebook
   ```

2. **Start with CrewAI-101**
   - Open `CrewAI-101-v1.ipynb`
   - Read through the markdown explanations
   - Execute code cells sequentially
   - Complete the exercises

3. **Progress to AI0322EN**
   - Choose a notebook based on interest
   - Follow the learning path
   - Complete all exercises
   - Experiment with modifications

4. **Advance to AI0324EN**
   - Understand LangGraph concepts
   - Build the meal planner
   - Customize for your use case

### Common Patterns

#### Creating a Custom Tool
```python
from crewai_tools import tool

@tool
def my_calculator(expression: str) -> str:
    """Calculate math expressions"""
    return str(eval(expression))
```

#### Defining an Agent
```python
from crewai import Agent

my_agent = Agent(
    role="Data Analyst",
    goal="Analyze data and provide insights",
    backstory="Expert in data science...",
    tools=[my_calculator],
    verbose=True
)
```

#### Creating Tasks
```python
from crewai import Task

task = Task(
    description="Analyze the dataset",
    agent=my_agent,
    expected_output="Statistical summary"
)
```

#### Running a Crew
```python
from crewai import Crew, Process

crew = Crew(
    agents=[agent1, agent2],
    tasks=[task1, task2],
    process=Process.sequential,
    verbose=True
)

result = crew.kickoff(inputs={"topic": "AI"})
```

### Troubleshooting

**Issue**: `ImportError: No module named 'crewai'`
- Solution: `pip install crewai crewai-tools`

**Issue**: `OpenAI API Key Error`
- Solution: Verify key in `.env` file and ensure it's valid

**Issue**: `Serper API Rate Limit`
- Solution: Check API quota and upgrade if needed

**Issue**: Notebook cells not running
- Solution: Install jupyter: `pip install jupyter`

---

## 🎓 Learning Outcomes

After completing all notebooks, you will be able to:

### Foundational Knowledge
- ✅ Understand agent architecture and design
- ✅ Create and configure agents with specific roles
- ✅ Define tasks with clear objectives
- ✅ Integrate multiple tools into agent workflows

### LangChain Expertise
- ✅ Build agents with LangChain
- ✅ Create custom tools and chains
- ✅ Use LCEL for composable pipelines
- ✅ Implement manual tool calling

### Advanced Patterns
- ✅ Design complex workflows with LangGraph
- ✅ Implement conditional logic and branching
- ✅ Handle state management in agents
- ✅ Build production-ready applications

### Practical Applications
- ✅ Create content generation systems
- ✅ Build data analysis pipelines
- ✅ Implement visualization agents
- ✅ Design domain-specific solutions

---

## 📊 Dataset Descriptions

### Classification Dataset
- **Files**: `classification-dataset.csv`, `.1`, `.2`
- **Size**: Multiple versions for different exercises
- **Features**: Binary/multiclass classification examples
- **Usage**: Training classification models in data science notebooks

### Regression Dataset
- **Files**: `regression-dataset.csv`, `.1`, `.2`
- **Size**: Multiple versions for different exercises
- **Features**: Continuous target variable examples
- **Usage**: Training regression models in data science notebooks

---

## 🤝 Contributing

Contributions are welcome! Here's how to help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Make your changes**
4. **Commit changes** (`git commit -m 'Add amazing feature'`)
5. **Push to branch** (`git push origin feature/amazing-feature`)
6. **Open a Pull Request**

### Guidelines
- Keep notebooks well-documented
- Add comments for complex cells
- Include markdown explanations
- Test all code before submitting
- Update this README if adding new notebooks

---

## 📝 License

This project is licensed under the MIT License - see LICENSE file for details.

---

## 👨‍💼 Author

**Lalit Nayyar**
- GitHub: [@lalitnayyar](https://github.com/lalitnayyar)
- Repository: [Agentic-AI-with-LangGraph-CrewAI-AutoGen-and-BeeAI](https://github.com/lalitnayyar/Agentic-AI-with-LangGraph-CrewAI-AutoGen-and-BeeAI)

---

## 🔗 Resources & References

### Official Documentation
- [CrewAI Documentation](https://docs.crewai.com)
- [LangChain Documentation](https://python.langchain.com/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [OpenAI API Docs](https://platform.openai.com/docs)

### Learning Resources
- [LangChain University Course (Free)](https://www.langchain.com/)
- [CrewAI Course](https://www.crewai.academy/)
- [Multi-Agent Systems in AI](https://arxiv.org/)

### Tools & Services
- [Serper API](https://serper.dev) - Web Search API
- [OpenAI](https://openai.com) - Language Models
- [IBM Watsonx](https://www.ibm.com/watsonx) - Enterprise LLM

---

## ❓ FAQ

**Q: Do I need paid API keys to run these notebooks?**
A: Some notebooks use free tier APIs. Check individual services for limits.

**Q: Can I modify these notebooks for my use case?**
A: Yes! These are provided as learning resources - feel free to adapt them.

**Q: How long does it take to complete all notebooks?**
A: Approximately 15-20 hours including exercises and experimentation.

**Q: Are there any prerequisites?**
A: Basic Python knowledge is helpful but not required.

**Q: Can I use smaller models instead of GPT-4?**
A: Yes, most notebooks work with GPT-3.5-turbo. Some advanced features may require GPT-4.

---

## 📞 Support

For issues, questions, or suggestions:
- Open an [Issue](https://github.com/lalitnayyar/Agentic-AI-with-LangGraph-CrewAI-AutoGen-and-BeeAI/issues)
- Check existing discussions
- Review notebook documentation

---

## 🎉 Getting Started Checklist

- [ ] Clone the repository
- [ ] Set up API keys in `.env`
- [ ] Install dependencies
- [ ] Open `CrewAI-101-v1.ipynb`
- [ ] Run first cell to verify setup
- [ ] Complete exercises
- [ ] Progress to next notebook
- [ ] Build your own agent!

---

**Happy Learning! 🚀**

Last Updated: February 2026
Repository Version: 1.0
