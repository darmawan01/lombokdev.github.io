# Lombok Dev Community Website

Jekyll-based website for Lombok Developer Community.

## Project Structure

- `_config.yml` - Jekyll configuration
- `_events/` - Event collection (meetups, workshops)
- `_galleries/` - Photo galleries
- `_certificates/` - Certificate collection
- `_register/` - Registration pages
- `_layouts/` - Page templates
- `_includes/` - Reusable HTML components
- `_posts/` - Blog posts
- `assets/` - CSS, JS, and images

## Project Setup

### Prerequisites

Install Ruby development headers (required for building native extensions):

```bash
# Ubuntu/Debian
sudo apt-get install ruby-dev build-essential

# Fedora/RHEL
sudo dnf install ruby-devel gcc make

# Arch Linux
sudo pacman -S ruby base-devel
```

### Install Bundler

**Option 1: Install to user directory (Recommended - avoids permission issues)**

```bash
# Install bundler to user directory (no sudo needed)
gem install --user-install bundler

# Add gem bin directory to PATH (add to ~/.zshrc for permanent)
export PATH="$HOME/.local/share/gem/ruby/3.0.0/bin:$PATH"
```

**Option 2: Use System Ruby (if you have sudo access)**

```bash
sudo gem install bundler
```

### Install Dependencies

After bundler is installed, install project dependencies:

```bash
bundle install
```

This will install all gems specified in `Gemfile` locally to the project (in `vendor/bundle/`).

## Development

### Run Development Server

```bash
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`

### Build Site

```bash
bundle exec jekyll build
```

Output will be in `_site/` directory.

### Serve with Live Reload

```bash
bundle exec jekyll serve --livereload
```

## Common Commands

- `bundle exec jekyll serve` - Start development server
- `bundle exec jekyll build` - Build static site
- `bundle exec jekyll clean` - Clean generated files
- `bundle update` - Update gem dependencies

## Troubleshooting

### Permission Errors

If you get permission errors when installing gems, use `--user-install`:

```bash
gem install --user-install bundler
```

### Missing Ruby Headers

If you see errors about missing `ruby.h`, install Ruby development headers:

```bash
sudo apt-get install ruby-dev build-essential
```

### Bundler Path Issues

If bundler is not found after installation, add it to your PATH:

```bash
export PATH="$HOME/.local/share/gem/ruby/3.0.0/bin:$PATH"
```

Add this line to your `~/.zshrc` or `~/.bashrc` to make it permanent.

## How Jekyll Works

This project uses Jekyll's static site generator features:

1. **Collections** (`_events/`, `_galleries/`, etc.) - Organized content types
2. **Layouts** (`_layouts/`) - Page templates
3. **Includes** (`_includes/`) - Reusable components
4. **Data Files** (`_data/`) - Structured data (YAML/JSON)
5. **Front Matter** - YAML metadata at the top of files
6. **Liquid Templates** - Dynamic content generation

When you run `bundle exec jekyll serve`, Jekyll:
- Reads `_config.yml` for site configuration
- Processes all files with front matter
- Renders Liquid templates
- Generates static HTML in `_site/` directory
- Serves the site at `http://localhost:4000`