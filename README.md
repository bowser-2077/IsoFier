# IsoFier

**IsoFier** is a simple Python library to create `.iso` images from folders or selected files.

## 📦 Installation

```bash
pip install isofier
```

🚀 Usage

Import the module and call create_iso():
From a folder:
```python
from isofier import create_iso

create_iso("C:/Users/Me/Documents/MyFolder", "myfolder.iso")

From a list of files

from isofier import create_iso

create_iso(["file1.txt", "file2.png"], "archive.iso")
```

🧠 Features

   - Create ISO from a folder or specific files

   - Cross-platform support (Windows/Linux)

   - Pure Python, no external dependencies

🛠️ Functions
```python
create_iso(input, output)
```

   - input: string (path to folder) or list of file paths

   - output: string (output ISO file path)

❗ Notes

   - On Windows, you must have permission to read all files/folders.

   - ISO creation uses temporary directory internally (auto-cleaned).

🔧 Example CLI Integration

```
if __name__ == "__main__":
    import sys
    from isofier import create_iso
    if len(sys.argv) >= 3:
        input_path = sys.argv[1]
        output_iso = sys.argv[2]
        create_iso(input_path, output_iso)
        print("ISO created successfully!")
    else:
        print("Usage: python my_script.py <input_path> <output.iso>")
```

📄 License
MIT


✨ Author
Created by Gaëtan Lerley

