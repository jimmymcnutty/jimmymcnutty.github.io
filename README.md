# Jasjeet Bajwa's Blog

A clean, dark-themed blog built with simple HTML and CSS.

## Getting Started with GitHub Pages

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the **+** icon in the top right and select **New repository**
3. Name it: `yourusername.github.io` (replace `yourusername` with your actual GitHub username)
4. Make it **Public**
5. Click **Create repository**

### 2. Upload Your Files

You have two options:

**Option A: Using GitHub's Web Interface (Easiest for beginners)**
1. On your repository page, click **Add file** → **Upload files**
2. Drag and drop `index.html` and `post-sample.html`
3. Scroll down and click **Commit changes**

**Option B: Using Git (Better for ongoing updates)**
```bash
# In your terminal, navigate to where you want to work
cd ~/Documents

# Clone your repository
git clone https://github.com/yourusername/yourusername.github.io.git

# Go into the folder
cd yourusername.github.io

# Copy your blog files here
# Then add them to git
git add .
git commit -m "Initial blog setup"
git push
```

### 3. Enable GitHub Pages

1. Go to your repository's **Settings**
2. Click **Pages** in the left sidebar
3. Under **Source**, select **main** branch
4. Click **Save**

Your blog will be live at: `https://yourusername.github.io`

## Connecting Your Custom Domain (jasjeetbajwa.com)

### At Your Domain Registrar:

1. Log in to where you bought jasjeetbajwa.com
2. Find the DNS settings
3. Add these DNS records:

**For the apex domain (jasjeetbajwa.com):**
- Type: `A`
- Name: `@`
- Value: `185.199.108.153`

Add three more A records with these values:
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

**For the www subdomain:**
- Type: `CNAME`
- Name: `www`
- Value: `yourusername.github.io`

### In GitHub:

1. Go to **Settings** → **Pages**
2. Under **Custom domain**, enter: `jasjeetbajwa.com`
3. Click **Save**
4. Check **Enforce HTTPS** (might take a few minutes to become available)

DNS changes can take 24-48 hours to fully propagate, but often work within an hour.

## Customizing Your Blog

### Easy Changes (No HTML/CSS knowledge needed):

**To add a new blog post:**
1. Duplicate `post-sample.html`
2. Rename it (e.g., `my-first-post.html`)
3. Open it in a text editor
4. Change the title, date, and content between the `<article>` tags
5. Upload to GitHub

**To update the home page:**
- Open `index.html`
- Find the sample posts (they start with `<article>`)
- Edit the titles, dates, and text
- Add new `<article>` sections for new posts

### Color Customization:

At the top of both HTML files, you'll see this section:
```css
:root {
    --bg-primary: #3a3a3a;      /* Main background color */
    --bg-secondary: #2d2d2d;    /* Code blocks, secondary elements */
    --text-primary: #e8e8e8;    /* Main text color */
    --text-secondary: #b8b8b8;  /* Dates, metadata */
    --accent: #6b9bd1;          /* Links */
    --accent-hover: #89b3e0;    /* Link hover color */
    --border: #505050;          /* Border lines */
    --code-bg: #2d2d2d;         /* Code background */
}
```

Change these hex codes to change colors. Try [coolors.co](https://coolors.co/) to find color combinations you like.

### Learning More:

**HTML Basics:**
- [MDN HTML Tutorial](https://developer.mozilla.org/en-US/docs/Learn/HTML)
- [HTML Dog HTML Tutorial](https://htmldog.com/guides/html/)

**CSS Basics:**
- [MDN CSS Tutorial](https://developer.mozilla.org/en-US/docs/Learn/CSS)
- [CSS Tricks](https://css-tricks.com/)

**Git/GitHub:**
- [GitHub Hello World](https://guides.github.com/activities/hello-world/)
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)

## File Structure

```
yourusername.github.io/
├── index.html          (Your home page with blog post list)
├── post-sample.html    (Example of a full blog post)
├── post2.html          (Add more posts as you write them)
├── post3.html          
└── README.md           (This file)
```

## Writing Posts

Each post is a separate HTML file. Keep the same structure as `post-sample.html`:
- Same CSS in the `<style>` section for consistency
- Same header/navigation
- Your content in the `<article>` section
- Link back to home in the footer

When you publish a new post, add it to `index.html` as a new `<article>` section.

## Tips

- **Keep it simple:** Don't try to add too much at once. Start with text posts and add features gradually.
- **Write first, design later:** Focus on writing good content. The design is already clean and readable.
- **Version control is your friend:** Commit often to GitHub. You can always undo changes.
- **Test locally:** Open your HTML files in a browser before uploading to see how they look.

## Questions?

This is a deliberately simple setup so you can learn HTML/CSS basics while having a functional blog. As you learn more, you can add features like:
- Search functionality
- RSS feed
- Archive page
- About page
- Tags/categories

But start simple. Write. Learn. Iterate.
