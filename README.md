# Markdown Documentation Site

Client-side markdown renderer that converts files from the `docs/` directory to HTML. No build process required.
You only need to upload the markdown files and it will work.

## Some details

- `index.html` uses Marked.js to render markdown files client-side
- JavaScript fetches directory listings to build the sidebar navigation
- Markdown files are loaded and rendered on demand
- Using Jetbrains Mono font... mmmm nice...

## Important: `.htaccess` File

The `docs/.htaccess` file enables Apache directory browsing:

```apache
Options +Indexes
IndexOptions FancyIndexing
```

This is required for the JavaScript to discover markdown files in subdirectories. Without it, the sidebar cannot list files.

## Setup

1. Place markdown files in `docs/` directory
2. Ensure `docs/.htaccess` is present
3. ....
4. profit !

