# 🗂️ File Organizer with GUI (Tkinter)

A simple yet powerful **File Organizer** built using **Python** and **Tkinter**. Automatically organizes files into folders by type (Images, Documents, Videos, etc.) and supports **undo** and **scheduled auto-organizing**.

---

## 📦 Features

- Organizes files into folders based on extensions
- Undo last organize operation
- Schedule auto-organization (every N minutes)
- User-friendly GUI
- Logging of all operations
- Supports a wide variety of file types

---

## 🧰 Requirements

- Python 3.6 or higher

### Install Dependencies (Only Standard Library used)
No external packages needed. Just ensure Python is installed.

---

## 🚀 How to Run

### 1. Save the Code

Save the provided Python code into a file named:
file_organizer.py

2. Run the Application
Open terminal or command prompt and run:

bash
Copy
Edit
python file_organizer.py
This will launch a GUI window.

🖥️ How to Use
🗃️ Organize Files
Click Browse to select the folder you want to organize.

Click Organize Files.

Files will be moved into folders like:

Images/

Documents/

Videos/

Archives/

Music/

Others/

A success message will pop up after organizing.

↩️ Undo Organize
If you made a mistake:

Click Undo Last Organize.

Files will be moved back to their original locations.

Works only for the last operation.

⏱️ Schedule Automatic Organizing
Enter the interval (in minutes) in the input field.

Click Start Scheduler.

The selected folder will be organized automatically at the given interval.

Click Stop Scheduler to cancel.

📁 Example
Suppose your folder contains:

python
Copy
Edit
project/
├── image1.jpg
├── doc1.pdf
├── song1.mp3
├── archive1.zip
After organizing, it becomes:

python
Copy
Edit
project/
├── Images/
│   └── image1.jpg
├── Documents/
│   └── doc1.pdf
├── Music/
│   └── song1.mp3
├── Archives/
│   └── archive1.zip
📝 Logs
All file moves and scheduling events are logged to:

lua
Copy
Edit
file_organizer.log
🔄 Undo Tracking
Moves are saved in:

pgsql
Copy
Edit
undo_record.json
Used for the Undo function. Gets deleted after undo is complete.

📦 Supported File Types
Category	Extensions
Images	.jpg, .jpeg, .png, .gif, .bmp, .tiff
Documents	.pdf, .doc, .docx, .txt, .xls, .xlsx, .ppt, .pptx
Archives	.zip, .rar, .7z, .tar, .gz
Videos	.mp4, .mov, .avi, .mkv
Music	.mp3, .wav, .aac, .flac
Others	Everything else

❗ Notes
Organizing and undo operations only affect files (not subfolders).

Undo only works for the most recent operation.

Don't delete undo_record.json if you plan to undo.

📤 Deployment
You can optionally convert it to a standalone app using PyInstaller:

bash
Copy
Edit
pip install pyinstaller
pyinstaller --noconsole --onefile file_organizer.py
This will generate an executable in the dist/ folder.

📄 License
MIT License. Free to use, modify, and distribute.

🙋‍♂️ Author
Made with ❤️ using Python and Tkinter.
