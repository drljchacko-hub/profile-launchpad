# Profile Launchpad

A private one-page website that helps you set up online profiles on professional, academic, social, publishing and medical/radiology platforms quickly.

**What it does**

- **Master profile kit** – type your name, headline, short/medium/long bio and preferred username once. Each field has a **Copy** button.
- **Platform cards** – 40 platforms in 5 groups. Each card has **Create account** and **Edit profile** buttons, the bio character limit, the recommended photo size, a check of whether your bio fits, and a **Done** tick box.
- **Handle checklist** – checks whether your preferred username is free on each platform.
- **Progress bars** – profiles finished and usernames secured.
- **Show/hide groups** – untick groups you don't need (e.g. Medical/Radiology for non-doctors). Hidden groups are left out of the list and the progress bars.
- **Free for anyone** – share the link with colleagues. Each person's details stay on their own device.

**Your privacy**

- Everything you type or tick is saved **only in the browser on the device you are using**. Nothing is sent to GitHub, Claude or anyone else.
- Other people who visit your website see an empty page, not your details.
- Your details will **not** move to your phone or another computer automatically. Use **Download backup** and **Load backup** (in the "My data" section) to move them.
- Do not type passwords, home address, phone numbers or any patient information into the site.

**About the yellow "VERIFY" labels**

A **VERIFY** label means that link, character limit or photo size could not be confirmed when the site was built. Check it on the platform itself. Note: no link could be click-tested during the build, so it is worth clicking each one once.

---

## Part 1 – Put the website online with GitHub Pages (about 5 minutes, one time only)

You only need to do this once. After this, the site has its own web address.

**Before you start:** the website files must be on the `main` branch. If Claude made them on a separate branch, do Step 0 first.

### Step 0 – Move the files onto the main branch (only if needed)

1. Go to **https://github.com/drljchacko-hub/profile-launchpad** and sign in.
2. If you see a yellow box near the top saying a branch "had recent pushes" with a green **Compare & pull request** button, click that button. If not, click the **Pull requests** tab, then the green **New pull request** button, and in the **compare:** drop-down choose the branch starting with `claude/`.
3. Click the green **Create pull request** button (and again on the next page if asked).
4. Click the green **Merge pull request** button, then **Confirm merge**.
5. Click the **Code** tab. You should now see `index.html`, `links.json`, `llms.txt` and `README.md` in the file list.

### Step 1 – Turn on GitHub Pages

1. On the repository page, click **Settings** (the gear icon, top right of the repository menu — not your account settings).
2. In the left-hand menu, under **Code and automation**, click **Pages**.
3. Under **Build and deployment**, find **Source** and make sure it says **Deploy from a branch**.
4. Under **Branch**, click the drop-down that says **None** and choose **main**.
5. In the next drop-down, leave it as **/ (root)**.
6. Click **Save**.

### Step 2 – Find your website address

1. Wait 1–2 minutes, then refresh the **Pages** settings page.
2. A box at the top will say **"Your site is live at …"**. The address will be: **https://drljchacko-hub.github.io/profile-launchpad/**
3. Click **Visit site**. Bookmark it.

### If it does not work

- **Page says 404:** wait 5 minutes and refresh. Check that Step 1 shows **main** and **/ (root)**.
- **Private repository:** free GitHub accounts can only publish Pages from **public** repositories. Either make the repository public (Settings → General → scroll to **Danger Zone** → **Change visibility**) or upgrade GitHub. The site files contain no personal data, so making it public is safe — but only do this if you are comfortable with it.
- **Use without publishing:** you can also just download `index.html` (click it on GitHub → the **Download raw file** button, top right of the file) and double-click it on your computer. It works offline.

---

## Part 2 – Using the site

1. Open the site. Go to **Profile kit** and fill in your details. They save automatically.
2. Go to **Handles**. Click **Check** on each row. If the page that opens says "not found", "page doesn't exist" or similar, the username is probably free → set status to **Available**. If it shows someone's profile → **Taken**.
3. Go to **Platforms**. For each one you want:
   1. Click **Create account** and sign up on the platform yourself.
   2. Use the **Copy** buttons to paste your name, headline and bio.
   3. Upload your photo at the size shown on the card.
   4. Tick **Done**. In the Handles table, set that platform to **Secured**.
4. Every so often, click **Download backup** under **My data** and keep the file somewhere safe.

---

## Part 3 – Adding a new platform later (ask Claude)

You do not need to edit any code. Open Claude Code on this repository and copy-paste a message like this, changing the details in brackets:

> Add **[platform name]** to Profile Launchpad in the **[Professional/Academic, Social, Publishing, Link-in-bio/Identity, or Medical/Radiology]** category. Its sign-up page is **[address, if you know it]**. Update both links.json and the embedded copy in index.html so they match, mark anything you cannot confirm as "verify", then commit and push.

Other useful requests:

- "The **Create account** link for **[platform]** is broken — the correct one is **[address]**. Please fix it in links.json and index.html."
- "I have checked **[platform]**: the bio limit is **[number]**. Update it and remove its 'verify' label."
- "Remove **[platform]** from Profile Launchpad." (Claude should ask you to confirm before removing anything.)

After Claude pushes the change to `main` (or you merge it, as in Step 0), the live website updates by itself within a few minutes.

---

## Files in this repository

| File | What it is |
|---|---|
| `index.html` | The whole website (one file). |
| `links.json` | The platform list in a format AI tools can read. |
| `llms.txt` | A plain-language description of the site for AI tools. |
| `README.md` | These instructions. |
