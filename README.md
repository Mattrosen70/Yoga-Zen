# 🧘 YOGA-ZEN: 90s Edition

> A retro-aesthetic relaxation app that blends 90s video game vibes with zen meditation

![Yoga-Zen](https://img.shields.io/badge/Yoga-Zen-90s%20Edition-purple?style=flat-square&logo=gameboy)
![HTML5](https://img.shields.io/badge/HTML5-000000?style=flat-square&logo=html5&logoColor=E34F26)
![CSS3](https://img.shields.io/badge/CSS3-000000?style=flat-square&logo=css3&logoColor=1572B6)
![JavaScript](https://img.shields.io/badge/JavaScript-000000?style=flat-square&logo=javascript&logoColor=F7DF1E)

---

## ✨ Features

🎮 **90s Video Game Aesthetic**
- Neon cyan & magenta glowing UI
- Flickering titles and animations
- Pixel-perfect scanlines
- Retro color scheme

🎵 **Dynamic Music Rotation**
- 6 calming yoga meditation tracks
- Auto-switches every 2-3 minutes
- Volume control slider
- Track display showing current selection

🧘 **Animated Yoga Poses**
- 8 different cartoon yoga poses
- Changes every 2 minutes
- Smooth pulsing animation
- Pose name displayed

📊 **Real-Time Session Statistics**
- Session timer
- Tracks played count
- Poses shown counter
- Live relaxation level meter
- Music visualizer with animated bars

🎮 **Intuitive Controls**
- Play / Pause / Stop buttons
- Volume slider (0-100%)
- Responsive button feedback
- Fully accessible keyboard support

📱 **Cross-Platform Compatible**
- Works on desktop, tablet, and mobile
- Responsive design that adapts to all screen sizes
- Smooth performance
- Touch-friendly buttons

---

## 🚀 Quick Start

### 1. **Clone the Repository**
```bash
git clone https://github.com/Mattrosen70/Yoga-Zen.git
cd Yoga-Zen
```

### 2. **Open the App**
```bash
# Option A: Direct (no audio)
open index.html

# Option B: Local Server (RECOMMENDED - audio will work)
# Python 3:
python -m http.server 8000
# Then visit: http://localhost:8000

# Option C: VS Code Live Server
# Right-click index.html → Open with Live Server
```

### 3. **Add Audio & Images**
- Create `assets/audio/` folder
- Create `assets/images/` folder
- Add 6 MP3 files and 8 PNG images
- See **SETUP_GUIDE.md** for detailed instructions

### 4. **Press PLAY**
Enjoy your zen meditation experience! 🧘✨

---

## 📁 Project Structure

```
Yoga-Zen/
├── index.html          # Main HTML interface
├── styles.css          # 90s aesthetic styling (neon, animations)
├── app.js              # Core application logic
├── README.md           # This file
├── SETUP_GUIDE.md      # Detailed asset setup instructions
├── .gitignore          # Git ignore configuration
└── assets/
    ├── audio/          # 6 yoga meditation MP3 tracks
    │   ├── zen-meditation.mp3
    │   ├── tranquil-garden.mp3
    │   ├── morning-sunrise.mp3
    │   ├── forest-whispers.mp3
    │   ├── ocean-waves.mp3
    │   └── himalayan-peace.mp3
    └── images/         # 8 yoga pose PNG images
        ├── pose-1.png
        ├── pose-2.png
        ├── pose-3.png
        ├── pose-4.png
        ├── pose-5.png
        ├── pose-6.png
        ├── pose-7.png
        └── pose-8.png
```

---

## 🎮 How It Works

### Music Rotation
- Automatically changes to a new track every **2-3 minutes** (randomized)
- 6 tracks loop in sequence
- Track name displayed in real-time

### Pose Rotation
- Changes to a new yoga pose every **2 minutes**
- 8 different poses cycle through
- Smooth animations with pulsing effect
- Pose name always visible

### Session Tracking
- **Session Time**: Elapsed time in HH:MM:SS format
- **Tracks Played**: Number of tracks rotated through
- **Poses Shown**: Number of yoga poses displayed
- **Relax Level**: Visual bar showing relaxation progress (starts at 80%, increases over time)

### Audio Controls
- **PLAY**: Start the meditation session
- **PAUSE**: Pause current track and timers
- **STOP**: Stop everything and reset session
- **Volume Slider**: Adjust audio level 0-100%

---

## 🎨 Design Highlights

### Color Scheme
- **Cyan (#00ffff)**: Primary accent, main text
- **Magenta (#ff00ff)**: Secondary accent, hover effects
- **Yellow (#ffff00)**: Status indicators, highlights
- **Green (#00ff00)**: Play button, success states
- **Dark Purple (#0a0e27)**: Background
- **Grid Pattern**: Visual grid overlay

### Animations
- **Title Flicker**: Glitchy text effect with color shifts
- **Glow Effects**: Neon box shadows and text shadows
- **Music Visualizer**: 5 animated bars bouncing to rhythm
- **Pose Pulse**: Gentle scale animation on yoga pose image
- **Button Hover**: Expanded glow and color intensity
- **Status Blink**: Yellow indicator pulses when playing

### Responsive Design
- **Desktop (1024px+)**: Full 2-column layout
- **Tablet (768px-1024px)**: Optimized controls
- **Mobile (480px-768px)**: Stacked single column
- **Small Mobile (<480px)**: Compact interface

---

## 🔧 Customization

### Change Rotation Times
Edit `app.js` line 117 (music) and 130 (poses):

```javascript
// Music rotation: 2-3 minutes (120-180 seconds)
const rotationTime = (120 + Math.random() * 60) * 1000;

// Pose rotation: 2 minutes (120 seconds)
this.poseRotationTimer = setInterval(() => {
    if (this.isPlaying) this.nextPose();
}, 120000); // Change 120000 to desired milliseconds
```

### Add More Tracks/Poses
Edit `app.js` around line 45 (tracks) and line 57 (poses):

```javascript
this.tracks = [
    { name: 'Your Track Name', file: 'assets/audio/your-file.mp3' },
    // Add more...
];

this.poses = [
    { name: 'Your Pose Name', image: 'assets/images/your-pose.png' },
    // Add more...
];
```

### Change Colors
Edit `styles.css` `:root` section (lines 1-12):

```css
:root {
    --neon-cyan: #00ffff;      /* Change any of these */
    --neon-magenta: #ff00ff;
    --neon-yellow: #ffff00;
    /* etc */
}
```

---

## 📋 Requirements

### Minimum
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No installation or dependencies required
- Works offline after initial load

### For Audio
- MP3 audio files (see SETUP_GUIDE.md)
- Local server recommended for CORS compliance

### For Images
- PNG images with transparency
- Pixel art style recommended for 90s aesthetic

---

## 🌐 Deployment

### GitHub Pages (Recommended)
```bash
# 1. Push code to GitHub
git push origin main

# 2. Go to repo Settings → Pages
# 3. Select "Deploy from a branch"
# 4. Choose "main" branch
# 5. Your app is live at: https://Mattrosen70.github.io/Yoga-Zen/
```

### Netlify
1. Connect GitHub repo
2. Build command: (leave blank)
3. Publish directory: (leave blank - use root)
4. Deploy!

### Vercel
1. Import GitHub repo
2. Framework: Other
3. Deploy!

---

## 🎯 Yoga Poses Included

1. **Mountain Pose** - Standing grounding pose
2. **Child Pose** - Restorative resting pose
3. **Tree Pose** - Balance and focus
4. **Downward Dog** - Full-body stretch
5. **Warrior Pose** - Strength and stability
6. **Lotus Position** - Meditation posture
7. **Cat-Cow Stretch** - Spinal mobility
8. **Savasana (Final Rest)** - Ultimate relaxation

---

## 🎵 Music Tracks Included

1. **Zen Meditation Breeze** - Peaceful morning meditation
2. **Tranquil Garden Vibes** - Nature-inspired calm
3. **Morning Sunrise Calm** - Awakening serenity
4. **Forest Whispers** - Ambient woodland sounds
5. **Ocean Waves Serenity** - Beach meditation
6. **Himalayan Peace** - Mountain zen vibes

---

## 📱 Browser Compatibility

| Browser | Support | Notes |
|---------|---------|-------|
| Chrome | ✅ Full | Recommended |
| Firefox | ✅ Full | Excellent audio support |
| Safari | ✅ Full | iOS & macOS |
| Edge | ✅ Full | Chromium-based |
| Opera | ✅ Full | Works perfectly |

---

## 🐛 Troubleshooting

### Audio not playing?
1. Check that MP3 files are in `assets/audio/`
2. Use a local server (not `file://` protocol)
3. Check browser console (F12) for errors
4. Try different browser

### Images not showing?
1. Verify PNG files in `assets/images/`
2. Check filenames match exactly (lowercase)
3. Ensure images are valid PNG format
4. Check file size < 500KB

### App not responsive?
1. Clear browser cache (Ctrl+Shift+Del)
2. Hard refresh (Ctrl+Shift+R)
3. Try different browser
4. Check console for JavaScript errors

---

## 📚 Asset Setup

See **SETUP_GUIDE.md** for detailed instructions on:
- Where to download free audio tracks
- How to find or create yoga pose images
- How to create pixel art in 90s style
- How to properly add files to the project
- Deployment options and GitHub Pages setup

---

## 💡 Tips for Best Experience

1. **Use a dark room** - Neon colors pop more
2. **Adjust volume** - Find your comfort level
3. **Consistent session** - Try 10-30 minute sessions
4. **Mobile + Bluetooth speaker** - Take it anywhere
5. **Add custom poses** - Create your own for variety

---

## 🚀 Future Enhancements

Planned features:
- [ ] More tracks (12-16 total)
- [ ] More yoga poses (16-20 total)
- [ ] Settings menu for customization
- [ ] Session timer with goals
- [ ] Difficulty levels
- [ ] Ambient sound mixing
- [ ] Mobile app (React Native)
- [ ] Breathing guide overlay

---

## 📄 License

MIT License - Feel free to use, modify, and share!

---

## 🙏 Credits

Created with ❤️ for zen and relaxation.

Inspired by:
- 90s video game aesthetics
- Retro CRT displays
- Meditation and yoga traditions
- Cyberpunk neon art

---

## 🧘 Final Thoughts

Whether you're looking to relax, meditate, or just enjoy some retro-aesthetic vibes, Yoga-Zen: 90s Edition is your digital sanctuary. Take a deep breath, press play, and let the neon glow wash over you. ✨

**Namaste** 🙏

---

<div align="center">

**[Get Started Now](#-quick-start)** • **[See Setup Guide](SETUP_GUIDE.md)** • **[View Code](app.js)**

Made with 🧘 & 🎮 in the spirit of relaxation

</div>
