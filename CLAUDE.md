# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Vite-powered web application named "vitya" configured for deployment to GitHub Pages. The repository is hosted on GitHub at `git@github.com:thejsbro/vitya.git`.

## Technology Stack

- **Framework**: Vite (vanilla JavaScript)
- **Build System**: Vite bundler
- **Deployment**: GitHub Pages via GitHub Actions
- **Package Manager**: npm

## Repository Structure

```
.
├── index.html                    # Main HTML entry point
├── main.js                      # Main JavaScript file
├── style.css                    # Main stylesheet
├── package.json                 # npm configuration and scripts
├── vite.config.js              # Vite configuration with GitHub Pages setup
├── public/
│   └── vite.svg                # Static assets
├── .github/workflows/
│   └── deploy.yml              # GitHub Actions deployment workflow
├── README.md                   # Project description
└── CLAUDE.md                   # This file
```

## Development Commands

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Deploy to GitHub Pages (manual)
npm run deploy
```

## Architecture Notes

- **Base Path**: Configured for GitHub Pages deployment at `/vitya/`
- **Build Output**: Located in `dist/` directory
- **Deployment**: Automated via GitHub Actions on push to main branch
- **Assets**: Static assets should be placed in the `public/` directory

## GitHub Pages Setup

The app is configured to deploy automatically to GitHub Pages when changes are pushed to the main branch. The GitHub Actions workflow:

1. Builds the project with `npm run build`
2. Uploads the `dist/` folder as a Pages artifact
3. Deploys to GitHub Pages

Make sure GitHub Pages is enabled in repository settings and set to deploy from GitHub Actions.