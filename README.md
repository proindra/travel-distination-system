# 🌍 Travel Destination Finder

A Python GUI application built with **Tkinter** that helps users find their ideal travel destinations based on selected preferences like climate, activities, and travel style.
🗺️ The app filters and ranks destinations from a CSV dataset based on features such as popularity, pricing, and selected categories.

---

## 🎯 Features

* 🖼️ **User-friendly GUI** built with Tkinter
* ✅ **Select travel preferences** such as tropical, adventure, historic, etc.
* 📊 **Filters destinations** based on matching features
* 🔝 **Ranks results by popularity** and price
* 🚨 **Fallback suggestions** when no match is found
* 📄 Easy-to-extend **CSV format** for new destinations

---

## ⚙️ How It Works

1. 📥 **Loads data** from a CSV file (`travel_destinations.csv`)
2. 🧾 User selects preferences:

   * Climate: Tropical, Cold
   * Activities: Adventure, Relaxation, Cultural, Nature, Shopping
   * Style: Modern, Historic
3. 🧠 App **filters destinations** matching selected preferences
4. 🌟 Displays **top 5 results** sorted by popularity
5. ❌ If no destination matches, shows **top 5 most popular** as suggestions

---

## 🧪 Quick Code Preview

Here's a small snippet from the project to get you started quickly:

```python
import tkinter as tk
from tkinter import messagebox
import csv

# Load destinations from CSV
def load_destinations(file_path):
    destinations = []
    try:
        with open(file_path, mode='r') as file:
            reader = csv.DictReader(file)
            for row in reader:
                row["popularity"] = float(row["popularity"])
                row["price"] = float(row["price"])
                for key in row:
                    if row[key] in {"0", "1"}:
                        row[key] = int(row[key])
                destinations.append(row)
    except Exception as e:
        messagebox.showerror("Error", f"Failed to load destinations: {e}")
    return destinations

# Start GUI
root = tk.Tk()
root.title("Travel Destination Finder")
root.geometry("500x600")
root.mainloop()
```

📌 Copy-paste this in `main.py` and make sure you have a CSV file named `travel_destinations.csv`!

---

## 🗃️ CSV File Format

Your `travel_destinations.csv` should include the following headers:

| Header           | Description                         | Type     |
| ---------------- | ----------------------------------- | -------- |
| `competitorname` | Name of the destination             | `string` |
| `popularity`     | Popularity score (higher is better) | `float`  |
| `price`          | Approximate price or cost           | `float`  |
| `tropical`       | 1 if tropical, 0 otherwise          | `int`    |
| `cold`           | 1 if cold, 0 otherwise              | `int`    |
| `adventure`      | 1 if offers adventure               | `int`    |
| `relaxation`     | 1 if offers relaxation              | `int`    |
| `cultural`       | 1 if culturally rich                | `int`    |
| `nature`         | 1 if nature-centric                 | `int`    |
| `shopping`       | 1 if shopping is a key activity     | `int`    |
| `modern`         | 1 if modern experience              | `int`    |
| `historic`       | 1 if historically rich              | `int`    |

---

## 🚀 Getting Started

### 🧰 Requirements

* Python 3.x (no external libraries needed)
* File: `main.py`
* Data: `travel_destinations.csv`

### ▶️ Run the App

```bash
python main.py
```

Make sure `main.py` and `travel_destinations.csv` are in the **same folder**.

---

## 🛠️ Technologies Used

* 🐍 Python 3.x
* 🖼️ Tkinter (GUI)
* 📄 CSV (Data Storage)

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

Made with ❤️ by **PRAJWALINDRA**
Let travel meet tech — one destination at a time 🌐✈️
