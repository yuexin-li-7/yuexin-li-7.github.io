# Professional Portfolio Website

This is a professional portfolio website built with Jekyll and hosted on GitHub Pages. It features a clean, responsive design and includes blog functionality and project showcases.

## Features

- **Blog section** with posts organized by date
- **About/CV page** with resume embedding
- **Project showcase** highlighting your work
- **Responsive design** for all devices
- **GitHub Pages** integration for easy deployment

## Getting Started

### Prerequisites

- Ruby (version 2.5.0 or higher)
- RubyGems
- GCC and Make (for some Jekyll dependencies)

### Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/portfolio.git
   cd portfolio
   ```

2. Install Jekyll and dependencies:
   ```
   gem install bundler
   bundle install
   ```

3. Run the site locally:
   ```
   bundle exec jekyll serve
   ```

4. View the site at `http://localhost:4000`

## Customization

### Site Configuration

Edit `_config.yml` to set your site's title, description, and other settings.

### Content

- **Blog posts**: Add new blog posts in the `_posts` directory with the format `YYYY-MM-DD-title.md`
- **Projects**: Add new projects in the `_projects` directory
- **About page**: Edit `about.md` to update your information
- **Images**: Place images in the `media` directory
- **Resume**: Place your resume in the `docs` directory

### Design

- Edit styles in the `_sass` directory
- Update layouts in the `_layouts` directory
- Modify components in the `_includes` directory

## Deployment

This site is designed to be deployed to GitHub Pages. To deploy:

1. Update the `url` and `baseurl` in `_config.yml`
2. Push changes to your GitHub repository
3. Enable GitHub Pages in your repository settings

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Jekyll for the static site generation
- GitHub Pages for hosting 