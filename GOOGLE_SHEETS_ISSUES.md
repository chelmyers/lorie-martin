GOOGLE SHEETS AS CMS - POTENTIAL ISSUES & ALTERNATIVES
======================================================

## Potential Problems with Google Sheets

### 1. **CORS Issues (Cross-Origin Resource Sharing)**
- Google Sheets CSV export SHOULD work, but some browsers/networks block it
- Symptom: Console error like "CORS policy blocked the request"
- Likelihood: LOW (Google generally allows this for published sheets)

### 2. **Rate Limiting**
- Google may throttle requests if site gets lots of traffic
- Symptom: Catalog fails to load during high traffic
- Likelihood: LOW for a personal site

### 3. **Caching**
- Changes to the sheet may take 5-15 minutes to appear
- Google caches the CSV export
- Symptom: Updates don't show immediately
- Likelihood: HIGH (this is expected behavior, not a bug)

### 4. **Sheet Must Be Public**
- The published CSV is publicly accessible
- Anyone with the sheet ID could theoretically access the raw data
- Likelihood: CERTAIN (this is how it works)
- Risk: LOW (it's just public catalog data anyway)

### 5. **Google Sheets Downtime**
- If Google Sheets goes down, catalog won't load
- Likelihood: VERY LOW (Google has 99.9%+ uptime)

### 6. **JavaScript Dependency**
- Users with JavaScript disabled won't see content
- Likelihood: VERY LOW (< 1% of users disable JS)

## Testing Before Going Live

Before deploying, test locally or on GitHub Pages:

1. Publish your Google Sheet
2. Get the Sheet ID
3. Update _config.yml
4. Deploy to GitHub Pages
5. Check browser console (F12) for errors
6. Test on multiple browsers (Chrome, Firefox, Safari)

If you see CORS errors, there are workarounds (see below).

## Alternative Solutions (If Google Sheets Doesn't Work)

### Option A: GitHub as CMS (No External Dependencies)

Instead of Google Sheets, store data in YAML files in the repo:

**Pros:**
- No external dependencies
- No CORS issues
- Version controlled
- Free forever

**Cons:**
- Lorie needs to learn GitHub or you edit for her
- Not as user-friendly as a spreadsheet

### Option B: Netlify CMS

Free CMS with a nice interface:

**Pros:**
- User-friendly editing interface
- No coding needed
- Free hosting on Netlify

**Cons:**
- Slightly more complex initial setup
- Different deployment process

### Option C: Airtable

Similar to Google Sheets but designed as a database:

**Pros:**
- Better API
- More reliable than Sheets
- Nice interface

**Cons:**
- Free tier has limits
- Requires Airtable account

### Option D: Simple JSON File

You manually create/update a JSON file:

**Pros:**
- Simple, reliable
- No external dependencies

**Cons:**
- Lorie can't edit herself
- You become the bottleneck

## My Recommendation

**Try Google Sheets first.** Here's why:

1. **It usually works fine** - Most sites using this pattern have no issues
2. **Easy to test** - Deploy to GitHub Pages and test in 10 minutes
3. **If it fails, pivot** - We can switch to GitHub-based YAML files easily

**The test:**
1. Set up the Google Sheet
2. Deploy to GitHub Pages
3. Open the site in Chrome/Firefox/Safari
4. Open browser console (F12)
5. Look for errors

If you see "CORS" errors or the catalog doesn't load, let me know and I'll give you the YAML-based solution.

## Workaround for CORS Issues (If Needed)

If you encounter CORS problems, use a proxy:

```javascript
// Instead of:
const csvUrl = `https://docs.google.com/spreadsheets/d/${sheetId}/export?format=csv&gid=${gid}`;

// Use this:
const csvUrl = `https://api.allorigins.win/raw?url=${encodeURIComponent(
    `https://docs.google.com/spreadsheets/d/${sheetId}/export?format=csv&gid=${gid}`
)}`;
```

This routes the request through a CORS proxy (free service).

## Bottom Line

**Google Sheets will probably work fine.** But if it doesn't:
- We have backup plans
- It's easy to switch
- No big deal

Try it first, then troubleshoot if needed!
