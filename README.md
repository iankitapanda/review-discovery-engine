# Review Discovery Engine — deploy steps

Same process as Depth Dial. You already have your Anthropic API key from that setup — reuse it.

## 1. Push to GitHub
Create a new repo (e.g. `review-discovery-engine`) and upload these files so the root contains:
```
review-discovery-engine/
├── api/
│   └── analyze.js
├── public/
│   └── index.html
└── package.json
```
Watch out for the same nesting issue as last time — make sure `api` and `public` sit at the repo root, not inside an extra wrapper folder.

## 2. Deploy on Vercel
- Add New → Project → import this repo
- Add environment variable: `ANTHROPIC_API_KEY` = (your existing key)
- Deploy

## 3. Test
Open the live URL, hit "Analyze reviews" on the pre-filled sample text, confirm you get themes/frustrations/segments back.
