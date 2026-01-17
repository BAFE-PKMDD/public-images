# Public Images – Email Usage Guide

This repository contains **public images intended for use in emails** (transactional and system emails such as **FMR Watch** notifications).

The images are hosted via **GitHub + jsDelivr CDN**, making them **safe and compatible with major email clients** (Gmail, Outlook, Yahoo, Apple Mail).

---

## ❗ Important Rule

**DO NOT use GitHub `blob` URLs in emails.**  
They will **not render** in email clients.

❌ Wrong:
```
https://github.com/BAFE-PKMDD/public-images/blob/main/fmr-watch-with-da-bafe.png
```

---

## ✅ Correct Image URL (Email-Safe)

Use the **jsDelivr CDN URL** format:

```
https://cdn.jsdelivr.net/gh/BAFE-PKMDD/public-images@main/fmr-watch-with-da-bafe.png
```

This URL:
- Uses HTTPS
- Is CDN-backed
- Works in Gmail, Outlook, Yahoo, Apple Mail
- Is suitable for production email use

---

## 📌 Usage with React Email

```tsx
import { Img } from "@react-email/components";

<Img
  src="https://cdn.jsdelivr.net/gh/BAFE-PKMDD/public-images@main/fmr-watch-with-da-bafe.png"
  alt="FMR Watch - DA BAFE"
  width="300"
  style={{ display: "block" }}
/>
```

### Best Practices
- Always set a **fixed width**
- Keep images **under 200–300 KB**
- Use **PNG or JPG** (avoid SVG in emails)
- Include meaningful `alt` text

---

## 📌 Usage with Plain HTML Email

```html
<img
  src="https://cdn.jsdelivr.net/gh/BAFE-PKMDD/public-images@main/fmr-watch-with-da-bafe.png"
  alt="FMR Watch - DA BAFE"
  width="300"
  style="display:block;"
/>
```

---

## 🔄 Updating Images (Cache Busting)

If an image is updated but email clients still show the old version, append a version query:

```
https://cdn.jsdelivr.net/gh/BAFE-PKMDD/public-images@main/fmr-watch-with-da-bafe.png?v=1
```

Increase `v=` when updating the image.

---

## 🚫 What NOT to Do

- ❌ Do not use Base64 images in emails
- ❌ Do not use Google Drive, Dropbox, or Imgur links
- ❌ Do not use private repositories
- ❌ Do not remove or rename files without updating references


---

## 🔐 Security Notes

- This repository is **public by design**
- Do **not** upload sensitive or private images
- Images here are accessible by anyone with the URL

---

## 🧪 Quick Test

If the image URL opens **directly as an image in your browser**, it will work in email.

---

## 🏷 Maintainer Notes

- Repo: `BAFE-PKMDD/public-images`
- CDN Provider: **jsDelivr**
- Intended use: **Email images only**
