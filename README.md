# STEM Tutor (free version)

A website where an AI answers only physics, engineering and math questions
(in Greek or English). It uses Google's Gemini API, which has a free tier,
and can be hosted for free on Render. No credit card should be needed for either.
Free plans can change, so check each site if something looks different.

## Step 1: Get a free API key
1. Go to https://aistudio.google.com and sign in with a Google account.
2. Click "Get API key" and create a key. Copy it and keep it secret.

## Step 2: Try it on your computer (optional)
1. Install Node.js (version 18 or newer) from https://nodejs.org
2. In this folder, copy `.env.example` to a new file named `.env` and paste your key after `GEMINI_API_KEY=`
3. Open a terminal in this folder and run: `npm start`
4. Open http://localhost:3000

## Step 3: Put it online for free
1. Create a free account at https://github.com and make a new repository.
2. Upload all files from this folder to it (use "Add file" > "Upload files").
   Do NOT upload a `.env` file, your key must stay secret.
3. Create a free account at https://render.com and click New > Web Service.
4. Connect your GitHub repository and choose the Free plan.
5. Build command: `npm install`   Start command: `npm start`
6. Under Environment, add `GEMINI_API_KEY` and paste your key.
7. Click Create. After a few minutes Render gives you a public link.

## Good to know
- On Render's free plan the site goes to sleep after 15 minutes without visitors.
  The first visit after that takes about a minute to wake up.
- There is no limit per visitor in this site. Google's free Gemini plan has its own daily limits, though. If many people use the site, it may stop answering until the limit resets (an error message will appear).
- The "only physics, engineering and math" rule is enforced by the AI's instructions.
  It works well but isn't 100% unbreakable.
- Change the model with `GEMINI_MODEL` if the default isn't available on your free plan.
