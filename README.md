# 📚 Retail RAG AI Customer Support Bot

> Built by Neha Durgadmath

## What it does
A production-grade RAG (Retrieval Augmented Generation) customer support system that answers customer questions exclusively from real retail policy documents. The AI never makes things up — it only answers from verified documents.

## Features
- 📄 Real retail returns and warranty policy documents as knowledge base
- 🧠 Full document vectorisation using OpenAI text-embedding-3-small
- 🔍 Cosine similarity search to find most relevant policy chunks per query
- 💬 Grounded GPT-4o-mini responses from verified documents only
- ✉️ Full chat transcript emailed to customer via AWS SES
- 📊 All sessions logged to Excel automatically
- 🇦🇺 Data Sovereignty compliant — documents processed locally

## Tech Stack
- R
- OpenAI API (gpt-4o-mini + text-embedding-3-small)
- AWS SES
- paws (AWS SDK for R)
- openxlsx

## What is RAG?
Instead of ChatGPT answering from random internet knowledge, this system first searches YOUR documents and then answers from them. Like giving AI a specific textbook to read before answering questions. Critical for enterprise clients who need accurate, verified answers.

## What is Data Sovereignty?
All policy documents are processed and stored locally. Only anonymised query vectors are sent externally — directly addressing compliance requirements for Australian government and banking clients.

## Example conversations
- "Can I return food items?" → AI correctly says NO, food items excluded
- "My appliance broke after 2 years, I have a warranty" → AI correctly explains manufacturer warranty coverage
- "Can I return opened cosmetics?" → AI correctly explains hygiene seal policy
