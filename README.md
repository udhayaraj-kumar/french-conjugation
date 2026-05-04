# French Verb Master

GitHub-ready project with:
- `index.html` — French Verb Master frontend
- `api/generate-quiz.js` — Vercel serverless AI quiz backend
- `package.json` — backend dependencies

## Important
Do not put your OpenAI API key in `index.html`. Keep it in Vercel Environment Variables.

## Deploy option A: Vercel recommended
1. Push this whole folder to GitHub.
2. Import the GitHub repo into Vercel.
3. In Vercel → Project Settings → Environment Variables, add:
   - `OPENAI_API_KEY` = your OpenAI API key
   - `OPENAI_MODEL` = `gpt-5.2` or another supported model
   - `ALLOWED_ORIGIN` = your deployed site URL, or `*` while testing
4. Deploy.
5. Open your Vercel site. The frontend and backend will be in one deployment.

## Deploy option B: GitHub Pages + Vercel backend
1. Put `index.html` in your GitHub Pages repo.
2. Put `api/generate-quiz.js` and `package.json` in a separate Vercel repo.
3. Add `OPENAI_API_KEY` in Vercel environment variables.
4. In the app Quiz section, paste the backend URL, e.g. `https://your-project.vercel.app`.

## Local testing
```bash
npm install
npx vercel dev
```
