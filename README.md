# Daily-AI-Newsletter

## Overview
This n8n workflow automates the creation and distribution of a daily newsletter focused on Artificial Intelligence, Machine Learning, and related topics. It fetches the latest news, filters for relevant articles, summarizes them using an AI model, and then sends the compiled newsletter to a specified email address.

## How It Works
The workflow is composed of the following steps:
1.Scheduled Trigger: The workflow is set to run automatically at a predefined time each day.
2.Fetch News Articles: It makes an HTTP request to the NewsAPI to get the latest articles related to "artificial intelligence," "machine learning," or "AI."  
3.Filter and Process:The retrieved articles are then filtered to remove any irrelevant or incomplete entries. The top 5 articles are selected for the newsletter.  
4.Summarize with AI: Each selected article is passed to an OpenAI model, which generates a concise and engaging summary.  
5.Compile Newsletter:The summaries are compiled into a single newsletter format, complete with a title, introduction, and conclusion.  
6.Send Email:The final newsletter is sent as an email to the designated recipient using Gmail.

## Setup
To use this workflow, you will need to configure the following:
* NewsAPI Key:An API key from [NewsAPI](https://newsapi.org/) is required to fetch the news articles.  
* penAI API Key:You'll need credentials for an OpenAI account to use the summarization model.  
* Gmail Credentials:The workflow uses OAuth2 to send emails via Gmail, so you will need to authorize access to a Gmail account.  
* Recipient Email:You will need to specify the email address where the newsletter should be sent.

## Customization
You can easily customize this workflow by:
* Changing the Schedule: Adjust the trigger to run at a different time or frequency.  
* Modifying Search Terms:Update the query in the HTTP Request node to fetch news on different topics.  
* Adjusting the Summarization Prompt:Modify the prompt in the "Daily AI Newsletter" node to change the tone or style of the summaries.  
* Altering the Newsletter Format: Edit the "Code1" node to change the layout and content of the newsletter.
