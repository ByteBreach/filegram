# filegram

filegram is a Python package to send files to Telegram groups.

## Installation

You can install filegram using pip:

```
pip install filegram
```

## Features

- Send files to Telegram groups easily from Python scripts or command line.
- Supports sending all types of files including images, PDFs, documents, etc.
- Flexible options to send specific files, files matching a pattern, or all files from a directory.

## Benefits

- **Easy Integration:** Quickly integrate file sending functionality into your Python projects.
- **Supports All File Types:** Send any type of file supported by Telegram.
- **Command-line Interface:** Use filegram from the command line for easy automation and scripting.
- **Cross-platform:** Works on Windows, macOS, and Linux.
- **Pythonic API:** Simple and intuitive Python API for sending files programmatically.

## Usage

## Command-line Usage:

```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id" [--path /path/to/directory] [--file filename] [--filetype *.pdf]
```

### Options:

- ` -h`, `--help`            Show this help message and exit
  
-  `--path /path/to/directory`    Directory path to send files from (default: current directory)
  
-  `--file filename`       Specific file to send
  
-  `--filetype *.pdf`      File type to send (e.g., *.pdf)

### Examples:

 - To send all files from the current directory:

```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id"
```

 - To send all files from a specific directory:

```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id" --path /path/to/directory
```

-  To send a specific file:
  
```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id" --file filename.txt
```

-  To send files matching a specific file type:

```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id" --filetype *.pdf
```

-  To send all files matching a pattern:
  
```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id" --filetype *.png
  ```

  - To send all files from a specific directory and a specific file:
  
```bash
filegram --token "YOUR_BOT_TOKEN" --chat "@your_chat_id" --path /path/to/directory --file file.txt
```

### Basic Usage:

```python
import filegram

# Replace these variables with your bot token and chat ID
BOT_TOKEN = 'YOUR_BOT_TOKEN'
CHAT_ID = 'YOUR_CHAT_ID'
directory_path = '/path/to/your/directory'

# Send all files from the current directory
if filegram.send_files(BOT_TOKEN, CHAT_ID, directory_path):
    print("Files sent successfully")
else:
    print("Failed to send files")
```

### Additional Usages:

- To send specific types of files from a directory:

```python
import filegram

# Replace these variables with your bot token, chat ID, directory path, and file type
BOT_TOKEN = 'YOUR_BOT_TOKEN'
CHAT_ID = 'YOUR_CHAT_ID'
directory_path = '/path/to/your/directory'
file_type = '*.jpg'

if filegram.send_files(BOT_TOKEN, CHAT_ID, directory_path, filetype=file_type):
    print("JPEG files sent successfully")
else:
    print("Failed to send JPEG files")
```

- To send a specific file type:

```python
import filegram

# Replace these variables with your bot token and chat ID
BOT_TOKEN = 'YOUR_BOT_TOKEN'
CHAT_ID = 'YOUR_CHAT_ID'
directory_path = '/path/to/your/directory'
file_type = '*.css'

# Send all files from the specified directory with the specified file type
if filegram.send_files(BOT_TOKEN, CHAT_ID, directory_path, filetype=file_type):
    print("Files sent successfully")
else:
    print("Failed to send files")
```

- To send a single file type from a directory:

```python
import filegram

# Replace these variables with your bot token, chat ID, directory path, and file type
BOT_TOKEN = 'YOUR_BOT_TOKEN'
CHAT_ID = 'YOUR_CHAT_ID'
directory_path = '/path/to/your/directory'
file_type = '*.docx'

if filegram.send_files(BOT_TOKEN, CHAT_ID, directory_path, filetype=file_type):
    print("DOCX files sent successfully")
else:
    print("Failed to send DOCX files")
```

- To send a specific file and check if it's sent:

```python
import filegram

# Replace these variables with your bot token, chat ID, and file path
BOT_TOKEN = 'YOUR_BOT_TOKEN'
CHAT_ID = 'YOUR_CHAT_ID'
file_path = '/path/to/your/file.txt'

if filegram.send_file(BOT_TOKEN, CHAT_ID, file_path):
    print("File sent successfully")
else:
    print("Failed to send file")
```

- To send all files from the current directory:

```python
import filegram

# Replace these variables with your bot token and chat ID
BOT_TOKEN = 'YOUR_BOT_TOKEN'
CHAT_ID = 'YOUR_CHAT_ID'

if filegram.send_files(BOT_TOKEN, CHAT_ID):
    print("All files from the current directory sent successfully")
else:
    print("Failed to send files")
```

## Thanks for Using filegram!

We hope you find filegram helpful for your projects. If you have any questions, suggestions, or issues, please feel free to open an issue on [GitHub](https://github.com/ByteBreach/filegram).

