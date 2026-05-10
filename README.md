# SalesComm.com

The new SalesComm website. Plain HTML/CSS — no build step, no framework, no npm.

## What's in here

```
salescomm-site/
├── index.html          ← the homepage
├── styles/
│   └── main.css        ← all styling lives here
├── images/             ← logos & photos go here (currently empty; logo loads from Wix CDN as a placeholder)
├── README.md           ← this file
└── .gitignore          ← tells Git to ignore Mac/editor junk
```

## How to edit a word on the site

1. Open `index.html` in any text editor (TextEdit, VS Code, even Notepad).
2. Find the word, change it, save.
3. Push to GitHub (see below). Cloudflare auto-deploys in ~30 seconds.

That's it. No commands to run.

## How to deploy (one-time setup)

This site deploys exactly like itsblend.com:

### 1. Create the GitHub repo

1. Go to https://github.com/new
2. Repository name: `salescomm-site`
3. Set it to **Private** (or Public — your call; Public is fine for a marketing site)
4. **Do not** check "Add a README" or "Add .gitignore" — we already have those
5. Click **Create repository**

### 2. Upload these files to the repo

Easiest path (no terminal):

1. On the new repo page, click **uploading an existing file**
2. Drag the contents of this `salescomm-site` folder into the browser
3. Scroll down, click **Commit changes**

### 3. Connect Cloudflare Pages

1. Go to https://dash.cloudflare.com → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. Pick the `salescomm-site` repo
3. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave blank)*
   - **Build output directory:** `/`
4. Click **Save and Deploy**
5. Once it's live, go to **Custom domains** in the project and add `salescomm.com`
6. Update DNS at your registrar to point to Cloudflare (Cloudflare will show you the exact records to add)

### 4. Going forward

Anytime you want to change the site:
- Edit a file on GitHub directly (pencil icon in the file view), or
- Drag a new copy of a file in to overwrite

Cloudflare watches the repo and redeploys automatically.

## To-do (Phase 2)

- Replace the Wix CDN logo URL with a local copy in `/images/` (so the site doesn't depend on Wix anymore)
- Add a real headshot for the "Meet Rob" section
- Build out the linked pages: For Schools, Services, Meet Rob, Video Library
- Confirm the secret-shop offer specifics (free? what does the prospect get back? timeline?)

## Contact

Rob — Rob@salescomm.com — 801-590-6020
