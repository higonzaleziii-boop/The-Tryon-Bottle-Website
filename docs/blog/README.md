# The Tryon Bottle — Blog (how it works)

This folder is the blog. You don't need to touch code day to day. Here's the map.

## What's in here

- `index.html` — the **blog listing page** (the grid of post cards visitors see at /blog/).
- `posts/` — one HTML file per published post. The file name is the web address (the "slug").
- `POST-TEMPLATE.html` — the **master template**. Every new post is a copy of this. Don't publish this file itself.
- `blog.css` — the shared look (colors, fonts, layout). Change it once, every post updates.

## How a new post gets published (the short version)

This is the manual flow. Later roadmap steps (5 and 6) will automate most of it.

1. **Draft.** Copy `POST-TEMPLATE.html` into `posts/` and rename it to a slug, for example
   `posts/best-cold-beers-for-summer-tryon-nc.html`. Slug rules: lowercase, words-separated-by-dashes, ends in `.html`.
2. **Fill it in.** Replace every `{{TOKEN}}` (title, description, date, image, body, etc.). The template lists each token at the top.
3. **List it.** Open `index.html`, copy the existing `post-card` block, paste it at the **top** of the grid (newest first), and update its link, image, date, title, and excerpt.
4. **Tell Google.** Add one `<url>` line to `../sitemap.xml`.
5. **Publish.** Push to GitHub. Netlify rebuilds the site automatically (roadmap Step 3).

## Writing rules (from the brand brief)

- Never use em dashes. Use commas, periods, parentheses, or "..." instead.
- Warm, witty, never snobby. Write to "you." One idea per post.
- Numbers as digits. Short sentences. Specific details over generic claims.

## Good SEO habits (already built into the template)

- Every post has a unique title, meta description, and canonical link.
- Each post carries Open Graph tags (nice link previews on Facebook/Instagram) and
  structured data (helps Google show it as a rich result).
- Use local keywords naturally: "Tryon NC," "downtown Tryon," "Trade Street," "beer/wine/cigar shop near me."
- Always fill in the image `alt` text. It helps search and accessibility.
