Arunodaya High School — Static Site
----------------------------------

This package contains a simple static website you can deploy to Netlify, GitHub Pages, or Vercel.

How to deploy (GitHub Pages)
1. Create a new GitHub repository (public or private).
2. Upload all files (root contains index.html and other .html pages, plus assets/).
3. In repository Settings > Pages, set branch to `main` (or `gh-pages`) and folder to `/ (root)`.
4. Save — your site will be available at https://<username>.github.io/<repo-name>/ after a few minutes.

How to deploy (Netlify)
1. Sign in to Netlify and choose "Add new site" → "Import from Git".
2. Point Netlify at the GitHub repository you created.
3. Build command: (leave empty) — Publish directory: `/` 
4. Click Deploy site.

How to deploy (Vercel)
1. Sign in to Vercel and import the Git repository.
2. Choose "Deploy" with default static settings. Publish directory: `/` .

Notes
- Replace the placeholder gallery images in assets/img with your real photos (keep filenames or update references).
- The contact details are already set to the phone and email you provided.
