# Open-DeepThink-Researcher

Open source deep researcher that also thinks based on `OpenAI DeepResearch. This automates online research using **DeepSeek-R1** via [Nebius AI Studio](https://dub.sh/AIStudio) and [Exa](https://exa.ai/) search APIs. It continuously generates search queries, extracts relevant content, evaluates information and produces a comprehensive research report based on all relevant information collected.

Watch demo video on [Youtube](https://youtu.be/aEOu9P4_2cU?si=SnAHPn-34C5FX4oS)

![Open-DeepThink-Researcher](https://github.com/user-attachments/assets/a0f93ac4-3da2-4648-b522-5445d23c90c4)

## Features

* **Automated Research**: Uses AI to generate search queries and evaluate results.
    
* **Iterative Search**: Runs multiple iterations to refine and improve the quality of results.
    
* **Content Extraction & Evaluation**: Identifies and extracts relevant information from search results.
    
* **Final Report Generation**: Summarizes findings into a well-structured report.
    
* **[Gradio](https://www.gradio.app/) UI**: Provides a user-friendly web interface for easy interaction.

### Potential Improvements

- User can choose any LLM models available via Nebius Studio to power DeepThink-Researcher.
- Increase the number of iterations to refine responses further.
- Extend the text/context length from 2,000 to 5,000 or even 20,000 words/characters — but this will increase processing time and API costs.
- Optimize response times for production and public use to enhance performance.
- Export whole notebook code into hosted python web app using tools like reflex.dev or streamlit.
- Add option for users to download final report. 

## Installation

To run this project, install the required dependencies:

```sh
!pip install nest_asyncio gradio aiohttp openai exa_py
```

## Configuration

Before running the researcher, set up your API keys in the notebook:

```python
NEBIUS_API_KEY = "your_nebius_api_key"  # Replace with your Nebius API key
EXA_API_KEY = "your_exa_api_key"  # Replace with your EXA API key
```

## Usage

You can run the research assistant either via a function call or using this [Google Colab](https://colab.research.google.com/drive/1MUKaQocLT4kP82u1PlPxUIcxPHD8cfwm?usp=sharing)

## Parameters

* **User Query**: The research topic or question you want to investigate.
    
* **Iteration Limit**: The maximum number of iterations the AI should perform while refining search queries.
    

## Example Queries

Try out the following example queries:

* "What are the latest advancements in quantum computing?"
    
* "How does intermittent fasting impact metabolism?"
    
* "Best practices for deploying large-scale AI models."
    
* "Comparison of cloud AI providers: AWS vs. GCP vs. Azure."
    

## Project Structure

* `async_research()`: Handles the asynchronous execution of research.
    
* `call_nebius_async()`: Calls Nebius AI for generating responses.
    
* `perform_search_async()`: Uses Exa API to fetch search results.
    
* `is_page_useful_async()`: Evaluates the relevance of a webpage.
    
* `extract_relevant_context_async()`: Extracts meaningful content from pages.
    
* `generate_final_report_async()`: Compiles all information into a final research report.
    
* `gradio_run()`: Wraps everything into a Gradio UI.
    

## Contributing

Contributions are welcome! Please feel free to open issues or submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE).

### Acknowledgments
- This researcher is a extended fork of [OpenDeepResearcher](https://github.com/mshumer/OpenDeepResearcher)
- DeepSeek Model is used via [Nebius AI Studio](https://dub.sh/AIStudio)

