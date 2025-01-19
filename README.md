# YT-MusicGuardian 🎵

**YT-MusicGuardian** is a Python-based tool for downloading music from YouTube while keeping track of previously downloaded songs. It ensures your music collection stays clean and organized by skipping duplicate downloads.

## 🚀 Features
- **Smart Duplicate Tracking**: Tracks downloaded links to avoid re-downloading the same content.
- **Organized Music Library**: Automatically organizes songs into folders by name and genre.
- **Efficient Logging**: Provides detailed logs of downloads, errors, and skipped files.

---

## 📂 Repository Structure
```
|-- examples/
    |-- songs.csv                # Input file containing music details (name, URL, genre)
    |-- backup.json              # Tracks already downloaded music links
|-- downloader.py                # Main script to download and organize music
```

---

## 🧑‍💻 How to Use

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/YT-MusicGuardian.git
   cd YT-MusicGuardian
   ```

2. **Create a Python Virtual Environment in Linux**:
   ```bash
   python -m venv yt_music_env
   source yt_music_env/bin/activate
   ```

3. **Modify the Script**:
   - Open `downloader.py` and update the `PIP_ENV_PATH` constant with the path to your Python environment.
   - Example:
     ```python
     PIP_ENV_PATH = "/path/to/your/yt_music_env/bin/pip3"  # Update this with your virtual environment path
     ```

4. **Prepare Input Files**:
   - Create a `songs.csv` file with the following format:
     ```csv
     SongName;YouTubeURL;Genre
     ```
   - Example:
     ```csv
     Song1;https://www.youtube.com/watch?v=abc123;pop
     Song2;https://www.youtube.com/watch?v=def456;rock
     ```

5. **Run the Script**:
   ```bash
   python downloader.py
   ```

6. **Find Your Music**:
   - Downloaded songs will be saved in the `songs/` folder, organized by genre and name.

---

## 📋 Example
### Input (`songs.csv`):
```csv
Song1;https://www.youtube.com/watch?v=abc123;pop
Song3;https://www.youtube.com/watch?v=ghi789;jazz
```

### Backup (`backup.json`):
```json
[
    {
        "name": "Song1",
        "url": "https://www.youtube.com/watch?v=abc123",
        "genre": "pop"
    }
]
```

### Output:
- `Song3` will be downloaded.
- `Song1` will be skipped as it is already in `backup.json`.

---

## 🔧 Configuration
- Modify logging level and settings in the `Diagnostic` class.
- Adjust YouTube download settings in `downloader.py` by tweaking `ydl_opts`.

---

## 📜 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions
Contributions are welcome! Feel free to fork the repository, submit issues, or create pull requests.

---

Happy downloading! 🎶
