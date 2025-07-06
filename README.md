# 🔍 Python Plagiarism Detector


This is a simple plagiarism checker built using Python's built-in `difflib` library. It compares the contents of two text files and outputs the percentage of similarity between them.

## 📁 Files Included

- `plagiarism-detector.py` — The Python script to calculate the plagiarism percentage upto two decimal values.
- `demo1.txt` — The original or reference file.
- `demo2.txt` — The file to be tested for plagiarism.

## 💡 How It Works

The script uses the `SequenceMatcher` class from the `difflib` module to compute the similarity ratio between the two files. It reads both files, compares their content, and prints the result as a percentage.

## 🧾 Code Sample

```python
from difflib import SequenceMatcher

with open('plagiarism.txt') as one_file, open('no-plagiarism.txt') as two_file:
    data_file1 = one_file.read()
    data_file2 = two_file.read()

    matches = SequenceMatcher(None, data_file1, data_file2).ratio()

    print(f"The plagiarism content is {matches * 100:.2f}%.")
```

---


## 🛠 Requirements

No external libraries are required. It runs with:

- Python 3.x

---

## 🚀 How to Run

1. Save your suspected file as `plagiarism.txt`.

2. Save your original/reference file as `no-plagiarism.txt`.

3. Run the script:

```bash
python plagiarism-detector.py
```

You’ll get an output like:

```bash
The plagiarism content is 86.25%.
```

---

## 📌 Note

- This is a basic string-level comparison.
- It does **not** detect paraphrasing or semantic similarities.
- For **educational purposes only**.

---

## 👨‍💻 Author

**Kuldeep Soni**  
📧 kuldeepsoni.dev@gmail.com  
🌐 [GitHub](https://github.com/justkuldeep) | [LinkedIn](https://www.linkedin.com/in/justkuldeep)

---

## 📄 License

**MIT License** — Feel free to use or modify it for learning and development.
