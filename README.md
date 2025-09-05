# ✨ Text to QR Code Generator

Transform any text into a scannable **QR Code** instantly! 🚀
A simple, lightweight, and user-friendly tool for generating QR codes from text input.

---

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-brightgreen.svg" alt="license" />
  <img src="https://img.shields.io/badge/Language-JavaScript%20%7C%20Python-blue.svg" alt="language" />
  <img src="https://img.shields.io/badge/Status-Alpha-orange.svg" alt="status" />
</p>

---

## 🎯 Features

- ✅ Convert plain text, long messages, or URLs into QR codes instantly
- ✅ Download generated QR codes as **PNG**, **JPEG** or **SVG**
- ✅ Optional customization: size, margin, error-correction level, and filename
- ✅ Lightweight client-side option (no backend required)
- ✅ Simple, responsive UI with accessibility-first HTML

---

## 📸 Demo

Scan this sample QR to see an example output:

![QR Demo](https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=Hello%20from%20Text-to-QR)

---

<details>
<summary>✨ Quick Preview</summary>

```html
<!-- index.html snippet -->
<form id="qr-form">
  <textarea id="text" placeholder="Type or paste text / URL"></textarea>
  <input type="number" id="size" value="200" min="100" max="2000" />
  <select id="ec-level">
    <option value="L">L (Low)</option>
    <option value="M" selected>M (Medium)</option>
    <option value="Q">Q (Quartile)</option>
    <option value="H">H (High)</option>
  </select>
  <button type="submit">Generate</button>
  <button id="download">Download PNG</button>
</form>
<canvas id="qr-canvas"></canvas>
```

</details>

---

## ⚡ Installation

**Clone the repo**

```bash
git clone https://github.com/your-username/text-to-qr-generator.git
cd text-to-qr-generator
```

### JavaScript / Node (optional backend)

Install dependencies:

```bash
npm install
```

Run locally:

```bash
npm start
# or serve statically with a server like http-server
npx http-server . -p 8080
```

### Python (simple script)

Install Python dependency (Pillow will be pulled by qrcode if required):

```bash
pip install qrcode[pil]
```

Run the script:

```bash
python generate_qr.py "Your text here" --out myqr.png --size 400
```

---

## 🚀 Usage

### Web UI (client-side)
1. Open `index.html` in your browser.
2. Paste your text / URL into the textarea.
3. Set size, margin and error correction level.
4. Click **Generate** — the QR renders instantly.
5. Click **Download** to save the QR image.

### CLI (Python)

```bash
python generate_qr.py "https://example.com" --out example.png --size 500
```

**Example output**: `example.png` (a 500×500 px QR image)

---

## 🛠️ Project Structure

```
text-to-qr-generator/
├─ index.html        # UI
├─ style.css         # Styles
├─ script.js         # Client-side logic (qrcode generation + download)
├─ app.js            # Optional Node server (express)
├─ generate_qr.py    # Python CLI generator using qrcode library
└─ README.md         # This file
```

---

## 🔧 Options & Parameters

- **size**: Pixel size of the generated QR (e.g. 200, 400)
- **margin**: Quiet zone around QR (0–4)
- **ec-level**: Error correction `L`, `M`, `Q`, `H` (higher = more redundancy)
- **format**: PNG / JPEG / SVG (SVG for vector output)

---

## 💡 Tips & Accessibility

- Use an appropriate contrast between foreground and background for scannability.
- Provide an accessible label for the textarea and the generate button.
- Validate very long inputs — some data may require higher error correction.

---

## ♻️ Extending the Project (Ideas)

- Add **color** customization (foreground & background)
- Add **QR history** and preset saving
- Generate **Wi‑Fi** QR codes (network SSID + password)
- Add dark/light theme
- Add drag-and-drop to upload text files for batch QR generation

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository 🍴
2. Create a new branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add ..."`
4. Push and open a pull request 🚀

Please open an issue for larger changes or feature discussions.

---

## 📜 License

Distributed under the **MIT License**. See `LICENSE` for details.

---

## 🙌 Credits

Made with ❤️ by **Your Name** — feel free to ping me for collabs or designs.
