You are an expert static-site engineer. Generate a complete, working MkDocs project that uses Material for MkDocs, with FOUR separate blog categories, each as its own blog section and URL, and deploys to GitHub Pages.

Requirements:
1) Use MkDocs + Material for MkDocs.
2) Use Material’s *built-in blog plugin* (not a third-party blog plugin).
3) Create 4 blog categories as separate blog sections:
   - /blog1/ for AI technology
   - /blog2/ for China US Relationship
   - /blog3/ for Macro Economics
   - /blog4/ for Leaders Digest
   Each blog section must:
   - have its own posts directory
   - have its own index (landing) page that shows that section’s posts
   - not mix posts between sections
4) Provide a custom Home page at / (docs/index.md) that lists the **latest blog summaries for each category**, e.g.:
   - “Latest in TAI technology” showing the most recent 3 posts from blog1
   - “Latest in China US Relationship” showing the most recent 3 posts from blog2
   - “Latest in Macro Economics” showing the most recent 3 posts from blog3
   - “Latest in Leaders Digest” showing the most recent 3 posts from blog4
   Each item on Home should show: title, date, short description/excerpt, and link.
   Use Material’s blog listing/templating features so it builds automatically from front-matter.
5) Add tags/categories support inside each blog section (front-matter: title, date, description, tags, categories).
6) Provide a clean nav:
   Home
   AI technology
   China US Relationship
   Macro Economics
   Leaders Digest
   About (placeholder page)
7) Include sample posts (at least 2 per blog section) to demonstrate the layout and the Home page aggregation.
8) Include a GitHub Actions workflow that builds and publishes to GitHub Pages on push to main.
9) Output:
   - repo folder structure
   - mkdocs.yml (fully configured)
   - docs/ markdown files including home and 4 blog indexes
   - sample posts with correct front-matter
   - .github/workflows/deploy.yml
   Make everything consistent and runnable as-is.

Implementation notes you must follow:
- Configure multiple instances of the blog plugin, each with distinct `blog_dir` and `post_dir` values pointing to different folders.
- Put blog landing pages at:
  docs/blog1/index.md
  docs/blog2/index.md
  docs/blog3/index.md
  docs/blog4/index.md
- Put posts at:
  docs/blog1/posts/*.md
  docs/blog2/posts/*.md
  docs/blog3/posts/*.md
  docs/blog4/posts/*.md
- Ensure the URLs are exactly /blog1/, /blog2/, /blog3/, /blog4/.
- Use Material theme features only; do not introduce frameworks like React/Vue.
- The Home page must auto-update based on latest posts per blog section.

After you generate the code, briefly explain:
- how to run locally (pip install, mkdocs serve)
- how to deploy (GitHub Pages settings)
- how to add new posts to a specific category.

Now generate the full project.
