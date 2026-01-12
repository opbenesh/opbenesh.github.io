# STYLE.md

This document defines the visual and content styling guidelines for the blog.

## Writing Style

### Tone and Voice
- **Conversational**: Write in a friendly, approachable tone as if talking to a fellow developer
- **Technical but accessible**: Balance technical accuracy with readability
- **Personal**: Include anecdotes and personal experiences where relevant
- **Authentic**: Be honest about challenges, limitations, and learning experiences
- **Enthusiastic**: Show genuine excitement about topics without being overly promotional

### Content Structure
- **TL;DR**: Start longer posts with a blockquote summary (using `> **TL;DR:**`)
- **Clear hierarchy**: Use `##` for main sections, `###` for subsections
- **Scannable**: Break up long text with headers, lists, and code blocks
- **Actionable**: Provide concrete examples, commands, and steps when applicable

### Formatting Conventions

#### Headers
- **No emojis**: Keep headers clean with plain text only
- **Sentence case**: Use sentence case for headers (not title case)
- **Descriptive**: Headers should clearly indicate section content

#### Lists
- Use bullet points (`*` or `-`) for unordered lists
- Use numbered lists for sequential steps or instructions
- Keep list items concise and parallel in structure

#### Code Blocks
- Always specify language for syntax highlighting (e.g., ````bash`, ````python`)
- Use inline code (backticks) for commands, file names, and variable names
- For terminal output with styling, use HTML `<pre>` blocks with custom styling

#### Emphasis
- **Bold** for key terms, important concepts, and emphasis
- *Italics* for subtle emphasis or introducing new terms
- Avoid excessive formatting - let content speak for itself

#### Links
- Use descriptive link text (not "click here")
- Format as `[Description](URL)`
- Include section in "Further Reading" for external resources when relevant

#### Sections and Dividers
- Use `---` (horizontal rule) to separate major content transitions
- Use `***` (triple asterisks) for lighter visual breaks
- Don't overuse dividers - headers should provide most structure

#### Images and Figures
- Use Hugo shortcodes for figures: `{{< figure src="image.jpg" caption="Description" >}}`
- Always include descriptive alt text
- Specify width when needed (e.g., `width="50%"`)
- Store images in page bundles alongside `index.md`

## Cover Image Design Principles

All blog post cover images should follow this consistent visual style:

### Technical Specifications
- **Dimensions**: 1200x300px (4:1 aspect ratio banner format)
- **Background**: Dark (#0a0a0a / nearly black)
- **Primary Color**: Neon green (#00ff88 / rgb(0, 255, 136))
- **File Format**: PNG
- **Location**: Page bundle (`content/posts/[post-name]/cover.png`)

### Design Guidelines
- **Layout**: Icon(s) on left side (starting ~80px from left edge), bold title text starting ~280px from left
- **Icons**: Simple geometric shapes representing the post topic (satellite dish for doom-coding, gopher for Hugo, etc.)
- **Typography**: Large, bold sans-serif font (~100pt), neon green color
- **Style**: Minimalist, clean, modern aesthetic with strong contrast
- **Consistency**: All covers should feel like part of the same brand family

### Front Matter Configuration
```toml
[cover]
image = "cover.png"
alt = "[Descriptive alt text]"
relative = true
```

### Creation Tips
- Use simple geometric primitives (circles, triangles, rectangles) for icons
- Keep icons outlined (stroke only) rather than filled for consistency
- Text should be concise (2-4 words max) and clearly readable
- Maintain ~8-10px stroke width for icon outlines
- Test visibility on both light and dark backgrounds (though primarily viewed on dark)

### How to Generate a Cover Photo

Use this prompt template with AI image generators (Claude, DALL-E, Midjourney, etc.):

```
Create a minimalist banner image for a blog post with these exact specifications:

DIMENSIONS: 1200 pixels wide × 300 pixels tall (4:1 ratio)

BACKGROUND: Solid dark color #0a0a0a (nearly black)

COLOR SCHEME:
- Primary: Neon green #00ff88 (rgb 0, 255, 136)
- Background: #0a0a0a (dark/nearly black)

LAYOUT:
- Left side (starting ~80px from left edge): Icon/graphic
- Right side (starting ~280px from left): Title text

ICON DESIGN:
- Simple geometric shapes representing [TOPIC - e.g., "Hugo static site generator and GitHub"]
- Style: Outlined shapes only (NOT filled), ~8-10px stroke width
- [SPECIFIC ICON DETAILS - e.g., "Hugo gopher: Circle for head with triangular ears, two dots for eyes"]
- All lines/shapes in neon green #00ff88

TYPOGRAPHY:
- Text: "[YOUR TITLE - 2-4 words max, e.g., 'Hugo + GitHub']"
- Font: Bold, clean sans-serif (like Helvetica Bold or similar)
- Size: ~100pt
- Color: Neon green #00ff88
- Position: Right side of banner, vertically centered

STYLE:
- Minimalist, flat design
- Strong contrast
- Modern tech aesthetic
- Clean geometric shapes
- Professional but approachable
- Terminal/developer vibe

NO gradients, NO shadows, NO textures - keep it flat and clean.
```

Replace the bracketed sections with your post-specific details.

## Front Matter Standards

### Required Fields
```yaml
title: "Post Title"
date: YYYY-MM-DDTHH:MM:SS+TZ
draft: false
tags: ["tag1", "tag2"]
summary: "Brief description under 160 characters for SEO"
author: "Ben Esh"
```

### Optional Fields
```yaml
ShowPostNavLinks: true  # Show previous/next post navigation
[cover]
  image: "cover.png"
  alt: "Image description"
  relative: true
```

### Metadata Rules
- **Tags**: Always lowercase, 3-6 tags per post
- **Summary**: Under 160 characters for SEO optimization
- **Title**: Clear and descriptive, avoid clickbait
- **Date**: Include timezone offset
- **Draft**: Set to `false` before publishing

## Asset Management

### Images
- **Prefer Page Bundles**: Store images alongside `index.md` in post folders
- **Alternative**: Use `/assets` folder for Hugo image processing
- **Fallback**: Use `/static` folder for raw assets
- **Naming**: Use descriptive, lowercase names with hyphens (e.g., `claude-interaction.jpg`)

### File Organization
```
content/posts/
  my-post/
    index.md
    cover.png
    screenshot-1.jpg
    diagram.svg
```

## Best Practices

### SEO and Accessibility
- Include descriptive alt text for all images
- Keep summaries under 160 characters
- Use semantic HTML when needed
- Ensure proper heading hierarchy
- Include descriptive link text

### Content Quality
- Proofread for typos and clarity
- Test all code examples
- Verify all links work
- Ensure internal references are accurate
- Run `hugo server` to preview before publishing

### Consistency
- Follow established patterns from existing posts
- Maintain the same tone and style across posts
- Use consistent terminology
- Keep formatting uniform

## Review Checklist

Before publishing a post, verify:
- [ ] No emojis in headers
- [ ] Cover image follows design principles
- [ ] Front matter is complete and correct
- [ ] Tags are lowercase
- [ ] Summary is under 160 characters
- [ ] All code blocks have language specified
- [ ] All images have alt text
- [ ] All links work
- [ ] `draft: false` is set
- [ ] Post has been previewed with `hugo server`
