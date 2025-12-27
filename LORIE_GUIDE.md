QUICK START GUIDE FOR LORIE - MULTI-TAB VERSION
===============================================

Hi Lorie! Here's how to manage your website using a Google Sheet with THREE TABS. Much easier to organize!

## Overview

Your Google Sheet will have 3 tabs:
1. **Site Settings** - All the text on your website (titles, about section, etc.)
2. **Music Catalog** - Your compositions
3. **Testimonials** - Quotes from choir directors

## EASY SETUP: Import the CSV Files

Chelsea will give you 3 CSV files:
- `tab1-site-settings.csv`
- `tab2-music-catalog.csv`
- `tab3-testimonials.csv`

### Import Instructions:

1. Go to Google Sheets (sheets.google.com)
2. Click **File > Import**
3. Click **Upload** tab
4. Drag `tab1-site-settings.csv` into the upload area
5. **Import location**: Select "Replace spreadsheet"
6. **Separator type**: Comma
7. Click **Import data**
8. Your first tab is now set up!

9. Now add the second tab:
   - Click the **+** button at the bottom to add a new tab
   - Click **File > Import** again
   - Upload `tab2-music-catalog.csv`
   - **Import location**: Select "Insert new sheet(s)"
   - Click **Import data**

10. Add the third tab:
    - Click **File > Import** again
    - Upload `tab3-testimonials.csv`
    - **Import location**: Select "Insert new sheet(s)"
    - Click **Import data**

11. Rename your tabs:
    - Right-click the first tab (bottom left), select "Rename", type "Site Settings"
    - Right-click the second tab, select "Rename", type "Music Catalog"
    - Right-click the third tab, select "Rename", type "Testimonials"

Done! Your sheet is now set up with all three tabs.

## Understanding Each Tab

### Tab 1: Site Settings

This controls all the text on your website.

**Columns:**
- `setting_name` - What you're changing (don't edit this column!)
- `value` - The actual text that appears on your site

**To change something:**
1. Find the setting_name you want to change
2. Edit the `value` column
3. That's it!

**For the `about_content` setting:**
- This is your entire "About My Music" section
- It's all in ONE cell
- To add paragraph breaks, just press Enter twice while editing
- The website will automatically split it into separate paragraphs

### Tab 2: Music Catalog

One row = one piece of music

**Columns:**
- `title` - Name of your piece
- `voicing_tag` - Basic voicing (SATB, SSA, etc.)
- `duration` - Length like "3:45"
- `description` - 2-3 sentences about the piece
- `voicing_details` - Full details like "SATB with piano or organ"
- `ideal_for` - When to use it
- `jw_pepper_link` - Full URL to J.W. Pepper page

**To add a new piece:**
1. Add a new row at the bottom
2. Fill in all the columns
3. Done!

**To reorder pieces:**
- Just drag rows up or down
- The website will show them in this order

### Tab 3: Testimonials

One row = one quote

**Columns:**
- `quote` - The actual quote text
- `attribution` - Person's name and organization

**To add a testimonial:**
1. Add a new row
2. Paste the quote
3. Add who said it
4. Done!

**If you don't have quotes yet:**
- That's fine! Leave the example quotes or delete them
- The website will hide the testimonials section if it's empty

## Publish to Web

Once your sheet is set up:

1. Click **File** → **Share** → **Publish to web**
2. Make sure **"Entire Document"** is selected (not just one tab!)
3. Change format to **"Comma-separated values (.csv)"**
4. Click **"Publish"**
5. Click **OK**

**Important:** You must publish the ENTIRE DOCUMENT!

## Get Your Sheet ID

1. Look at the URL of your Google Sheet
2. It looks like: `https://docs.google.com/spreadsheets/d/LONG_STRING_HERE/edit`
3. Copy just the `LONG_STRING_HERE` part
4. Send this to Chelsea

## Updating Content

### To change site text:
1. Go to "Site Settings" tab
2. Find the setting you want
3. Edit the `value` column
4. Wait a few minutes, refresh your website

### To add/edit music:
1. Go to "Music Catalog" tab
2. Add a new row or edit existing cells
3. Changes appear automatically on the site

### To add testimonials:
1. Go to "Testimonials" tab
2. Add a new row with the quote
3. Done!

## Tips

- You can make the `about_content` cell taller to see all your text
- Music pieces appear in the order you have them in the sheet
- You can hide columns you don't need to see
- Always keep a backup copy of your sheet!
- Changes take 1-5 minutes to appear on the website

## Need Help?

Ask Chelsea! She can help you with:
- Importing the CSV files
- Publishing the sheet
- Finding the Sheet ID
- Any troubleshooting

Remember: It's just a spreadsheet with three tabs. No coding required!
