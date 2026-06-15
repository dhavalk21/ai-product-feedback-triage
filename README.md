# 🚀 Automated AI Product Feedback Triage System

This project is an automated system that reads customer feedback, uses AI to understand it, and automatically sends it to the right place.

It helps product teams save hours of manual work. Instead of a human reading every support ticket or feedback form, the AI instantly finds the bugs, decides how urgent they are, and sends them directly to Notion and Slack.

## 🎯 The Problem This Solves

When customer feedback comes in from different places, it is hard to keep track of it all.

🔴 Critical bugs get lost in long spreadsheets.

⚡ Engineers get distracted by too many Slack notifications.

⏳ Product managers spend hours copy-pasting feedback from one tool to another.

This automation solves those problems by reading the feedback immediately, sorting it, and only alerting the team when there is an actual emergency.

## ⚙️ How the System Works

The system is built as a visual pipeline that connects different tools together:

1. Getting the Feedback: The system listens for new feedback coming from a manual chat window, a website contact form, or a Google Sheet.

2. AI Analysis: An AI agent reads the feedback. It extracts the customer's main pain point, decides if the sentiment is positive or negative, and categorizes the message (for example: Bug, Feature Request, or Compliment).

3. Master Logging: All analyzed feedback is saved in a central Google Sheet for long-term storage.

4. Smart Routing:

   * Urgent or High Priority Bugs: The system posts a detailed alert in a Slack channel and creates a tracking page in Notion.

   * Standard Bugs: The system quietly creates a Notion page for the backlog so engineers can fix it later. This keeps Slack quiet and prevents alert fatigue.

   * General Feedback or Feature Ideas: The system saves these in the database but does not alert engineers, keeping their focus on building.

## 📊 What the Pipeline Looks Like

<img width="779" height="295" alt="Screenshot 2026-06-15 155850" src="https://github.com/user-attachments/assets/6d84acb6-ec35-4909-ada4-b10b2c34be10" />



## 🛠️ How to Set This Up in Your Workspace

If you want to use this workflow in your own n8n account, follow these quick steps:

1. Copy the Code: Copy the contents of the sanitized_n8n_workflow.json file from this repository.

2. Import to n8n: Open your n8n workspace, create a new blank workflow, and paste the code.

3. Connect Your Accounts: Open the Google Sheets, Slack, and Notion nodes to link your own accounts.

4. Add Your Details: Replace the placeholders like "YOUR_SPREADSHEET_ID_HERE" with your actual spreadsheet and database links.

5. Go Live: Turn the workflow on.
