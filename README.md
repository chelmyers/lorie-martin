# Lorie Martin - Choral Music Website

A Jekyll-based website that uses Google Sheets as a lightweight CMS for managing music catalog content.

## Features

- Clean, professional design
- Google Sheets integration for easy content management
- Responsive layout
- Contact form integration
- GitHub Pages hosting ready

## Setup Instructions

### 1. Set Up Google Sheets

You'll find three CSV files in the project:
- `tab1-site-settings.csv`
- `tab2-music-catalog.csv`
- `tab3-testimonials.csv`

**Quick Import Method:**

1. Go to Google Sheets and create a new spreadsheet
2. Import the first CSV:
   - File > Import > Upload `tab1-site-settings.csv`
   - Import location: "Replace spreadsheet"
   - Click Import
3. Add second tab:
   - Click + at bottom to add new sheet
   - File > Import > Upload `tab2-music-catalog.csv`
   - Import location: "Insert new sheet(s)"
   - Click Import
4. Add third tab:
   - File > Import > Upload `tab3-testimonials.csv`
   - Import location: "Insert new sheet(s)"
   - Click Import
5. Rename tabs (right-click each tab):
   - Tab 1: "Site Settings"
   - Tab 2: "Music Catalog"
   - Tab 3: "Testimonials"

**Manual Setup (Alternative):**

Create three tabs with the following structure:

**Tab 1: Site Settings**
- Columns: `setting_name`, `value`
- Settings: site_title, tagline, hero_button_text, about_title, about_content, catalog_subtitle, contact_title, contact_intro, purchase_title, purchase_text, jw_pepper_catalog_link

**Tab 2: Music Catalog**
- Columns: `title`, `voicing_tag`, `duration`, `description`, `voicing_details`, `ideal_for`, `jw_pepper_link`
- One row per composition

**Tab 3: Testimonials**
- Columns: `quote`, `attribution`
- One row per testimonial

See the CSV files for example data.

### 2. Publish Your Google Sheet

1. In Google Sheets, click **File > Share > Publish to web**
2. Select **Entire Document** (important - must publish all tabs!)
3. Select **Comma-separated values (.csv)**
4. Click **Publish**
5. Copy the **Sheet ID** from your sheet's URL
   - URL format: `https://docs.google.com/spreadsheets/d/SHEET_ID_HERE/edit`
   - Copy just the `SHEET_ID_HERE` part

### 3. Configure Jekyll Site

1. Open `_config.yml`
2. Replace `YOUR_GOOGLE_SHEET_ID_HERE` with your actual Sheet ID
3. Update the `url` and `baseurl` for your GitHub Pages URL:
   ```yaml
   url: "https://your-username.github.io"
   baseurl: "/lorie-martin-site"
   ```

### 4. Set Up Contact Form (Optional)

1. Go to [Formspree.io](https://formspree.io) and create a free account
2. Create a new form and get your form endpoint
3. In `index.html`, replace `YOUR_FORM_ID` with your Formspree form ID:
   ```html
   <form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

### 5. Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g., `lorie-martin-site`)
2. Push this code to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/your-username/lorie-martin-site.git
   git push -u origin main
   ```
3. Go to your repository **Settings > Pages**
4. Under "Source", select your `main` branch
5. Click **Save**
6. Your site will be live at `https://your-username.github.io/lorie-martin-site/`

### 6. Local Development (Optional)

To test locally before deploying:

```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# Visit http://localhost:4000 in your browser
```

## Updating Content

To update the music catalog or testimonials:

1. Edit your Google Sheet
2. Changes will appear on the website automatically (may take a few minutes to refresh)
3. No need to redeploy or edit code!

## Customization

### Colors
Edit `assets/css/style.css` to change colors. Current color palette:
- Primary: `#8b9d83` (sage green)
- Secondary: `#4a5f7a` (muted navy)
- Background: `#fafaf8` (cream)

### About Section
Edit the about text in `index.html` under the `<!-- About Section -->` comment.

### Adding More Pages
Create new `.html` files in the root directory with the same front matter:
```yaml
---
layout: default
---
```

## Troubleshooting

**Catalog not loading:**
- Make sure your Google Sheet is published to the web as CSV
- Check that the Sheet ID in `_config.yml` is correct
- Open browser console (F12) to check for errors

**Contact form not working:**
- Make sure you've set up Formspree and replaced the form ID
- Check that the form action URL is correct

**Styles not loading:**
- Clear your browser cache
- Check that `assets/css/style.css` exists
- Make sure `baseurl` in `_config.yml` matches your repository name

## Support

For questions or issues, please open an issue on GitHub or contact the site administrator.

## License

© 2024 Lorie Martin. All rights reserved.
