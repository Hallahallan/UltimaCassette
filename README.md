# Ultima Cassette

A web application inspired to be used by the Ultima Music Festival that plays audio snippets and collects emotional responses through an interactive word cloud interface.

## Quick Overview

**User Flow:**
1. **Start Screen** - Click play button
2. **Emotion Selection** - Listen to audio while selecting feelings from word cloud
3. **Email Collection** - Submit email address
4. **Thank You** - Session complete

**Data Collection:** Audio played, selected emotions, and email addresses are automatically saved to Google Sheets.

## How to Add New Songs

### Step 1: Add Audio Files
1. Place your MP3 files in the `audio/` folder
2. **Requirements:**
   - Format: `.mp3` (best browser compatibility)
   - Length: 15-30 seconds recommended
   - Size: Under 5MB per file
   - Naming: Use descriptive names (e.g., `ambient_calm.mp3`)

### Step 2: Update the Songs Array
In `UltimaCassette.html`, find this section and add your new files to the songs array:

```javascript
const songs = [
    'audio/love.mp3',
    'audio/nature.mp3',
    'audio/your-new-song.mp3',  // Add your files here
    'audio/another-song.mp3'    // Add as many as you want
];
```

### Step 3: Test
- Open the app in your browser
- Check browser console (F12) for any error messages
- Verify audio plays correctly on Screen 2

## Project Structure

```
UltimaC/
├── UltimaCassette.html     # Main application file
├── audio/                  # Audio files folder
│   ├── love.mp3
│   ├── nature.mp3
│   └── (your new songs)
└── README.md              # This file
```

## Configuration

**Google Sheets Integration:** Update `GOOGLE_APPS_SCRIPT_URL` in the JavaScript section with your Google Apps Script deployment URL.

**Emotion Words:** Modify the `emotions` array to customize the word cloud options.

## Deployment

Works with any static hosting service:
- **Netlify**: Drag & drop your folder
- **GitHub Pages**: Push to a repository
- **Vercel**: Connect your Git repository

## Troubleshooting Audio

❌ **Audio not playing?**
- Check file paths match the `songs` array exactly
- Verify audio files are in the correct `audio/` folder
- Test individual files: `your-site.com/audio/filename.mp3`
- Check browser console for 404 errors

❌ **Autoplay blocked?**
- This is normal browser behavior
- Audio starts after user interaction (clicking the play button)

## Tech Stack

- **Frontend**: Vanilla HTML/CSS/JavaScript
- **Audio**: HTML5 Audio API
- **Backend**: Google Apps Script (for data collection)
- **Hosting**: Static hosting (Netlify/GitHub Pages)

---

**Total setup time:** ~15 minutes  
**Cost:** Free (with Google Sheets + static hosting)