# Project Matrixx – Markdown Viewer (GitHub Pages)

A lightweight, serverless Markdown viewer used by **Project Matrixx** to render device-specific documentation and changelogs directly from GitHub.
This tool lets us display `.md` files **independently of the main website**, especially when we need clean, readable device-specific pages.

---

## 🚀 Features

- **Render any Markdown file** via a simple URL parameter
  ```
  ?url=https://raw.githubusercontent.com/user/repo/branch/file.md
  ```
- Fully **serverless** — powered by GitHub Pages
- **Fast GitHub-style rendering** using markdown-it
- **Instant auto-update** whenever the remote Markdown changes
- **Embeddable anywhere**, including the main Project Matrixx website
- Zero backend, super lightweight, mobile-friendly

---

## 🔧 How It Works

The viewer fetches a remote Markdown file (like a ROM changelog or device guide) and renders it into readable HTML in the browser.

Viewer usage example:

```
https://install.projectmatrixx.org/?url=https://raw.githubusercontent.com/user/repo/branch/markdown.md
```

Just replace the `url=` parameter with any public raw Markdown link from GitHub.

---

## 📦 Usage

### **1. Open the Viewer**

```
https://install.projectmatrixx.org/?url=<RAW_MARKDOWN_URL>
```

Example (your changelog):

```
https://install.projectmatrixx.org/?url=https://raw.githubusercontent.com/Matrixx-Devices/android_vendor_MatrixxOTA/refs/heads/16.0/changelogs/source_changelog.md
```

### **2. Embed in Any Website**

```html
<iframe 
  src="https://install.projectmatrixx.org/?url=RAW_MARKDOWN_URL"
  style="width:100%;height:600px;border:none;">
</iframe>
```

Perfect for embedding device-specific docs or changelogs on the Project Matrixx website without manually converting Markdown into HTML.

---

## 🛠️ Technologies Used

- **GitHub Pages** — static hosting
- **Markdown-it** — fast Markdown parser
- **Vanilla JavaScript** — fetch & render logic
- **Simple CSS** — clean GitHub-like styling

---

## 📁 Project Structure

```
/ (root)
 ├── index.html     # Main viewer
 ├── README.md      # This file
 └── (no backend required)
```

---

## 💡 Why This Exists

Project Matrixx maintains device-specific documentation and changelogs in GitHub repositories.
Raw Markdown files are not user-friendly, so this viewer provides:

- Clean, readable rendered output
- A standalone docs viewer independent of the main site
- Fast updates — no need to edit WordPress or HTML manually
- Simple embed support for device installation instructions

This keeps our workflow fast, flexible, and developer-friendly.

---

## 🔒 Security Notes

- Only **public** Markdown URLs are supported
- HTML injection disabled (`html: false` in markdown-it)
- No backend → extremely low attack surface
- Everything renders client-side

---

## 🧩 Future Enhancements

- 🌙 Dark mode
- 🎨 Optional themes
- 📌 `?device=sweet` auto-loader for device pages
- 🧭 Sidebar navigation for multi-file docs
- ⚡ Client-side caching for faster reloads

---

## 🤝 Contributing

Pull requests, improvements, and feature suggestions are welcome!
If you want to help add themes, device-specific loaders, or UI enhancements — feel free to contribute.

---

## 📜 License

This project is open-source under the **MIT License**.
You are free to use, modify, and integrate it anywhere.
