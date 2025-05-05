# Mintec Zola Theme

A minimal, responsive Zola theme focused on readability, featuring margin notes and a clean layout.

## Features

* **Minimal Design:** Focuses on content presentation.
* **Responsive Layout:** Adapts to various screen sizes, hiding margin notes and TOC on smaller devices.
* **Margin Notes:** Uses a shortcode `{{ marginnote(content="Your note here.") }}` or `{% marginnote() %} Your note here. {% end %}` to place notes in the margin (requires JavaScript).
* **Table of Contents (TOC):** Automatically generated for pages, sticky on desktop.
* **Dark Mode:** Toggleable light/dark theme based on user preference or button click.
* **Syntax Highlighting:** Enabled via Zola's built-in highlighting.
* **Simple Blog Index/Section Views:** Clean list of posts with dates.
* **Configurable Menu & Social Links:** Easily add navigation and social links via `config.toml`.

## Installation

1.  Download or clone this theme into your Zola site's `themes/` directory:
    ```bash
    git clone https://github.com/coffeeri/mintec-zola-theme.git themes/mintec
    ```
2.  Enable the theme in your `config.toml`:
    ```toml
    theme = "mintec"
    ```

## Configuration

Customize the theme via your site's `config.toml`:

```toml
# Base URL of your site
base_url = "[https://example.com](https://example.com)"

# Site title
title = "My Mintec Site"

# Optional site description
description = "A site using the Mintec theme"

# Set author
author = "Your Name"

# Enable syntax highlighting in code blocks
[markdown]
highlight_code = true
highlight_theme = "css" # Choose a Zola theme, e.g., "css", "ayu-dark"

# Enable taxonomies (e.g., tags)
taxonomies = [
    { name = "tags", feed = true },
]

# Generate RSS/Atom feed (requires feed_filenames)
generate_feed = true
feed_filenames = ["atom.xml"] # Or ["rss.xml"]

[extra]
# Optional: Add main navigation menu items
main_menu = [
    { url = "/", name = "Home" },
    { url = "/about", name = "About" },
    # Add other menu items here
]

# Optional: Add social media links (currently supports GitHub and LinkedIn text links)
# You can replace the text links in templates/base.html with SVG icons if desired.
[extra.social_links]
github = "http://github.com/your-user"
linkedin = "https://linkedin.com/in/your-account/"
