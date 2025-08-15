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

## 📁 CSV File Format

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

👉 All binary columns (`0` or `1`) indicate whether the feature applies to the destination.

---

## 🖥️ GUI Preview

```
+----------------------------------------+
| Select Your Travel Preferences         |
| [ ] Tropical     [ ] Cold              |
| [ ] Adventure    [ ] Relaxation        |
| [ ] Cultural     [ ] Nature            |
| [ ] Shopping     [ ] Modern            |
| [ ] Historic                             |
|                                        |
| [ Find Destinations ] [ Clear ]        |
|                                        |
| Results:                               |
| - Top picks with popularity & price - |
+----------------------------------------+
```

---

## 🚀 Getting Started

1. 📌 Make sure you have **Python 3.x** installed
2. 📁 Create a `travel_destinations.csv` with the format above
3. 🔽 Run the Python script:

```bash
python travel_finder.py
```

4. ✅ Select preferences and discover your ideal travel spot!

---

## 🛠️ Technologies Used

* 🐍 Python 3.x
* 🖼️ Tkinter for GUI
* 📄 CSV for data storage and filtering

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

Built with ✨ passion and Python by **PRAJWALINDRA**
Let travel meet tech — one destination at a time 🌐✈️

---
