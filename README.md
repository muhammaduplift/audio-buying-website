# Audio Buying App - Download Website

A simple, clean website for distributing the Audio Buying App APK using GitHub Pages and GitHub Releases.

## Setup Instructions

### 1. Push to GitHub

```bash
git add .
git commit -m "Initial commit: APK download website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/audio-buying-website.git
git push -u origin main
```

### 2. Upload Your APK to GitHub Releases

1. Go to your GitHub repository
2. Click on "Releases" (right sidebar)
3. Click "Create a new release"
4. Tag version: `v1.0.0`
5. Release title: `v1.0.0`
6. Upload your APK file and rename it to `app.apk`
7. Click "Publish release"

### 3. Enable GitHub Pages

1. Go to your repository settings
2. Navigate to "Pages" (left sidebar)
3. Under "Source", select `main` branch
4. Click "Save"
5. Your site will be live at: `https://YOUR_USERNAME.github.io/audio-buying-website/`

### 4. Update the Download Link

In `index.html`, update line 30:
```html
<a href="https://github.com/YOUR_USERNAME/audio-buying-website/releases/latest/download/app.apk"
```

Replace `YOUR_USERNAME` with your actual GitHub username.

### 5. Customize Content

Edit `index.html` to update:
- App name and description
- Features list
- Version number
- Installation instructions
- System requirements

## Updating the APK

When you have a new version:

1. Create a new release on GitHub
2. Upload the new APK (named `app.apk`)
3. Update the version number in `index.html`
4. Commit and push changes

The download link will automatically point to the latest release!

## Features

- ✅ Clean, modern design
- ✅ Responsive layout (mobile-friendly)
- ✅ Direct APK download from GitHub Releases
- ✅ No hosting costs
- ✅ Fast CDN delivery
- ✅ Version control for your APK files

## File Structure

```
audio-buying-website/
├── index.html          # Main download page
├── style.css           # Styling
└── README.md          # This file
```

## License

MIT License
