# Deploy AllNetworks site to Vercel

## What’s ready

- **index.html** – main page (home + order form)
- **terms.html** – Terms of Use & Privacy Policy
- **about-allnetworks-english.html** – About Us
- **vercel.json** – Vercel config
- **.vercelignore** – excludes .docx from deploy (verification server is separate)

All links use `index.html`, so the site works on Vercel.

---

## Deploy with Vercel (choose one)

### Option A: Deploy with Vercel website (no Git)

1. Go to [vercel.com](https://vercel.com) and sign in (GitHub/GitLab/Bitbucket or email).
2. Click **Add New…** → **Project**.
3. **Import Git Repository**: if the project is in GitHub/GitLab/Bitbucket, connect the repo and deploy (Vercel will detect the static site).
4. **No Git**:  
   - Install the Vercel CLI: `npm i -g vercel`  
   - In a terminal, go to the project folder:
     ```bash
     cd c:\projects\sim-website\allnetworks-site
     ```
   - Run:
     ```bash
     vercel
     ```
   - Log in if asked, then follow the prompts (defaults are fine).
   - When it asks for “Override the settings?”, you can say **N**.
5. Vercel will give you a URL like `https://sim-website-xxx.vercel.app`. Open it to see the site.

### Option B: Deploy with Vercel CLI (from folder)

1. Install Node.js if you don’t have it: [nodejs.org](https://nodejs.org).
2. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```
3. Open PowerShell or Command Prompt and go to this folder:
   ```bash
   cd c:\projects\sim-website\allnetworks-site
   ```
4. Run:
   ```bash
   vercel
   ```
5. First time: log in (browser or token).
6. Answer:
   - **Set up and deploy?** Yes  
   - **Which scope?** Your account  
   - **Link to existing project?** No  
   - **Project name?** e.g. `sim-website` or `allnetworks`  
   - **In which directory is your code?** `./` (current folder)
7. Wait for the build. You’ll get a **Production** URL – that’s your live site.

### Option C: Deploy with Git (GitHub + Vercel)

1. Create a repo on GitHub and push this folder (`allnetworks-site`). It contains only the site files.
2. On [vercel.com](https://vercel.com): **Add New…** → **Project** → **Import** your GitHub repo.
3. Leave **Root Directory** as `.` and **Build Command** empty (static site).
4. Click **Deploy**. Every push to the main branch will redeploy.

---

## After deploy

- Homepage: `https://your-project.vercel.app/` or `https://your-project.vercel.app/index.html`
- Terms: `https://your-project.vercel.app/terms.html`
- About: `https://your-project.vercel.app/about-allnetworks-english.html`

If you use a custom domain, add it in the Vercel project **Settings → Domains**.
