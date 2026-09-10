# 📷 Image EXIF & Location Inspector

A lightweight, browser-based tool to extract **EXIF metadata** and **GPS location** from images. Runs entirely in the browser — no server, no uploads, no tracking.

---

## ✨ Features

- **Full EXIF extraction** — camera make/model, date taken, aperture, shutter speed, ISO, focal length, flash, orientation, software, white balance, metering mode
- **GPS coordinates** — latitude, longitude, altitude, GPS date, and GPS time
- **Interactive map** — GPS location plotted on OpenStreetMap via Leaflet
- **100% offline-capable** — after the page loads, everything runs locally
- **Privacy-first** — images never leave the user's device
- **Mobile-friendly** — responsive layout works on phones and desktops
- **No install, no signup** — just open the URL and use it

---

## 🚀 How to Use

1. Open the live URL: `https://YOUR-USERNAME.github.io/exif-viewer/`
2. Click **"Pick from Gallery"** or **"Pick from Files"**, or tap the upload area
3. Select an image
4. View the extracted metadata and GPS map below

That's it. Nothing is uploaded, nothing is stored.

---

## 🌐 Live Demo

👉 [Open the tool](https://YOUR-USERNAME.github.io/exif-viewer/)

---

## 🛠️ Tech Stack

| Component | Purpose |
|---|---|
| [ExifReader](https://github.com/mattiasw/ExifReader) | Parses EXIF, GPS, IPTC, and XMP metadata |
| [Leaflet](https://leafletjs.com/) | Interactive maps |
| [OpenStreetMap](https://www.openstreetmap.org/) | Map tiles |
| Vanilla HTML/CSS/JS | No framework, no build step |

---

## 📱 Usage Notes

### On a desktop browser
Works perfectly. This is the **recommended** environment for reliable results.

### On Android (Chrome)
Android 13+ uses a **restricted Photo Picker** for privacy. This can prevent the browser from reading the raw file bytes, causing the error:

> *"The requested file could not be read, typically due to permission problems."*

**Workarounds:**
- Tap **"Pick from Files"** instead of **"Pick from Gallery"** — this opens the real File Manager
- Copy the image to the **Downloads** folder first, then pick it from there
- Use **Samsung Internet** instead of Chrome — its file picker behaves differently
- Open the page on a **computer** if possible

### On iPhone (Safari)
Works normally. Select the photo from your Library — Safari reads the file correctly.

---

## 🔒 Privacy

- No images are uploaded to any server
- No analytics, no tracking, no cookies
- All parsing happens in the user's browser using JavaScript
- The page only connects to the internet to load:
  - ExifReader library (CDN)
  - Leaflet library (CDN)
  - OpenStreetMap tiles (for the map)

You can verify this by opening **Developer Tools → Network** in your browser.

---

## ⚠️ Limitations

- **Metadata is often stripped** by messaging apps (WhatsApp, Telegram, Signal), social media, and some email clients
- **PNG files** generally don't contain EXIF data
- **HEIC files** (iPhone default) may have partial support depending on the browser
- **Screenshots** have no camera EXIF data (only file info)
- **GPS accuracy** varies — usually within 5–50 meters
- **Metadata can be edited** — this tool reads what's in the file, not what's necessarily true

For **audit purposes**, always request the **original image file** via email or cloud storage (not chat apps), and verify with a second tool if authenticity is critical.

---

## 🧪 Testing Your Setup

To confirm the tool works correctly:

1. Take a fresh photo with your phone — **enable Location in the Camera app settings**
2. Transfer it via **USB cable** or **email** to a computer (do **not** send via WhatsApp)
3. Open the tool on the computer
4. Upload the image
5. You should see the GPS map, camera model, date, and full metadata

If you see "⚠️ No GPS data found", the metadata was stripped during transfer.

---

## 📄 License

MIT License — free to use, modify, and share.

---

## 🙏 Credits

- EXIF parsing: [ExifReader](https://github.com/mattiasw/ExifReader) by Mattias Wallander
- Map rendering: [Leaflet](https://leafletjs.com/) by Volodymyr Agafonkin
- Map data: [OpenStreetMap](https://www.openstreetmap.org/) contributors

---

## 🐛 Issues / Contributions

Open an issue or submit a pull request on GitHub if you'd like to improve this tool.

---

**Built for practical image auditing. Runs anywhere, uploads nothing.**
