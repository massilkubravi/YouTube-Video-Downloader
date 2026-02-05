
# YouTube Video Downloader (yt-dlp)

A minimal command-line YouTube video downloader written in Python using **yt-dlp**.

This tool fetches all available video formats for a given YouTube URL, lets the user manually choose a format, or automatically downloads the highest available resolution.

Simple, readable, and meant for learning—not production abuse.

---

## Features

- Lists all available video formats for a YouTube video
- Displays format ID, file extension, and resolution
- Manual format selection via terminal
- Automatic highest-resolution download option
- Uses `yt-dlp` (actively maintained `youtube-dl` fork)

---

## Requirements

- Python 3.8+
- yt-dlp

Install dependency:

```bash
pip install yt-dlp
````

---

## Installation

Clone the repository:

```bash
git clone https://github.com/massilkubravi/YouTube-Video-Downloader.git
cd YouTube-Video-Downloader
```

---

## Usage

Run the script:

```bash
python downloader.py
```

Follow the prompts:

1. Enter a YouTube video URL
2. Review the available formats printed in the terminal
3. Choose:

   * `y` to manually select a format ID
   * `n` to automatically download the highest-resolution format

The video will be saved in the current directory using the video title as the filename.

---

## Example Output

```text
137: mp4 (1080p)
136: mp4 (720p)
135: mp4 (480p)

Do you want to select from the available options? (y/n):
```

---

## How It Works

* Uses `yt-dlp` to extract video metadata without downloading
* Reads available formats from the video information
* Selects either:

  * A user-chosen format ID
  * The highest-resolution format based on video height
* Downloads the selected format

No GUI. No background processes. No hidden behavior.

---

## Limitations

Be aware of the following:

* Some high-resolution formats may be **video-only** (no audio)
* No automatic audio/video merging
* No playlist support
* No error handling for private or region-restricted videos
* No output directory selection

This is a basic script, not a full downloader application.

---

## Future Improvements

If you want to extend this project:

* Automatically download and merge best video + audio
* Add CLI arguments using `argparse`
* Add exception handling and logging
* Support playlists
* Add output directory configuration

---

## Legal Disclaimer

This project is intended for **educational purposes only**.

Downloading copyrighted content without permission may violate YouTube’s Terms of Service or local laws.
You are solely responsible for how you use this software.

---




