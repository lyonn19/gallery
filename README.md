# Liam Gallery

A beautiful, responsive art gallery website to showcase your child's drawings. Upload photos or draw directly in the browser.

## 📁 Project Structure

```
gallery/
├── index.html          ← The gallery website (everything you need!)
├── images/             ← Folder for storing drawing images (optional)
│   ├── drawing1.jpg
│   ├── drawing2.png
│   └── ...
└── README.md          ← This file
```

## 🚀 Quick Start

### 1. Prepare Your Project

You now have a `gallery/` folder with:
- `index.html` - The complete gallery (all in one file!)
- `images/` - Optional folder to store physical image files

### 2. Deploy to Netlify (Free!)

**Easiest way - Drag & Drop:**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the entire `gallery` folder onto the page
3. Your site goes live instantly! 🎉

**Alternatively - Git:**
1. Push `gallery/` folder to GitHub
2. Connect repo to Netlify
3. Auto-deploys on every push

## 🎨 How to Use

### Add Drawings

**Method 1: Upload Photos**
- Click "Upload a drawing +"
- Select the "Upload" tab
- Choose an image file (JPG, PNG, WEBP)
- Add title & description
- Click "Upload"

**Method 2: Draw in Browser**
- Click "Upload a drawing +"
- Select the "Draw" tab
- Draw with your mouse/touch
- Pick color and brush size
- Add title & category
- Click "Upload"

All drawings are stored on this device automatically!

### Navigate

- **All works** - View all drawings
- **Paintings / Drawings / Mixed media** - Filter by category
- **About** - Instructions
- **EN / FR / ES** - Change language

Click any drawing to view it full-screen.

## 💾 Important Notes

**Storage:**
- Drawings saved locally in browser (no cloud sync)
- Data persists across browser sessions
- Only visible on this device/browser
- Clear browser cache to delete all drawings

**Backup:**
- Right-click any drawing → "Save image as"
- Save to `images/` folder regularly

## 📝 Customize

### Change the Name

Open `index.html` in a text editor, find this line:
```html
<h1 class="site-title"><em>Liam</em> Gallery</h1>
```
Change "Liam" to your child's name.

### Change Colors

Find the `:root` section at the top of the CSS:
```css
--accent:#c8a96e;   /* Gold accents */
--dark:#1a1714;     /* Dark text */
--bg:#f5f3ef;       /* Light background */
```
Modify the hex colors as needed.

## 🌍 Languages

Supports English, French, and Spanish. Click the language buttons in the top right to switch.

## 🔧 Troubleshooting

**Uploads not working?**
- Check file size (keep under 5MB)
- Use JPG/PNG format
- Clear browser cache (Ctrl+Shift+Delete)
- Try a different browser

**Drawings disappeared?**
- Check if you cleared browser data
- Try another browser
- Right-click and save images you want to keep

## 📱 Responsive

Works perfectly on:
- Desktop computers
- Tablets
- Mobile phones

## 🆓 Free Forever

No backend, no database, no server needed. Everything runs in your browser!

---

**Ready?** Upload to Netlify now → [app.netlify.com/drop](https://app.netlify.com/drop) 🎨
