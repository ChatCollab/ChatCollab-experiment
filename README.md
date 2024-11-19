# ChatCollab - Experimental Data, Analysis, and Visualization

This repository contains the experimental data, analysis, and visualizations used for the ChatCollab system as described in the associated paper.

## Data Structure

The data is organized in a nested folder hierarchy under `collab_dynamics/`:

- asks_opinion/
- gives_opinion/ 
- asks_suggestion/
- gives_suggestion/
- asks_orientation/
- gives_orientation/
- shows_solidarity/
- control/

Each condition folder contains numbered runs (1,2,3) with:
- OpenAI interaction logs (.json)
- Conversation transcripts (.md)
- Metadata about the experimental run

## Output Directory

The processed data is stored in the `output/` directory:

- `parsed_dialogues.csv` - Conversation data from all experimental conditions including the run number, name of speaker, role of speaker, timestamp, and the content of the message.
- `analyzed_dialogues.csv` - Analyzed dialogue data such as human reviewed categories, LLM-labeled categories, and collapsed categories.

## Analysis Notebook

The `interaction_process_analysis.ipynb` Jupyter notebook contains:

1. Data Processing
2. LLM categorizations using OpenAI's API
3. Visualizations

The notebook processes the conversation data and generates visualizations to analyze interaction patterns between agents, serving as our collaboration analysis.

## Setup

1. Create a `.env` file with your OpenAI API key:
```
OPENAI_API_KEY='your_openai_api_key'
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Run the Jupyter notebook:
```
jupyter lab interaction_process_analysis.ipynb
```
