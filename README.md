## AI Research Assistant via Telegram (GPT-4o mini + Gemini 2.5 Flash + SerpAPI)



## 👥 Who’s it for

This workflow is perfect for anyone who wants to receive AI-powered research summaries directly on Telegram. Ideal for people asking frequent product, tech, or decision-making questions and want up-to-date answers sourced from the web.

## 🤖 What it does

Users send a question via Telegram. An AI agent (Gemini 2.5 Flash) reformulates and understands the intent, while a second agent (GPT-4o mini) performs live research using SerpAPI. The most relevant answers, including links and images, are delivered back via Telegram.

 
## ⚙️ How it works

📲 Telegram Trigger – Starts when a user sends a message to your Telegram bot.
🧠 Gemini 2.5 Flash Agent – Understands, clarifies, or reformulates the user query.
🧠 Research AI Agent (GPT-4o mini + SerpAPI) – Searches the web and summarizes the best results.
📤 Send Telegram Message – Sends the response back to the same user.

## 📋 Requirements

- Telegram bot (via BotFather) with API token set in n8n credentials

- OpenAI account with API key and balance for GPT-4o mini

- SerpAPI account (100 free searches/month) with API key

- Gemini account with API key and balance

## 🛠️ How to set up

Create your Telegram bot using BotFather and connect it using the Telegram Trigger node
Set up Gemini credentials and add a Chat Model AI Agent node using Gemini 2.5 Flash to reformulate the user’s question
Set up OpenAI credentials and add a second ChatGPT AI Agent node using GPT-4o mini
In the GPT-4o node, enable the SerpAPI Tool and add your SerpAPI API key
Pass the reformulated question from Gemini to the GPT-4o agent for live search and summarization
Format the response (text, links, optional images)
Send the final reply to the user using the Telegram Send Message node
Ensure your n8n instance is publicly accessible
Test the workflow by sending a message to your Telegram bot ✅
