# Spotify Offline Playlist Downloader
This application allows you to download Spotify playlists for offline listening.  It interacts with the Spotify Web API to fetch playlist details and downloads the tracks for local storage.


## Features
- Download entire Spotify playlists locally.
- User-friendly interface for playlist selection.
- Supports audio file organization by artist, album, or custom folders.
- Handles errors during downloads and retries automatically.

## Getting Started
### Prerequisites
1. Python (v3.9 or higher)
2. Spotify Developer Account with API credentials
3. FFmpeg (Ensure it’s installed and added to your system PATH)
#### What is FFmpeg?
FFmpeg is a tool required by the script to process and convert Spotify audio streams into playable files on your machine.
### How to Install FFmpeg:
1. ### Download FFmpeg:
   - Go to [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html).
   - Download the version for your operating system.
2. ### Add FFmpeg to PATH (Windows):
   - Extract the downloaded file and place the folder (e.g., C:\ffmpeg) where it’s easy to find.
   - Add the `bin` folder (e.g., `C:\ffmpeg\bin`) to your system PATH:
   - Search for "Environment Variables" → Edit system PATH → Add the `bin` folder path → Save.
3. ### Verify Installation:
   - Open a terminal or command prompt and type `ffmpeg -version`.
   - If FFmpeg is installed, you’ll see version details.


      




