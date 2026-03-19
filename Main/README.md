# Google Form Deployer

![FormDeployer](pic.png)

**An AI-Powered Google Forms Automator using CrewAI**

Form Deployer is an intelligent system that completely automates the design and instant deployment of Google Forms based on simple, natural language requirements. Built on the CrewAI framework, it utilizes a specialized team of AI agents working in concert to interpret your needs and deliver professional, ready-to-use Google Forms in seconds.

---

## ✨ Features

### 🤖 **Collaborative Agent Intelligence**
* **Requirements Analyst Agent**: Deconstructs and clarifies your form requirements from natural language inputs.
* **Form Architect Agent**: Transforms finalized specifications into optimized, user-friendly Google Forms.

### 🎯 **Seamless Form Generation**
* **Natural Language Input**: Describe your form in plain English—no technical skills required.
* **Intelligent Question Design**: Automatically selects and phrases the most relevant question types (Multiple Choice, Scale, Text, etc.).
* **Optimized Structure**: Produces clean layouts with proper sections, logic, and professional formatting.
* **Instant Deployment**: Leverages direct integration with the Google Forms API for immediate, real-time creation.

### 🌐 **Google Forms Integration**
* **Direct API Connection**: Secures an efficient, reliable connection to your Google Cloud Project.
* **Real-Time Deployment**: Forms are built, configured, and made live instantly.
* **Shareable Links**: Immediately provides public URLs and edit links for easy distribution.

---

## 🏗️ Architecture

Form Deployer follows a modular, multi-agent architecture:

```text
FormDeployer/
├── 🧠 Requirements Analyst Agent
│   ├── Interprets user input & extracts key objectives
│   └── Ensures all necessary data points are covered
└── 🛠️ Form Architect Agent
    ├── Designs form structure and flow
    ├── Provisions the Google Form via API
    └── Outputs live URLs and confirmation

-----

## 📋 Prerequisites

  * **Python**: Version 3.10 to 3.13
  * **Google Cloud Project**: With the Google Forms API enabled
  * **Service Account**: JSON credentials file with appropriate permissions
  * **GEMINI\_API\_KEY**: Required for AI agent operations

-----

## 🚀 Quick Start

### 1\. Installation

```bash
# Clone the repository
git clone [https://github.com/Anandtech09/FormDeployer.git](https://github.com/Anandtech09/FormDeployer.git)
cd FormDeployer

# Install UV package manager (if not already installed)
pip install uv

# Install dependencies
crewai install
```

### 2\. Configuration

Create a `.env` file in the root directory:

```env
MODEL=gemini/gemini-1.5-flash
GEMINI_API_KEY=your_api_key_here
SERVICEJSON=/path/to/your/google-service-account.json
```

### 3\. Run Form Deployer

```bash
crewai run
```

-----

## 💡 Usage Examples

### Event Registration Form

```python
inputs = {
    'topic': """
        Design an event registration form for a Tech Summit:
        - Attendee name and business email
        - Job title and organization
        - Choice of breakout sessions
        - Dietary restrictions
    """
}
```

### Customer Feedback

```python
inputs = {
    'topic': """
        Create a feedback form for a coffee shop:
        - Rating of the coffee (1-5)
        - Cleanliness of the store
        - Frequency of visits
        - Open suggestions
    """
}
```

-----

## 🔧 Advanced Configuration

| Variable | Description | Required |
| :--- | :--- | :--- |
| `GEMINI_API_KEY` | API key for AI agent intelligence | Yes |
| `SERVICEJSON` | Full path to Google Service Account JSON | Yes |

> **Note:** You can customize agent behavior by editing `src/googleform/config/agents.yaml` and task requirements in `src/googleform/config/tasks.yaml`.

-----

## 🤝 Contributing

We welcome contributions\!

1.  **Fork** the repository.
2.  **Create** a feature branch.
3.  **Commit** your changes.
4.  **Push** and open a Pull Request.

-----

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

-----

**Ready to deploy forms with intelligence?**
