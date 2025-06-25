# IsoFier

**IsoFier** is a simple Python library to create `.iso` images from folders or selected files.

## 📦 Installation

```bash
pip install isofier
```

🚀 Usage

### Import the module and call create_iso():

From a folder:
```python
from isofier import create_iso

create_iso("C:/Users/Me/Documents/MyFolder", "myfolder.iso")

From a list of files

from isofier import create_iso

create_iso(["file1.txt", "file2.png"], "archive.iso")
```
📁 From specific files
```python
from isofier import create_iso

files = [
    "report.pdf",
    "image.png",
    "code/main.py"
]

create_iso(files, "archive.iso")
```

🔧 Function Reference

```python
create_iso(input: Union[str, List[str]], output: str) -> None
```

   - input: Either a path to a folder (str) or a list of file paths.

   - output: Path to the output .iso file.

If the input is a folder, all files and subfolders are recursively added to the ISO.


💻 CLI (Optional)

You can also use IsoFier in a Python script with command-line arguments:

```python
python create.py "C:/MyFolder" "output.iso"

Example code for create.py:

import sys
from isofier import create_iso

if len(sys.argv) != 3:
    print("Usage: python create.py <input_path> <output_iso>")
else:
    create_iso(sys.argv[1], sys.argv[2])
    print(" ISO created successfully!")
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

```python
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

