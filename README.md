Here’s a polished **README.md** for your project:

---

# 🎨 SpectrumScript-CC02

**SpectrumScript-CC02** is a Django-based web application for **image color analysis**.
It allows users to upload an image and get detailed insights such as:

* Dominant and secondary colors
* Color palettes
* Matching/complementary colors
* Light/dark variations
* Color percentages in the image

---

## ⚡ Features

* Upload an image through a simple web form.
* Extract **dominant and secondary colors** using `KMeans clustering`.
* Generate **color palettes** (hex and RGB values).
* Suggest **matching colors** (complementary, triadic, analogous, split-complementary).
* Display **lighter/darker versions** of each palette color.
* Calculate **percentage distribution** of colors in the image.
* Built with **Django + OpenCV + scikit-learn + NumPy + Matplotlib**.

---

## 🛠️ Installation Guide

### **Step 1: Create Virtual Environment (Windows CMD)**

1. Navigate to the directory where you want the virtual environment.
2. Run:

   ```bash
   py -m venv myworld
   ```

### **Step 2: Install Packages**

1. Navigate to `myworld/Scripts`.
2. Copy the `requirements.txt` file into that directory.
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### **Step 3: Migrate the Project**

1. Download the `SpectrumScript-CC02` folder.
2. Place it in the same directory as your virtual environment (or nearby).
3. Navigate into `SpectrumScript-CC02/`.
4. Run migrations and collect static files:

   ```bash
   py manage.py migrate
   py manage.py collectstatic
   ```

### **Step 4: Run the Server**

1. Stay inside `SpectrumScript-CC02/`.
2. Start the Django development server:

   ```bash
   py manage.py runserver
   ```
3. Open the displayed **localhost URL** in your browser.

---

## 📂 Project Structure

```
SpectrumScript-CC02/
│── manage.py
│── SpectrumScript/        # Django project settings
│── app/                   # Main application
│   │── views.py           # Handles requests & image upload
│   │── backend/           # ImageColorAnalyzer class
│   │── models.py          # Image model
│   │── forms.py           # Upload form
│   │── templates/         # HTML templates (main.html, index.html)
│── media/                 # Uploaded images (temporary storage)
│── requirements.txt
```

---

## 🚀 How It Works

1. **Upload an Image** → via the main page (`main.html`).
2. **Backend Analysis** → `ImageColorAnalyzer` (OpenCV + scikit-learn) processes the image.
3. **Extract Colors** → Dominant, secondary, palette, lighter/darker, matching.
4. **Percentages** → Calculates how much of each color appears in the image.
5. **Results Page** → Displays all findings beautifully (`index.html`).

---

## 📊 Example Output

* **Dominant Color**: `#ff5733`
* **Second Dominant Color**: `#33c1ff`
* **Palette Colors**: `[ #ff5733, #33c1ff, #75ff33, ... ]`
* **Matching Colors**: `[ #33ffd7, #ff33b2, ... ]`
* **Percentages**: `[40%, 25%, 20%, 15%]`

---

## 📌 Requirements

* Python 3.8+
* Django
* OpenCV (`opencv-python` + `opencv-contrib-python`)
* NumPy
* scikit-learn
* matplotlib

---

## 🛠️ Future Improvements

* Add **downloadable palette files** (e.g., `.ase` for Adobe, `.gpl` for GIMP).
* Build **REST API** for programmatic color analysis.
* Enhance **UI** with live previews.
* Store and manage previous analyses.

---

## 👨‍💻 Author

Developed by **@Abishekganesh-BS**


