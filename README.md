
# 🌟 T20 Multi-Agent System

**T20 is your personal AI team.** It’s a multi-agent framework that helps you tackle complex tasks by bringing together specialized AI agents that work together under a central planner. Whether you want to design something, code, create music, write content, or analyze data, T20 gives you a collaborative AI system that’s organized, transparent, and easy to understand.

---

## 🧠 Philosophy

T20 is built around **Cognitive Cadence**, which is a way for AI agents to work like a human team. Each agent has a role – like planner, researcher, creator, or specialist – and they collaborate step by step to solve your problem. Think of it as your own AI dream team that’s powerful, but also clear and traceable, so you always know what’s happening.

---

## ⚙️ How T20 Works

T20 uses an **orchestrator-delegate model**, which keeps things simple:

1. **Define Your Goal** – Tell T20 what you want done, for example, “Build a landing page for my app.”
2. **Dynamic Planning** – A lead `Orchestrator` agent breaks your goal into steps.
3. **Task Delegation** – Each step is assigned to the agent best suited to handle it.
4. **Iterative Execution** – Agents complete tasks while building on each other’s work.
5. **Transparent Logging** – Every step is saved so you can trace exactly what happened.

```
[Your Goal] -> [Orchestrator] -> [Agent A] -> [Agent B] -> [Final Output]
                     |
                  [Plan.json]
```

---

## ✨ Create Your Own Agent

1. **Make a YAML file** in the `agents/` folder (e.g., `my_new_agent.yaml`).
2. **Define properties**:

```yaml
name: MyNewAgent
role: Data Analyst
goal: Analyze data and generate insights.
model: gemini-1.5-flash-latest
```

3. **Optional system prompt** in `prompts/` folder (e.g., `mynewagent_instructions.txt`)

```
You are an expert data analyst. Examine datasets, identify trends, and present actionable insights clearly.
```

Once added, your agent is ready to join the T20 workflow.

---

## 🛠 Prerequisites

* Python 3.9+
* Git

---

## 🚀 Installation

```bash
git clone <your-repo-url>
cd t20-multi-agent

python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

pip install -e .

# Add your API keys in a .env file
GOOGLE_API_KEY="YOUR_API_KEY_HERE"
```

---

## 🏃‍♂️ Usage

Run tasks with the `t20-system` command:

```bash
t20-system "Design and create a minimalist landing page for my new app."
```

Or specify an orchestrator:

```bash
t20-system -o LaMetta "Generate a 30-second lo-fi music track."
```

---

## 📝 What Happens Next

1. A session folder is created in `sessions/`.
2. The orchestrator generates a plan (`initial_plan.json`).
3. Agents complete tasks and save outputs.
4. The final result is saved in the session folder for you to review or build on.

---

## 💡 Use Cases

* **Web Development** – Build responsive websites quickly.
* **Content Creation** – Write articles, scripts, or marketing copy.
* **Music Production** – Compose and produce music tracks.
* **Research & Analysis** – Break down complex topics into actionable insights.
* **Prototyping** – Experiment and iterate on new ideas fast.

---

## 📂 Project Structure

```
t20/
├── agents/       # Agent YAML definitions
├── prompts/      # System prompts for agents
├── runtime/      # Core Python code
├── sessions/     # Output directories
├── logs/         # Debugging logs
├── requirements.txt
└── README.md
```

The `runtime/` folder contains all the core logic, from orchestrators to agent execution and logging.

---

## 🤝 Contributing

We welcome contributions! Suggest new agents, improve the workflow, or submit ideas to make T20 even smarter.

