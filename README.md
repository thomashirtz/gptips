# GPTips

## Wrapping Code Block Text

When displaying code on web pages, ensuring readability is key. One common issue is horizontal overflow, especially with long lines of code. This guide presents CSS solutions to wrap code blocks for better readability, applicable to any web page and specifically tailored for LaTeX code blocks.

### General Solution for All Code Blocks

To make any code block wrap and avoid horizontal overflow, apply the following CSS:

```css
div.p-4.overflow-y-auto {
    overflow-y: visible !important; /* Make vertical overflow visible */
    overflow-x: auto !important; /* Allow horizontal scrolling if needed */
}

div.p-4.overflow-y-auto pre, 
div.p-4.overflow-y-auto code {
    white-space: pre-wrap !important;
    word-wrap: break-word !important;
    max-width: 100% !important;
}
```

### Specific Solution for LaTeX Code Blocks

If you want to specifically target LaTeX code blocks for wrapping, use this CSS:

```css
/* Targeting the div container that may cause scrolling, allowing for horizontal scroll */
div.p-4.overflow-y-auto {
    overflow-y: visible !important; /* Make vertical overflow visible */
    overflow-x: auto !important; /* Enable horizontal scrolling if necessary */
}

/* Specifically targeting LaTeX code blocks for text wrapping */
div.p-4.overflow-y-auto pre code.language-latex {
    white-space: pre-wrap !important; /* Enable wrapping of text */
    word-wrap: break-word !important; /* Break words at the end of the line */
    max-width: 100% !important; /* Ensure code does not exceed the container's width */
}
```

### Applying CSS with Stylus

To apply these styles without altering your website's code, you can use the Stylus browser extension:

1. Install Stylus for [Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/) or [Chrome](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?hl=en).
2. Click on the Stylus icon in your browser toolbar and select "Manage."
3. Click "Write new style."
4. Paste the CSS you want to use into the editor.
5. Name your style for easy reference.
6. Choose to apply the style to the URLS on the domain `chat.openai.com`.
7. Save your style.

This guide should help improve the readability of code blocks on your web pages by wrapping text to fit within the content area, enhancing the overall user experience.
