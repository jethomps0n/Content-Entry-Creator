# Content-Entry-Creator

**Welcome!**

This script goes in tandem with [my website files](https://github.com/jethomps0n/My-Portfolio-Website). It offers an easy to navigate GUI interface for managing my [`data.json`]([https://github.com/jethomps0n/My-Portfolio-Website](https://github.com/jethomps0n/My-Portfolio-Website/blob/main/resources/json/data.json)) file, which contains the main content I promote on my website.

[On my website I promote my filmmaking content](https://itsjonathanthompson.com), from films to screenplays. So with that put into perspective, the only content I am displaying are either videos or PDFs.

Most of my video content is hosted through YouTube or Vimeo – this script allows me to paste a video link (or a link to a playlist) and automatically fetch the data I need to display on my site (with only a few manual actions). It can generate a short preview file, for active hovering over a given video thumbnail. The code for which is driven in large part by my [Video Preview Generator](https://github.com/jethomps0n/Video-Preview-Generator) repo. It can also smart parse through a list of credits (essential for filmmaking) and correctly format the credits to my need.

It can do the same with PDFs, in terms of fetching data, albeit there is less data to fetch from a given PDF.

Local files and [a wide range of sites](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md) are supported.

---
## Images
![CleanShot 2025-07-02 at 21 50 31](https://github.com/user-attachments/assets/e559d3f0-cf74-4750-8433-939fc1725134)
![CleanShot 2025-07-02 at 21 53 07](https://github.com/user-attachments/assets/c05ada76-b1f5-4196-901e-26edba4fdb4d)
![CleanShot 2025-07-02 at 21 56 08](https://github.com/user-attachments/assets/e17c788a-323e-45f7-84ee-a94892911cfb)

---
## Note
This script is highly specific to my use case, but if you would like to try out the script, a minimal install and usage guide is below.

---

## Installation Guide

### 1. Install Dependencies
- Python 3.7+
- ffmpeg

To install via Homebrew:
```sh
brew install python ffmpeg
```

### 2. Install Python Packages
- yt-dlp
- PyPDF2
- requests

To install via pip:
```sh
pip3 install yt-dlp PyPDF2 requests
```

### 3. Download Script
```sh
mkdir content-entry-creator
cd content-entry-creator
wget https://raw.github.com/jethomps0n/Content-Entry-Creator/main/contentEntryCreator.py
```

---

## Usage Guide

Navigate to the script directory and run:
```sh
python3 makeobject.py
```

Should be pretty simple from there. Folder/file paths and other commonly variable data can be modified near the top of the script.

---

## Alternate Usage Guide

I'm going to be using this tool frequently, and I don't want to have to use the CLI every time I want to open this script. So I've created a very simple Automator script to launch the app for me.

### In Automator:

1. **Choose "Application"**
2. **Search for and select "Run Shell Script"**
3. In the text area on the right, paste the code below (replacing `/path/to/` with the path to the file/folder):
    ```sh
    /path/to/python3 /path/to/contentEntryCreator.py
    ```
4. **Save and run the application**
