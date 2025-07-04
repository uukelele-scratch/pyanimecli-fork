# pyanimecli

A powerful command-line interface for searching, getting info, and watching anime directly from your terminal, powered by the [YumaAPI](https://yumaapi.vercel.app/).



## Features

- **Search:** Find any anime by title.
- **Detailed Info:** Get comprehensive details including descriptions, episode lists, genres, and more.
- **Stream with VLC:** Watch subbed or dubbed episodes directly in VLC Media Player.
- **Automatic Subtitles:** Automatically downloads and loads subtitles for subbed streams.
- **Discover:** Browse recently updated episodes, top airing anime, and spotlight series.
- **Explore:** Search for anime by genre or studio.
- **Schedule:** Check the airing schedule for any given date.
- **Cross-Platform:** Works on both Linux and Windows.
- **Rich Formatting:** Clean, colorful, and easy-to-read output in your terminal.

## Prerequisites

1.  **Python 3.6+**
2.  **VLC Media Player:** Must be installed and accessible from your system's PATH. You can download it from [videolan.org](https://www.videolan.org/vlc/).
3.  **Required Utilities:**
    -   On **Linux**: `wget`
    -   On **Windows**: `curl` (Comes pre-installed on modern Windows 10/11).
4.  **Python Libraries:** `requests` and `rich`.

## Installation

1.  **Download the script:**
    Save the code as `pyanimecli.py`.

2.  **Install Python dependencies:**
    ```bash
    pip install requests rich
    ```

3.  **Make the script executable (Linux/macOS):**
    ```bash
    chmod +x pyanimecli.py
    ```

4.  **(Optional but Recommended) Add to your PATH:**
    To use `pyanimecli` from anywhere, move it to a directory in your system's PATH.

    -   **On Linux/macOS:**
        ```bash
        sudo mv pyanimecli.py /usr/local/bin/pyanimecli
        ```
    -   **On Windows:**
        Move `pyanimecli.py` to a folder that is included in your `Path` Environment Variable. You can then run it using `python pyanimecli.py <args>`.

## Usage

Get a full list of commands with `-h` or `-help`.

```bash
pyanimecli -h
```

### Command Examples

**1. Search for an anime:**
```bash
pyanimecli -s "Attack on Titan"
```

**2. Get detailed info for an anime (using the ID from the search results):**
```bash
pyanimecli -i "attack-on-titan-3d"
```
This will display the description and a list of all available episodes.

**3. Watch an episode (using the Episode ID from the info list):**
```bash
# Watch a subbed episode
pyanimecli -w "attack-on-titan-3d$episode$571" sub

# Watch a dubbed episode
pyanimecli -w "attack-on-titan-3d$episode$571" dub
```

**4. Browse Recently Updated Episodes:**
```bash
pyanimecli -re
```

**5. Browse Top Airing Anime:**
```bash
pyanimecli -ta
```

**6. Use Pagination:**
Add the `-p` or `-page` flag to any command that supports it.
```bash
pyanimecli -ta -p 2
```

**7. List all Genres and Search by Genre:**
```bash
# List all genres
pyanimecli -g

# Search for anime in the 'action' genre
pyanimecli -gs "action"
```

**8. View the Airing Schedule:**
```bash
# Get schedule for a specific date
pyanimecli -sc 2025-07-04
```

### Disclaimer
This tool is created for educational purposes. All content is sourced from the publicly available YumaAPI. Please respect the service providers.
