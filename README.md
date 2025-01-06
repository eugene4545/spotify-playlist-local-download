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

## macOS/Linux:
Install using a package manager:
- macOS: `brew install ffmpeg`
- Linux (Ubuntu): `sudo apt install ffmpeg`

After setup, the script will use FFmpeg to save downloaded files correctly!

## Installation
1. Clone the repository:
   ```
   git clone https://github.com/eugene4545/spotify-playlist-local-download.git 
   cd spotify-downloader
   ```
2. Install required Python packages:
   ```
   pip install -r requirements.txt  
   ```
3. Set up your Spotify API credentials:
    - Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
    - Create an application and retrieve the `Client ID` and `Client Secret`.
   
4. Create a `.env` file in the project root and add the following variables from the data retrieved from the dashboard:
   ```
      CLIENT_ID="your_spotify_client_id"
      CLIENT_SECRET="your_spotify_client_secret"
      REDIRECT_URL="http://localhost:8888/callback"
   ```
# Running the application
1. ### Run the script:
   To run the program in VSCode, click the 'Run' button in the top right corner while viewing main.py.
   When you run the app, it will ask you to go to a URL for authorization. Open the URL in your browser:
   ```
   https://accounts.spotify.com/authorize?client_id=your_spotify_client_id&response_type=code&redirect_uri=http%3A%2F%2Flocalhost%3A8888%2Fcallback&scope=user-library-read+playlist-read-private+playlist-read-collaborative
   ```
   Also you can use the command to run the script:
   ```
   python main.py
   ```
   
3. ### Login to Spotify and Authorize:
   After logging into your Spotify account, you will be prompted to grant permission to the app. Once authorized, you will be redirected to a URL, and you'll see an authorization code in the URL (after code=).

   Example of a successful URL:
   ```
   KBWN5LPQM3nRtXHYp8V-7mvZkkDJSBw4TCNR2X8ujKL9xb-MP2yFtTDwi_Nj6B4pXm1ZhPyqwNrLDDvWH7Uzsrwp4elS-xB2WJKrn5rVwgmSm197qO885KJMK74dwhbrk8gHhvSs1bY3sgRFlTfHTTzVm_NhIf6_UqCmjAy5FoAjzmxIp5WvKht906ksi42cQKhO-ni0yt9LlYnDAoiYFoK3PIROl8JwMYorl-7wjfxhpm3TPp6N5Vzjd_-iOz70Sbsuypk5OxQr
   ```
4. ### Enter the Authorization Code:
   Copy the authorization code from the URL and paste it back into your terminal when prompted:
   ```
   Enter the authorization code: [your_code_here]
   ```
   After entering the authorization code, the application will fetch an access token, and you will be able to download your playlists to your machine.
5. ### Select the playlist you'd like to download.
   ![App_playlist_select](image/Screenshot_(1342).png)

   
7. The tracks will be downloaded to the specified DOWNLOAD_DIRECTORY.

# Common Error
If you encounter an error like:
```
Spotify OAuth setup error: No client_id. Pass it or set a SPOTIPY_CLIENT_ID environment variable.
```

Ensure that your .env file contains the correct CLIENT_ID and CLIENT_SECRET.







      




