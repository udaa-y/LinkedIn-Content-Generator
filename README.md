# LinkedIn-Content-Generator
The LinkedIn Content Generator is an n8n workflow that pulls topics from Google Sheets, searches the web with Tavily, and uses Google Gemini to generate concise, entrepreneur-focused LinkedIn posts. It writes inspiring content, updates the sheet with the post, and marks status as “Created.”

#  LinkedIn Content Generator (n8n Workflow)

This repository contains an **n8n workflow** that automates the process of generating **entrepreneur-focused LinkedIn posts** using:
- **Google Sheets** (topics + status tracking)
- **Tavily API** (web research)
- **Google Gemini API** (AI-powered content generation)

---

## Features
-  **Topic Management**: Pulls topics marked as `To do` from a Google Sheet.
-  **Automated Research**: Uses Tavily API to fetch content from the web based on the topic.
-  **AI Writing Agent**: Google Gemini + custom system prompt to write concise, inspiring LinkedIn posts for entrepreneurs.
-  **Auto Update**: Writes the generated content back to the Google Sheet and marks the status as `Created`.
-  **Reusable Workflow**: Can be extended for Twitter/X, blogs, or other platforms.

---

## Workflow Overview
1. **Manual Trigger** → Start the workflow from n8n.
2. **Google Sheets** → Fetch topics with status = `To do`.
3. **Tavily API Request** → Search for 3 recent, relevant articles.
4. **AI Agent (Gemini)** → Summarize insights into a professional LinkedIn post.
5. **Google Sheets Update** → Insert generated post into the sheet and mark as `Created`.

---

## Requirements
- **n8n** (v1.0+)
- **Google Sheets API credentials**
- **Tavily API key**
- **Google Gemini (PaLM/Gemini) API key**

---

## Usage
1. Import `LinkedIn Content Generator.json` into your **n8n instance**.
2. Configure credentials:
   - Google Sheets (OAuth2)
   - Tavily API key
   - Google Gemini API
3. Update the Google Sheet ID in the workflow to your own sheet.
4. Add topics in the sheet with status = `To do`.
5. Run the workflow → generated LinkedIn posts will be added to the sheet under `Content`.

---

