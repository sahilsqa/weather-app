# Notion Setup Guide for YouTube Channel Project

## Step 1: Create Notion Integration
1. Go to https://notion.so/my-integrations
2. Click "New integration"
3. Name it "YouTube Channel Manager"
4. Select your workspace
5. Copy the API key (starts with `secret_` or `ntn_`)

## Step 2: Save API Key
Run this command in terminal:
```bash
mkdir -p ~/.config/notion
echo "YOUR_API_KEY_HERE" > ~/.config/notion/api_key
```

## Step 3: Create Workspace
1. In Notion, create a new page called "YouTube Channel - Tech in Action"
2. Click "..." (three dots) → "Connect to" → "YouTube Channel Manager"
3. Share this page with the integration

## Step 4: Get Page ID
1. Open your "YouTube Channel" page in Notion
2. Copy the URL: `https://www.notion.so/Workspace-Name-PAGE_ID_HERE`
3. Save the PAGE_ID (32-character string)

Once done, I'll create the full project structure with:
- 📁 Content Calendar (database)
- 📁 Video Production Pipeline (Kanban board)
- 📁 Resources & Research
- 📁 Analytics & Growth Tracking

Ready to proceed?
