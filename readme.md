# CPL Generator

A Python tool to generate a PDF from your C++ Competitive Programming Library.

## 📂 Project Structure

Drop the `cpl-generator` folder directly into the root of your competitive programming repository. The script will recursively scan the parent directory for all `.cpp` files.

```text
your-cp-library/
├── Math/
│   ├── gcd.cpp
│   └── sieve.cpp
├── Graphs/
│   ├── dijkstra.cpp
│   └── dfs.cpp
└── cpl-generator/          <-- Drop the generator here
    ├── generator.py
    ├── requirements.txt
    └── icon.png            <-- Your team/university logo
```

## ⚙️ Setup & Installation

**1. Navigate to the generator folder:**
```bash
cd your-cp-library/cpl-generator
```

**2. Create and activate a Virtual Environment:**
```bash
python3 -m venv env
source env/bin/activate
```

**3. Install dependencies:**
```bash
pip install -r requirements.txt
```

## 🛠️ Configuration

Open the `generator.py` file and update the `user_info` dictionary at the bottom of the script with your personal details:

```python
if __name__ == '__main__':
    lib_data = scan_library_files()
    if lib_data:
        user_info = {
            'name': 'YOUR NAME',        
            'team': 'YOUR TEAM',        
            'icon_path': 'icon.png'     # Set to None if you don't have a logo
        }
        generate_pdf(lib_data, user_info)
```

## 🚀 Usage

Run the script from inside the `cpl-generator` folder:

```bash
python generator.py
```

A file named `library.pdf` will be generated in the same folder.
