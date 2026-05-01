# Zyra Bot - Free 24/7 Deployment Guide (Render.com)

## Step 1: GitHub Setup
1. Go to github.com and create a free account (if you don't have one)
2. Click "New Repository" (green button)
3. Name it: `zyra-bot`
4. Keep it Public or Private (your choice)
5. Click "Create Repository"
6. Upload all files from this folder: `bot.py`, `requirements.txt`, `Procfile`, `render.yaml`

## Step 2: Render.com Setup
1. Go to render.com
2. Click "Sign Up" → Sign up with GitHub
3. After login, click "New +" → "Background Worker"
4. Connect your GitHub repo (`zyra-bot`)
5. Settings:
   - Name: zyra-bot
   - Runtime: Python
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `python bot.py`
   - Plan: Free

## Step 3: Environment Variables
In Render dashboard, go to "Environment" tab and add:

| Key | Value |
|-----|-------|
| TELEGRAM_BOT_TOKEN | `8608668611:AAHQwiK0bjlCnFCLJ2IWekGH0vnvLp_t5EM` |
| OPENAI_API_KEY | Your OpenAI API key from platform.openai.com |
| ADMIN_ID | `7054505887` |

## Step 4: Deploy!
Click "Create Background Worker" — Done! Zyra will be live 24/7!

## Important Notes:
- Render free tier may sleep after 15 min of inactivity (for web services only, NOT background workers)
- Background Worker stays ON 24/7 on free tier
- If bot stops, just go to Render dashboard and click "Manual Deploy"
- Logs visible in Render dashboard

## Get OpenAI API Key:
1. Go to platform.openai.com
2. Sign up / Login
3. Go to API Keys section
4. Create new key
5. Copy and paste in Render environment variables

That's it! Zyra will run forever for FREE! 🔥
