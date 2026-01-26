# Proper Dog Cornwall Website

Professional dog training and grooming services website for RSPCA Cornwall Branch.

## Quick Start

1. Open `index.html` in your browser to preview the site locally
2. Edit the HTML and CSS files as needed
3. Add your own images to the `images/` folder

## File Structure

```
website/
├── index.html          # Main website page
├── css/
│   └── style.css       # All styles (brand colours, layout)
├── images/
│   └── (logo files)    # Brand images
└── README.md           # This file
```

## Deploying to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to https://github.com and sign in (or create an account)
2. Click the **+** icon → **New repository**
3. Name it `properdog-website` (or similar)
4. Keep it **Public** (required for free GitHub Pages)
5. Click **Create repository**

### Step 2: Upload Your Files

**Option A: Using GitHub Web Interface**
1. On your new repo page, click **uploading an existing file**
2. Drag all files from your `website` folder
3. Click **Commit changes**

**Option B: Using Git (Command Line)**
```bash
cd "C:\Users\olija\Documents\Dog Business\Proper Dog Cornwall\website"
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/properdog-website.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Source", select **Deploy from a branch**
4. Choose **main** branch and **/ (root)** folder
5. Click **Save**
6. Wait a few minutes - your site will be live at:
   `https://YOUR-USERNAME.github.io/properdog-website/`

### Step 4: Point Your Subdomain

To use `properdog.rspcacornwall.org.uk`:

1. **In GitHub Pages settings:**
   - Under "Custom domain", enter: `properdog.rspcacornwall.org.uk`
   - Click Save

2. **In your DNS provider** (whoever manages rspcacornwall.org.uk):
   - Add a **CNAME record**:
     - Name: `properdog`
     - Value: `YOUR-USERNAME.github.io`

   Or if using apex domain, add **A records** pointing to GitHub's IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

3. Wait for DNS propagation (can take up to 48 hours, usually faster)

4. **Enable HTTPS** in GitHub Pages settings once the domain is verified

## Editing the Website

### Adding/Changing Text
Open `index.html` in any text editor (Notepad, VS Code, etc.) and find the section you want to edit.

### Changing Colours
Edit `css/style.css` - the brand colours are at the top:
```css
:root {
    --pdc-teal: #36C1A2;
    --pdc-navy: #2C3263;
    /* etc. */
}
```

### Adding Images
1. Put images in the `images/` folder
2. Reference them in HTML: `<img src="images/your-image.jpg" alt="Description">`

### Adding Pages
1. Create a new HTML file (e.g., `training.html`)
2. Copy the structure from `index.html`
3. Update the content
4. Link to it: `<a href="training.html">Training</a>`

## Contact Form

The current contact form doesn't send emails - it's just a template. Options to make it work:

1. **Formspree** (easiest): Change form action to `https://formspree.io/f/YOUR-ID`
2. **Netlify Forms**: If hosted on Netlify, add `netlify` attribute to form
3. **Google Forms**: Embed a Google Form instead

## Brand Guidelines

- Primary colour: Teal `#36C1A2`
- Secondary colour: Navy `#2C3263`
- Font: Outfit (loaded from Google Fonts)
- Logo: "Proper" (bold) + "Dog" (regular)

See the brand guidelines HTML file for complete details.

## Support

For questions about the website, contact RSPCA Cornwall Branch.
