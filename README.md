# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

### Date:
### Register no.: 212223240037
# Aim: 
Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

## AI Tools Required:
| Category            | Tool                                |
| ------------------- | ----------------------------------- |
| AI Coding Assistant | ChatGPT (GPT-4/5) or GitHub Copilot |
| IDE                 | VS Code or Google Colab             |
| API Testing         | Postman                             |
| Data Visualization  | Pandas + Matplotlib                 |
| Documentation       | Notion / Google Docs                |
| Presentation        | Canva / PowerPoint                  |

## Stage 1: Prompting AI to Generate Python Code for Interacting with Multiple APIs

**Goal:**
To get the AI to generate a Python script that connects to, retrieves data from, and handles responses from multiple APIs.

**Example Prompt:**
```
Write a Python program that connects to two weather APIs — OpenWeatherMap and WeatherAPI — retrieves current temperature and humidity data for a given city, and prints both results in a structured format.
```
**Expected AI Response:**

- Python code using requests library.

- API integration with sample API keys.

- JSON data parsing.

- Printed comparison output.

**Sample AI-Generated Output (Simplified):**
```py
import requests

def get_openweather_data(city):
    url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid=API_KEY"
    return requests.get(url).json()

def get_weatherapi_data(city):
    url = f"http://api.weatherapi.com/v1/current.json?key=API_KEY&q={city}"
    return requests.get(url).json()

city = "Chennai"
data1 = get_openweather_data(city)
data2 = get_weatherapi_data(city)

print("OpenWeather:", data1["main"]["temp"])
print("WeatherAPI:", data2["current"]["temp_c"])
```
## Stage 2: Prompting AI to Compare Outputs from Different APIs

**Goal:**
To guide the AI in creating code that compares the outputs and highlights differences or inconsistencies.

**Example Prompt:**
```
Generate a Python function that takes two API responses containing weather data and compares their temperature and humidity values. Highlight any differences greater than 2 degrees or 5%.
```

**Expected AI Response:**

- A comparison function.

- Logic for detecting deviations.

- User-friendly print statements summarizing differences.

**Sample AI-Generated Output:**
```py
def compare_weather(data1, data2):
    temp_diff = abs(data1 - data2)
    if temp_diff > 2:
        print(f"Temperature difference detected: {temp_diff}°C")
    else:
        print("Temperature data is consistent between APIs.")
```

## Stage 3: Prompting AI to Suggest Insights or Next Steps

**Goal:**
To use AI not just for coding but also for data-driven analysis and decision-making.

**Example Prompt:**
```
Based on the compared results from two weather APIs, suggest possible reasons for discrepancies and how a developer could handle them in real-world applications.
```
**Expected AI Response:**

- Insights explaining potential causes (e.g., data refresh intervals, API precision differences).

- Recommendations for project enhancement.

**Sample AI-Generated Insights:**

> *"The discrepancy in temperature may result from different data update frequencies or measurement sources.
Developers can handle this by averaging results from both APIs or prioritizing the one with higher reliability for specific regions."*

# AI Tools Comparision
## 1. Code-Generation & Prompt-Based AI Tools
- These tools help generate, debug, and explain code from well-structured prompts.

|  Tool |  Purpose |  Key Features |  Example Use |
| --------------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| **ChatGPT (GPT-4 or GPT-5)**      | To generate Python code, explain logic, and compare API outputs.      | Natural language prompt understanding, multi-step reasoning, code debugging. | “Write Python code to fetch data from two APIs and compare outputs.” |
| **GitHub Copilot**                | AI pair-programmer that suggests code as you type.                    | Works directly inside VS Code, JetBrains, or GitHub Codespaces.              | Auto-completes function definitions and error handling.              |
| **Google Gemini (Bard Advanced)** | Alternative to ChatGPT for cross-verification and variety of outputs. | Supports code interpretation, visualization, and explanation.                | “Explain how to handle JSON data from multiple APIs in Python.”      |
| **Claude (Anthropic)**            | Great for large text/code understanding and prompt refinement.        | Handles long documents and multi-file project prompts effectively.           | “Compare API results and summarize differences in a report format.”  |

## 2. Code Execution & Testing Tools
- After AI generates the code, these tools are used to run, debug, and validate the Python scripts.

