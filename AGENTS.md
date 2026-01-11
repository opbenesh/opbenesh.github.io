# AGENTS.md

## Important Guidelines

- **IMPORTANT**: Whenever you discover something that you didn't know about this environment, about referenced APIs or used tools, append it to `AGENTS.md`.
- **IMPORTANT**: Please maintain the `README.md` file after any significant changes to ensure documentation stays synchronized with the content.
- **IMPORTANT**: Commit changes after completing major features or refactoring steps to ensure work is backed up and synchronized.
## Automation Workflows

### Automate Metadata & Tags
- **Prompt**: "Review `content/posts/new-post.md`. Generate a 2-sentence summary for the description field and suggest 5 relevant tags based on the content. Update the file front matter directly."

### Automate the "About" Page
- **Prompt**: "Read `README.md` from my Spotify Tracker repo and my last three blog posts. Update `content/about.md` to reflect my current focus on metal music and mobile development."

### Pre-Flight Review & Post
- **Prompt**: "Check all files in `content/posts/`. Ensure `draft` is set to `false` for completed posts, verify all internal links work, and ensure images are correctly referenced in the `/static` folder. If everything is correct, commit with the message 'Release: [Post Title]' and push to `main`."

## Project Rules
- Always use PaperMod-compatible front matter.
- Tags should be lowercase.
- Summaries should be under 160 characters for SEO.
- Run `hugo server` to validate builds before suggesting a push.

#### Discoveries
