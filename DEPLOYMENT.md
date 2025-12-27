DEPLOYMENT CHECKLIST
====================

Follow these steps in order to get the site live:

## ☐ 1. Set Up Google Sheet
- [ ] Create new Google Sheet called "Lorie Martin Music Catalog"
- [ ] Add column headers (see LORIE_GUIDE.md)
- [ ] Add music pieces data
- [ ] Publish sheet to web as CSV
- [ ] Copy Sheet ID from URL

## ☐ 2. Configure Site
- [ ] Open `_config.yml`
- [ ] Replace `YOUR_GOOGLE_SHEET_ID_HERE` with actual Sheet ID
- [ ] Update `url` to your GitHub username: `https://USERNAME.github.io`
- [ ] Update `baseurl` if needed (default is `/lorie-martin-site`)

## ☐ 3. Set Up Contact Form (Optional)
- [ ] Create account at formspree.io
- [ ] Create new form
- [ ] Copy form ID
- [ ] Open `index.html`
- [ ] Replace `YOUR_FORM_ID` in the form action URL

## ☐ 4. Create GitHub Repository
- [ ] Go to github.com
- [ ] Click "New Repository"
- [ ] Name it `lorie-martin-site` (or whatever you want)
- [ ] Make it public
- [ ] Don't initialize with README (we already have one)
- [ ] Click "Create Repository"

## ☐ 5. Push Code to GitHub
Run these commands in the terminal (in the lorie-martin-site folder):

```bash
git init
git add .
git commit -m "Initial commit - Lorie Martin website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/lorie-martin-site.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

## ☐ 6. Enable GitHub Pages
- [ ] Go to your repository on GitHub
- [ ] Click "Settings" tab
- [ ] Click "Pages" in the left sidebar
- [ ] Under "Source", select "main" branch
- [ ] Click "Save"
- [ ] Wait 2-5 minutes for deployment

## ☐ 7. Test the Site
- [ ] Visit `https://YOUR_USERNAME.github.io/lorie-martin-site/`
- [ ] Check that music catalog loads
- [ ] Verify all pieces are showing
- [ ] Test contact form
- [ ] Check on mobile device

## ☐ 8. Future Updates

To update the site:
- **Content changes**: Just edit the Google Sheet - changes appear automatically
- **Design changes**: Edit files locally, then push to GitHub:
  ```bash
  git add .
  git commit -m "Description of changes"
  git push
  ```

## Troubleshooting

**Catalog not showing:**
- Check that Google Sheet is published to web
- Verify Sheet ID in `_config.yml` is correct
- Check browser console for errors (F12)

**Site not loading:**
- Wait 5-10 minutes after enabling GitHub Pages
- Check GitHub Pages settings are correct
- Clear browser cache

**Contact form not working:**
- Verify Formspree form ID is correct
- Check form action URL in index.html

**Styles look broken:**
- Check that `baseurl` in `_config.yml` matches your repo name
- Clear browser cache
- Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

## Need Help?

1. Check README.md for detailed instructions
2. Check LORIE_GUIDE.md for Google Sheets help
3. Open an issue on GitHub
4. Contact Chelsea

## Quick Reference

**Google Sheet Structure:**
- Columns: title, voicing_tag, duration, description, voicing_details, ideal_for, jw_pepper_link, type, quote, attribution
- One piece per row
- Use type="quote" for testimonials

**File Locations:**
- Main content: `index.html`
- Styles: `assets/css/style.css`
- Configuration: `_config.yml`
- About text: `index.html` (around line 30-50)

**GitHub Pages URL Pattern:**
`https://USERNAME.github.io/REPO-NAME/`
