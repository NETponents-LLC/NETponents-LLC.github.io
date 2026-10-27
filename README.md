# NETponents LLC website

Hugo site (extended not required; CSS is plain). Build: `hugo --gc --minify`. Dev: `hugo server -D`.

## Structure
- `content/_index.md` – founder/about copy on the homepage (hero and pillars live in `themes/netponentsllc/layouts/_default/home.html`)
- `content/contact/_index.md` – "How we work" and contact info
- `content/blog/` – blog section (`layouts/blog/list.html` and `single.html` in the theme)
- `themes/netponentsllc/assets/css/main.css` – all styling; brand colors are CSS variables at the top

## Adding a blog post
```
hugo new blog/my-post-title.md          # single file
hugo new blog/my-post/index.md          # page bundle (keep images next to the post)
```
Uses `archetypes/blog.md`. Front matter: `title`, `date`, `draft` (set `false` to publish), `tags`, optional `summary` (shown on the index).
Reading time, date and tags render automatically. Use fenced code blocks with a language (```` ```c ````, ```` ```go ````) for highlighting. Images in a bundle: `![alt](photo.jpg)`.
