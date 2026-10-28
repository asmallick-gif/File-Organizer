# 🗂️ File Organizer with GUI (Tkinter)

A simple yet powerful file organizer built with Python and Tkinter. It automatically sorts files into folders by type (images, documents, videos, archives, music, and more) and includes undo and scheduling support.

---

## Features

- Organize files into folders based on file extension
- Undo the most recent organization action
- Schedule automatic organization at a chosen interval
- User-friendly GUI interface
- Log file operations
- Support for a wide range of file types

---

## Requirements

- Python 3.6 or higher

No external libraries are required. The project uses the Python standard library only.

---

## How to Run

### 1. Save the script

Save the Python file as:

```bash
file_organizer.py
```

### 2. Run the application

Open a terminal or command prompt and run:

```bash
python file_organizer.py
```

This will launch the GUI window.

---

## How to Use

### Organize Files

1. Click `Browse`.
2. Select the folder you want to organize.
3. Click `Organize Files`.

The application will move files into folders such as:

- `Images/`
- `Documents/`
- `Videos/`
- `Archives/`
- `Music/`
- `Others/`

A success message appears when the process finishes.

### Undo Organize

If you made a mistake:

1. Click `Undo Last Organize`.
2. Files are moved back to their original locations.

This only works for the most recent organization operation.

### Schedule Automatic Organizing

1. Enter the interval in minutes.
2. Click `Start Scheduler`.
3. The selected folder is organized automatically at the chosen interval.

To stop the scheduler, click `Stop Scheduler`.

---

## Example

Suppose your folder contains:

```text
project/
├── image1.jpg
├── doc1.pdf
├── song1.mp3
├── archive1.zip
```

After organizing, it becomes:

```text
project/
├── Images/
│   └── image1.jpg
├── Documents/
│   └── doc1.pdf
├── Music/
│   └── song1.mp3
├── Archives/
│   └── archive1.zip
```

---

## Logs

All file moves and scheduling events are logged to:

```text
file_organizer.log
```

## Undo Tracking

The application stores move records in:

```text
undo_record.json
```

This file is used by the undo feature and is removed after the undo operation is complete.

---

## Supported File Types

| Category | Extensions |
|----------|------------|
| Images | `.jpg`, `.jpeg`, `.png`, `.gif`, `.bmp`, `.tiff` |
| Documents | `.pdf`, `.doc`, `.docx`, `.txt`, `.xls`, `.xlsx`, `.ppt`, `.pptx` |
| Archives | `.zip`, `.rar`, `.7z`, `.tar`, `.gz` |
| Videos | `.mp4`, `.mov`, `.avi`, `.mkv` |
| Music | `.mp3`, `.wav`, `.aac`, `.flac` |
| Others | Everything else |

---

## Notes

- Organizing and undo operations affect only files, not subfolders.
- Undo works only for the most recent action.
- Do not delete `undo_record.json` unless you are sure you no longer need to undo.

---

## Deployment

You can optionally convert the app to a standalone executable with PyInstaller:

```bash
pip install pyinstaller
pyinstaller --noconsole --onefile file_organizer.py
```

This generates an executable in the `dist/` folder.

---

## License

MIT License. Free to use, modify, and distribute.

---

## Author

Made with ❤️ using Python and Tkinter.
