# How to Sync This Course into GitBook

This repo is structured for GitBook. Use **Git Sync** (recommended, since you already use GitHub).

## Repo structure

- `.gitbook.yaml` - GitBook config (root, readme, summary)
- `README.md` - course landing / welcome page
- `SUMMARY.md` - sidebar navigation (GitBook reads this to build the whole course)
- `SYLLABUS.md` - full syllabus page
- `module-1-...` ... `module-8-...` - one folder per module, each with a README overview and lesson pages

Each lesson page includes: SEO meta description, a YouTube embed, learning objectives, an overview, an FAQ section, a free YouTube-comments discussion link, and internal next-lesson navigation.

## Git Sync (recommended)

1. Push these files to the root of a GitHub/GitLab repo.
2. In GitBook: open your space -> Integrations -> Git Sync (or Configure -> GitHub).
3. Authorize, then select the repo and the `main` branch.
4. Choose "GitBook <- repository" for the first import.
5. GitBook reads `.gitbook.yaml` and `SUMMARY.md` and builds the full course automatically.
6. Click Publish.

After the first sync, any push to the repo flows into GitBook automatically.

## SEO optimization (built in)

Every page is optimized for search:

- Meta descriptions via YAML frontmatter (`description:`).
- Keyword-forward H1s and a "Quick answer" paragraph on each lesson (featured-snippet bait).
- FAQ sections on every lesson (eligible for FAQ rich results).
- Internal linking: each lesson links to the next lesson, module overview, course home, and syllabus.
- Clean, descriptive URL slugs for every lesson.

One-time SEO steps in the GitBook UI after publishing:
1. Set a keyword-rich space title, e.g. "ServiceNow System Administrator Training (Free Full Course)".
2. Ensure the site is public and indexable by search engines.
3. (Premium) Connect a custom domain for stronger branding and SEO authority.

## Student comments and your replies (free)

GitBook's free plan does NOT include reader comments or discussions (reader "user feedback" is a Premium-only thumbs up/down, not a reply thread). To get comments + instructor replies for free, each lesson page links to the YouTube comment section of its embedded video:

- Students comment under the video; you reply directly on YouTube.
- Uses content you already own and costs nothing.

Optional free upgrade - Giscus: To embed comments directly on each GitBook page, add Giscus (https://giscus.app) - free, backed by your GitHub repo's Discussions. Requires enabling Discussions, installing the Giscus app, embedding its snippet, and a public repo.

## YouTube embeds

Each lesson uses GitBook native embed syntax: `{% embed url="https://www.youtube.com/watch?v=VIDEO_ID" %}`. An HTML iframe fallback is included as a comment in each lesson if your theme does not render the embed.

## Monetization later

GitBook free publishes a public site. When ready to monetize: upgrade to Premium/Ultimate for custom domain, branding, and authenticated (gated) access; or keep GitBook free as the public companion and sell cohort/access separately.

*Generated for TechTalk with Bill - ServiceNow System Administrator: Zero to Certified.*
