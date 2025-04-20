# HWFWM Character Wiki

A fan-made wiki for tracking characters and their appearances in the novel HWFWM. This wiki is built with Jekyll and hosted on GitHub Pages.

## Features

- Character profiles with detailed information
- Track character appearances by chapter
- Easy search and filtering of characters
- Responsive design for mobile and desktop
- Expandable template system

## Getting Started

### Prerequisites

To run this site locally, you'll need:

- [Ruby](https://www.ruby-lang.org/en/downloads/) (version 2.5.0 or higher)
- [Bundler](https://bundler.io/)
- [Git](https://git-scm.com/)

### Installation

1. Clone this repository:
   ```
   git clone https://github.com/HWFWM/Wiki.git
   cd Wiki
   ```

2. Install dependencies:
   ```
   bundle install
   ```

3. Run the site locally:
   ```
   bundle exec jekyll serve
   ```

4. View the site at `http://localhost:4000/Wiki/`

## Adding Content

### Adding a New Character

See [How to Add a New Character](how-to-add-character.md) for detailed instructions.

### Adding Character Images

1. Add character images to the `assets/images/` directory
2. Reference the image in the character's front matter:
   ```yaml
   image: character-name.jpg
   ```

## Customization

### Site Configuration

Edit `_config.yml` to change the site name, description, and other configuration options.

### Styling

The site uses SCSS for styling. Edit the files in `assets/css/` to customize the look and feel.

## Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the main branch.

To set up GitHub Pages:

1. Go to your repository settings
2. Scroll down to the GitHub Pages section
3. Select the "main" branch as the source
4. Click Save

Your site will be available at `https://HWFWM.github.io/Wiki/`

## Notes

- This wiki is a fan project and is **not** affiliated with Shirtaloon!!!
- Character information is based on the chapters (up to the latest one on Royal Road) and may contain spoilers for e-Book readers!
