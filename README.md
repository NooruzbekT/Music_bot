# Music Downloader Bot

This is a Telegram bot that can download music from YouTube and manage your download history.

## Requirements

- Python 3.12.3
- aiogram 2.14.3
- yt-dlp 2025.1.15
- SQLite3
- IDE: PyCharm or VS Code (code written in PyCharm)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/NooruzbekT/Music_bot.git
    ```

2. Create a virtual environment and activate it:
    ```sh
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Install FFmpeg:
   - Download the latest full build of FFmpeg for your operating system from [gyan.dev](https://www.gyan.dev/ffmpeg/builds/).
   - Extract the downloaded archive and add the path to the `bin` folder (e.g., `.../ffmpeg/bin`) to your system's environment variable `PATH`.
   - To verify installation, run the following command in your terminal:
     ```sh
     ffmpeg -version
     ```

5. Create a bot on Telegram:
   - Go to [BotFather](https://t.me/BotFather) and follow the instructions to create a new bot.
   - Watch a YouTube tutorial for more detailed instructions if needed.
   - Copy the API token provided by BotFather and replace `API_TOKEN` in the code with this token.
## Usage

1. Run the bot:
    ```sh
    python mp3.py
    ```

2. Interact with the bot on Telegram using the following commands:
    - `/start` or `/help`: Get a welcome message and instructions.
    - `/download`: Start the process of downloading a track by providing its name and artist.
    - `/history`: Show your download history.
    - `/download_from_history`: Download tracks from your download history.
    - `/delete_history`: Delete your download history.

## Code Overview

The bot performs the following tasks:
- Handles user commands to interact with the bot.
- Downloads music from YouTube using `yt-dlp`.
- Converts and processes audio files using FFmpeg.
- Stores and retrieves download history using SQLite3.
- Manages user states using FSM (Finite State Machine) storage in `aiogram`.

### File Structure

- `mp3.py`: Main script containing the bot logic and command handlers.
- `mp3_db.db`: SQLite3 database file storing the download history.

### Detailed Description

- The bot uses `yt-dlp` to search for and download music from YouTube.
- Downloaded tracks are saved in the `music` directory.
- User interactions and states are managed using `aiogram`.
- Download history is stored in an SQLite3 database for easy retrieval and management.


## Note

- To use this code, you should have a basic understanding of the `aiogram` and `yt-dlp` libraries. If you lack this knowledge, you can watch video tutorials on YouTube.

- Comments in the code were written by AI and edited by me. 

- Before you start using the code, create a folder named `music` where all downloaded user songs will be stored. (You can later move everything to cloud storage if you wish.)

## Contact

For any inquiries or issues, please contact `nookentoktobaev@gmail.com`.
