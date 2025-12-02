# CAD WebGL Viewer

A GPU-accelerated STEP file viewer built with Three.js and WebAssembly. View and interact with 3D CAD models directly in your browser with hardware acceleration.

![STEP Viewer](https://img.shields.io/badge/WebGL-Enabled-brightgreen) ![GPU-Accelerated](https://img.shields.io/badge/GPU-Accelerated-blue) ![Three.js](https://img.shields.io/badge/Three.js-0.160.0-orange)

## ✨ Features

### 🎨 Material Customization
- **5 Material Types**: Normal (Rainbow), Standard PBR, Phong, Lambert, Wireframe
- **Real-time Color Picker**: Change model colors instantly
- **Live Updates**: Material changes apply immediately to loaded models

### 🖱️ CAD-Style Controls
- **Left Mouse**: Rotate model
- **Right Mouse**: Pan view
- **Middle Mouse**: Zoom (dolly)
- **Scroll Wheel**: Zoom in/out
- **Smooth Damping**: Professional-grade camera controls

### 🚀 Performance
- **Hardware Acceleration**: Automatically uses dedicated GPU (NVIDIA/AMD/Intel)
- **Real-time FPS Counter**: Monitor rendering performance
- **GPU Detection**: Displays active GPU vendor and model
- **WebGL 2.0**: Modern graphics pipeline

### 📐 Smart Features
- **Dynamic Grid**: Automatically resizes based on model dimensions
- **Auto Camera Positioning**: Optimal view of loaded models
- **Model Centering**: Centers models at origin for easy manipulation
- **Responsive Design**: Works on any screen size

### 🎨 Modern UI
- **Pink/Magenta Theme**: Beautiful gradient design
- **Glassmorphism Effects**: Frosted glass UI panels
- **Dark Mode**: Easy on the eyes
- **Minimalist Controls**: Clean, intuitive interface

## 🚀 Quick Start

### Online Demo
Simply open `index.html` in a modern browser (Chrome, Firefox, Edge, Safari).

### Local Development
```bash
# Clone the repository
git clone https://github.com/RaghavpravinKS/cad-webgl.git
cd cad-webgl

# Open in browser
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
```

### Using a Local Server (Recommended)
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# Then open http://localhost:8000
```

## 📖 Usage

1. **Load a STEP File**
   - Click "📂 Open STEP File"
   - Select a `.step` or `.stp` file from your computer
   - Wait for parsing (large files may take a moment)

2. **Customize Appearance**
   - Use the **Material** dropdown to change rendering style
   - Click the **Color** picker to change model color
   - Changes apply instantly!

3. **Navigate the Model**
   - **Rotate**: Left-click and drag
   - **Pan**: Right-click and drag
   - **Zoom**: Middle-click drag or scroll wheel

4. **Monitor Performance**
   - Check GPU info in the top-left panel
   - View real-time FPS counter
   - Logs panel shows loading progress

## 🛠️ Technical Stack

- **Three.js** (v0.160.0) - 3D rendering engine
- **OCCT Import JS** (v0.0.16) - STEP file parser (WebAssembly)
- **WebGL 2.0** - Hardware-accelerated graphics
- **ES6 Modules** - Modern JavaScript

## 🎯 Supported File Formats

- `.step` - STEP (Standard for the Exchange of Product Data)
- `.stp` - STEP (alternative extension)

## 🖥️ Browser Compatibility

| Browser | Support | Notes |
|---------|---------|-------|
| Chrome | ✅ Full | Best GPU detection |
| Firefox | ✅ Full | Excellent performance |
| Edge | ✅ Full | Chromium-based |
| Safari | ✅ Full | WebKit support |

**Requirements:**
- WebGL 2.0 support
- ES6 module support
- Modern GPU (dedicated or integrated)

## 🎨 Material Types

### Normal (Rainbow)
Shows surface normals as colors - great for inspecting geometry

### Standard (PBR)
Physically-based rendering with metalness and roughness

### Phong
Classic shiny plastic appearance with specular highlights

### Lambert
Matte, diffuse-only shading

### Wireframe
See the underlying mesh structure

## 🔧 Configuration

The viewer automatically configures itself for optimal performance:
- Requests high-performance GPU
- Enables antialiasing
- Sets appropriate pixel ratio
- Configures CAD-style camera controls

## 📊 Performance Tips

1. **Use Chrome** for best GPU detection
2. **Enable Hardware Acceleration** in browser settings
3. **Close other GPU-intensive apps** for better performance
4. **Use smaller STEP files** for faster loading (< 50MB recommended)

## 🐛 Troubleshooting

### Model not visible
- Check the Logs panel for errors
- Ensure file is a valid STEP format
- Try a smaller test file first

### Low FPS
- Check if hardware acceleration is enabled
- Verify GPU is being used (see GPU Renderer in UI)
- Try Wireframe material for better performance

### GPU shows "WebKit WebGL"
- This is normal for some browsers on `file://` protocol
- Use a local server (`http://localhost`) for accurate GPU detection
- Performance is still hardware-accelerated

## 📝 License

MIT License - feel free to use in your projects!

## 🤝 Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 🙏 Credits

- **Three.js** - 3D rendering
- **OCCT Import JS** - STEP file parsing
- **ANGLE** - WebGL implementation on Windows

---

Made with ❤️ for CAD enthusiasts
