# Crew-AI-blog-writer-
This project automates the process of researching and writing blog content using YouTube video transcripts. The system consists of two agents, a Blog Researcher and a Blog Writer, which collaborate to extract relevant information from YouTube videos and craft a compelling blog post.

Features:

Blog Researcher: Extracts relevant video transcriptions from YouTube for a given topic.

Blog Writer: Uses the transcription to narrate and create blog content.

Sequential Task Execution: Both agents work in a coordinated, step-by-step manner.

Memory and Caching: Agents retain memory of previous interactions, enhancing their performance with consistent caching for fast retrieval.

Project Structure

tasks.py: Defines the tasks that each agent will perform.

tools.py: Provides necessary tools, such as YouTube transcript retrieval.

requirements.txt: Lists the dependencies required to run this project.

Agent Details

Blog Researcher: Expert in AI, Data Science, Machine Learning, and Generative AI video analysis. The researcher's task is to gather relevant video transcriptions.

Blog Writer: Specializes in simplifying complex topics and writing engaging blog posts. The writer uses the transcription provided by the researcher to create readable content.

Installation

To set up and run the project, follow these steps:

Clone the repository:

bash

git clone https://github.com/yourusername/ai-blog-content-creator.git

cd ai-blog-content-creator

Install dependencies: Make sure you have Python 3.8+ installed, then run:

bash

pip install -r requirements.txt

Set up environment variables: Create a .env file in the root directory with the following:

bash

OPENAI_API_KEY=your_openai_api_key

How to Use

Run the Project: The main logic can be executed by running a Python script. This will trigger both the research and writing processes based on a given topic.

Example usage:

bash

python your_script_name.py

Task Execution: The project supports sequential execution of tasks. The blog_researcher agent will first gather video data, and the blog_writer will use that data to generate the blog content.

python

result = crew.kickoff(inputs={'topic': 'AI vs ML vs DL vs Data Science'})

print(result)
