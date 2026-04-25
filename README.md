# Villanova Economics Society Website

Static website for the Villanova Economics Society. Built with plain HTML, CSS, and a touch of JavaScript — no build step, no frameworks. Designed to be deployed for free on GitHub Pages.

## Project Structure

```
ves-site/
├── index.html       # Homepage
├── about.html       # About the society
├── events.html      # Upcoming events
├── board.html       # Executive board
├── contact.html     # Contact form
├── css/
│   └── styles.css   # All styles
├── js/
│   └── main.js      # Mobile nav toggle
└── README.md
```

## Local Preview

Just double-click `index.html` to open it in your browser. No server needed.

## Deploying to GitHub Pages (Step-by-Step)

### 1. Create a GitHub account
If you don't have one yet, go to github.com and sign up. Use your villanova.edu email — students get free access to GitHub Pro through the GitHub Student Developer Pack.

### 2. Create a new repository
- Click the "+" icon (top right) → "New repository"
- Name it something like `villanova-econ-society` or `ves-website`
- Set it to **Public** (required for free GitHub Pages)
- Don't initialize with a README (we have our own files)
- Click "Create repository"

### 3. Upload these files
Easiest way (no command line):
- On the new repo page, click "uploading an existing file"
- Drag the entire contents of this folder (the HTML files, the css/ folder, the js/ folder, etc.) into the upload area
- Scroll down, click "Commit changes"

### 4. Enable GitHub Pages
- In the repo, click "Settings" (top of page)
- In the left sidebar, click "Pages"
- Under "Source", select **Deploy from a branch**
- Set branch to `main` and folder to `/ (root)`
- Click "Save"
- Wait 1-2 minutes. GitHub will give you a URL like:
  `https://<your-username>.github.io/<repo-name>/`

That's it — your site is live.

## Hooking Up the Contact Form

The contact form needs Formspree (a free service) to actually deliver messages to your inbox. GitHub Pages can't process form submissions on its own.

1. Go to https://formspree.io and sign up — the free plan allows 50 submissions per month, which is plenty for a club site.
2. Create a new form. Set the destination email to wherever you want messages delivered (e.g., your club email).
3. Formspree gives you an endpoint URL that looks like `https://formspree.io/f/abcd1234`.
4. In `contact.html`, find the line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with the ID from your Formspree form (the part after `/f/`).
5. Commit the change. The form is now live.

## Customization Checklist

Before showing the site to anyone, update these things:

- [ ] **Board page** — replace placeholder names, roles, and bios with your actual board members. The two-letter initials in the photo placeholder come from the HTML — change `JD`, `VP`, etc. to match each person's initials. When you have real photos, swap the `<div class="officer-photo">JD</div>` for `<img src="path/to/photo.jpg" alt="Name" class="officer-photo" />`.
- [ ] **Events page** — replace the "TBA" events with your actual upcoming events, with real dates and locations.
- [ ] **About page** — verify the stats (member count, events per year) reflect your actual club. Update if needed.
- [ ] **Footer / contact info** — replace `econsociety@villanova.edu` with your real club email throughout.
- [ ] **Social links** — update the Instagram and LinkedIn `href="#"` placeholders in the footer with real URLs (or remove them).
- [ ] **Contact form** — set up Formspree as described above.

## Want a Custom Domain?

If you want `villanovaecon.org` instead of the github.io URL:
1. Buy the domain from Namecheap, Cloudflare, or Porkbun (~$10-15/year).
2. In your repo Settings → Pages, add the custom domain.
3. Configure DNS records as GitHub instructs. Cloudflare's free DNS makes this simple.

## License & Credits

Built for the Villanova Economics Society. Fonts from Google Fonts (Playfair Display + Inter).
