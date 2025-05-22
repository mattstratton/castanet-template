# Podcast Site Template (Castanet)

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/netlify/netlify-statuskit)

This repository is a template for creating a new podcast website using the [Castanet](https://github.com/mattstratton/castanet) theme for [Hugo](https://gohugo.io/). It provides a ready-to-use structure for hosting, managing, and publishing your podcast episodes with ease.

## Features
- Built with the Castanet Hugo theme
- Easy episode and guest management
- Configurable for any podcast
- Modern, responsive design

## Prerequisites
- [Hugo](https://gohugo.io/getting-started/installing/) (version 0.110.0 or later recommended)
- [Node.js](https://nodejs.org/) (for asset building, if needed)

## Getting Started

1. **Use this template**
   - Click "Use this template" on GitHub, or clone this repo:
     ```sh
     git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
     cd YOUR_REPO_NAME
     ```
2. **Install dependencies** (if using asset pipelines):
   ```sh
   npm install
   ```
3. **Run the development server:**
   ```sh
   hugo server
   ```
   Visit [http://localhost:1313](http://localhost:1313) to view your site.

## Configuration

Site configuration is managed in the `config/_default/` directory, especially `params.toml`. Here you can set:
- Podcast title, description, and copyright
- Social media links
- Podcast feed details (Apple, Spotify, etc.)
- Host/author information

Example from `config/_default/params.toml`:
```toml
mainSections = ["episode"]
colorScheme = "slate"
description = "The HugoCast is the best podcast you've ever seen."
media_prefix = "https://media.blubrry.com/XXXX/"

[feed]
  apple_podcasts_author = "Your Name"
  apple_podcasts_image = "https://yoursite.com/img/podcast-logo.png"
  apple_podcasts_top_category = "Technology"
```

See comments in the file for more options.

## Adding Episodes
Episodes are stored as Markdown files in `content/episode/`. Use the provided archetype or copy an example file:

Example front matter from `content/episode/example-1.md`:
```toml
+++
title = "Did We Scare You?"
date = "2015-10-25T04:10:04-05:00"
episode = "1"
author = "Matt"
description = "Learning curve MVP scrum project..."
podcast_file = "arrested-devops-podcast-episode053.mp3"
podcast_duration = "1:08:22"
guests = ["example-1", "example-2"]
+++
Episode summary goes here.
```

## Customization
- Update images and branding in the `static/` directory.
- Adjust layouts or add custom pages in `layouts/`.
- Add hosts in the `[authors]` section of `params.toml`.

## Building for Production
```sh
hugo
```
The generated site will be in the `public/` directory.

## Learn More
- [Castanet Theme Documentation](https://github.com/mattstratton/castanet)
- [Hugo Documentation](https://gohugo.io/documentation/)

## License

This project is licensed under the [MIT License](LICENSE). 