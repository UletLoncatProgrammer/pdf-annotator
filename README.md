# 📄✏️ PDF Live Annotator

Real-time PDF annotation sync between a **tablet/mobile** and a **laptop** — present through a projector.

---

## 🎯 What it does

| Device | Role |
|---|---|
| **Laptop** | Opens PDF, displays on projector, receives annotations |
| **Tablet/Phone** | Draws & marks on PDF, syncs to laptop in real-time |

---

## 🚀 Live Demo

👉 **[Open the app](https://YOUR-USERNAME.github.io/pdf-annotator)**

---

## 📱 How to Use

### Step 1 — Laptop (Presenter)
1. Open the app on your laptop browser
2. Click **"Open as Presenter"**
3. A **6-digit room code** and **QR code** will appear
4. Click **"Choose PDF File"** to load your PDF
5. Connect the laptop to the projector

### Step 2 — Tablet/Phone (Annotator)
1. Open the same app URL on your tablet
2. Click **"Join as Annotator"**
3. Scan the QR code **or** enter the 6-digit room code
4. Start drawing — annotations appear on the laptop instantly!

---

## 🎨 Drawing Tools

| Tool | Description |
|---|---|
| 🔴🔵🟢🟡⬜ | 5 pen colors |
| S / M / L | Pen size: small / medium / large |
| ⌫ Erase | Switch to eraser mode |
| 🗑 Clear | Clear current page annotations |
| ↩ Undo | Undo last stroke |
| ‹ / › | Navigate pages from tablet |

---

## 🌐 Deploy to GitHub Pages

### Method 1 — Manual (easiest)
1. Fork or create a new GitHub repository
2. Upload `index.html` to the repo root
3. Go to **Settings → Pages**
4. Set Source to **"Deploy from branch"** → `main` → `/ (root)`
5. Click Save — your app is live at `https://USERNAME.github.io/REPO-NAME`

### Method 2 — Auto deploy (with Actions)
Create `.github/workflows/deploy.yml` with the content from this repo — it auto-deploys on every push.

---

## 🔧 Technical Details

| Component | Technology |
|---|---|
| PDF Rendering | PDF.js 3.11 (Mozilla) |
| Real-time Sync | PeerJS (WebRTC P2P) |
| QR Code | QRCode.js |
| Backend | **None** — fully serverless! |

**How sync works:**
- Laptop creates a PeerJS room with a 6-digit code
- Tablet connects via WebRTC P2P (direct, no server relay for data)
- Drawing coordinates sent as normalized (0–1) values for device-size independence
- Annotations stored per-page on the presenter — persists when navigating

---

## 💡 Tips

- Both devices must be able to reach the internet (for PeerJS signaling)
- Works best on the **same Wi-Fi network** but also works over mobile data
- Use **fullscreen mode** (⛶ button) on laptop for cleaner projector display
- Tablet annotator can also **navigate pages** (‹ ›) — presenter follows

---

## 📋 Requirements

- Modern browser (Chrome recommended)
- Internet connection for initial peer connection
- No install required — runs entirely in browser

---

## 🏢 Made for

PT. Optima Rekayasa Teknologi — IT Vendor & Enterprise Solutions