|  Tool |  Purpose |  Functionality           |
| ----------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------ |
| **Google Colab / Jupyter Notebook** | Execute and visualize AI-generated Python code. | Free cloud-based environment for Python, perfect for testing APIs. |
| **Visual Studio Code (VS Code)**    | IDE for editing and running AI-generated code.  | Integrates with GitHub Copilot and API testing extensions.         |
| **Replit / CodeSandbox**            | Online code playgrounds for quick testing.      | No installation required — ideal for class submissions or demos.   |

## 3. API Testing & Integration Tools

- These tools are crucial for verifying API connections, response formats, and comparing outputs.

|  Tool      |  Purpose|  Features |
| ------------ | ---------------------------------------------- | ----------------------------------------------------------------------- |
| **Postman**  | To test and visualize API responses.           | Helps students see JSON outputs and check API parameters before coding. |
| **RapidAPI** | To find and connect with multiple APIs easily. | Central hub for discovering, comparing, and testing APIs.               |
| **Insomnia** | Lightweight API client for REST and GraphQL.   | Great alternative to Postman with a clean interface.                    |

## 4. Insight & Visualization Tools

- These help transform API results into visual or analytical insights.

| Tool |  Purpose | Usage Example |
| --------------------------- | -------------------------------------------------------- | --------------------------------------------------------------------- |
| **Pandas (Python Library)** | Data handling and comparison of API outputs.             | “Compare average temperatures from both APIs using Pandas DataFrame.” |
| **Matplotlib / Plotly**     | Data visualization and graphing.                         | Create bar charts showing API differences visually.                   |
| **Excel / Google Sheets**   | For quick comparisons and insights after exporting data. | Paste API results into sheets for manual inspection.                  |


## 5. Prompt Refinement & Documentation Tools

- These tools help students design, refine, and document their prompts and reflections effectively.

|  Tool |  Purpose | Key Benefit |
| -------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------- |
| **Notion / Obsidian**                  | For documenting prompt versions and reflections.                | Helps track how prompts evolve and improve clarity.        |
| **Canva / PowerPoint / Google Slides** | To present the final deliverables and AI interactions visually. | Create slides showing “Prompt → Response → Reflection.”    |
| **Grammarly / QuillBot**               | To refine written reflections and prompts for clarity.          | Ensures professional, grammatically correct documentation. |


## Advanced AI Tools (For Innovation Projects)

- For exploring cutting-edge integrations:

|  Tool                         |  Advanced Use Case                                        |
| ------------------------------- | ----------------------------------------------------------- |
| **LangChain**                   | Build custom AI apps that combine multiple APIs and models. |
| **Hugging Face Transformers**   | Use open-source AI models for NLP or image processing.      |
| **AutoGPT / OpenDevin**         | Automate multi-step coding tasks with autonomous AI agents. |
| **OpenAI API (via Python SDK)** | Directly integrate GPT models into your project code.       |

# Conclusion:
## AI-Generated Responses

| Stage | Prompt                                                               | AI Response Summary                                                    |
| ----- | -------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| 1     | "Write a Python code to connect to OpenWeatherMap and WeatherAPI..." | Generated working code with explanations for requests and JSON parsing |
| 2     | "Compare outputs and highlight differences..."                       | Provided a comparison function with logical checks                     |
| 3     | "Suggest insights..."                                                | Explained data variation causes and mitigation strategies              |

## Effective Prompt Framing
|   Weak Prompt                                |  Strong Prompt                                                                                                                                               |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Write Python code to get data from an API." | "Write Python code using the requests library to fetch temperature and humidity data for a given city from the OpenWeatherMap API and display it in Celsius." |
| "Compare API results."                       | "Compare temperature values from two weather APIs and highlight differences greater than 2°C with explanations."                                              |
| "Give insights."                             | "Based on differing outputs from APIs, explain potential causes and suggest how a developer can standardize results for a weather dashboard project."         |

## Short Conclusion
> ***Initially, my prompts were vague, leading the AI to produce generic code without clear API handling. After refining my prompts to specify the libraries, data format, and comparison logic, the AI generated accurate and ready-to-run Python code. I learned that detailed context (like naming the APIs, defining expected outputs, and stating the comparison criteria) makes prompts much more effective. Next time, I’ll include expected output formats and edge cases to get even better results.***

# Result: 
The corresponding Prompt is executed successfully.
