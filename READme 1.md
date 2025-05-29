# Text Merge Pro 🔗

A simple, efficient web-based tool for merging multiple text files and snippets into a single document. Built with vanilla HTML, CSS, and JavaScript for maximum compatibility and performance.

![Text Merge Pro Screenshot](https://via.placeholder.com/800x400/4A2E4D/FFFFFF?text=Text+Merge+Pro)

## ✨ Features

- **File Selection**: Support for multiple text files (.txt, .md, .csv)
- **Direct Text Input**: Paste or type text directly into the app
- **Custom Separators**: Choose from predefined separators or create custom ones
- **Real-time Preview**: See merged content before downloading
- **Statistics Display**: Track file count, character count, and line count
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Download Functionality**: Save merged content as .txt file
- **Error Handling**: Comprehensive error messages and validation
- **Clean UI**: Modern, intuitive interface with beautiful color scheme

## 🚀 Quick Start

### Option 1: Direct Download
1. Download the `index.html` file
2. Open it in any modern web browser
3. Start merging text files immediately!

### Option 2: Clone Repository
```bash
git clone https://github.com/yourusername/text-merge-pro.git
cd text-merge-pro
```

Open `index.html` in your browser or serve it using a local server.

## 📁 Project Structure

```
text-merge-pro/
├── index.html          # Main application file
├── README.md          # This file
├── LICENSE            # MIT License
└── docs/
    ├── screenshots/   # Application screenshots
    └── deployment/    # Deployment guides
```

## 🛠️ Technology Stack

- **HTML5**: Semantic markup and file handling
- **CSS3**: Modern styling with CSS Grid and Flexbox
- **Vanilla JavaScript**: ES6+ features, File API, Blob API
- **No Dependencies**: Pure web technologies, no frameworks needed

## 🎨 Color Scheme

The application uses a carefully selected color palette:
- **Purple**: `#4A2E4D` - Primary text and buttons
- **Mauve**: `#8B5A8C` - Secondary elements and hover states  
- **Peach**: `#F4C2A1` - Accent colors and borders
- **Cream**: `#F5F5DC` - Background elements and preview areas

## 📖 Usage Guide

### Basic Usage
1. **Select Files**: Click "Choose Text Files" to select multiple .txt, .md, or .csv files
2. **Add Text**: Optionally paste or type additional text in the text input area
3. **Configure**: Choose separator type and output filename
4. **Preview**: Click "Generate Preview" to see the merged result
5. **Download**: Click "Download Merged File" to save the merged content

### Advanced Features
- **Custom Separators**: Select "Custom" separator option and enter your preferred delimiter
- **File Management**: Remove individual files using the × button next to each file
- **Statistics**: Monitor file count, total characters, and lines in real-time
- **Clear Functions**: Use "Clear Files" or "Clear Text" buttons to reset inputs

## 🌐 Deployment Options

### 1. Vercel (Recommended)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Follow prompts to deploy
```

**Alternative: Drag & Drop**
1. Visit [vercel.com](https://vercel.com)
2. Drag your project folder to the deployment area
3. Your app will be live instantly!

### 2. Netlify
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Deploy
netlify deploy --prod --dir .
```

**Alternative: Git Integration**
1. Push code to GitHub
2. Connect repository to Netlify
3. Auto-deploy on every commit

### 3. GitHub Pages
1. Push code to GitHub repository
2. Go to Settings → Pages
3. Select source branch (main/master)
4. Access via `https://yourusername.github.io/text-merge-pro`

### 4. Firebase Hosting
```bash
# Install Firebase CLI
npm install -g firebase-tools

# Initialize
firebase login
firebase init hosting

# Deploy
firebase deploy
```

## 🖥️ VPS Deployment

### Using Nginx
```bash
# Install Nginx
sudo apt update
sudo apt install nginx

# Copy files
sudo cp -r text-merge-pro/* /var/www/html/

# Configure Nginx (optional custom domain)
sudo nano /etc/nginx/sites-available/text-merge-pro

# Restart Nginx
sudo systemctl restart nginx
```

### Using Apache
```bash
# Install Apache
sudo apt update
sudo apt install apache2

# Copy files
sudo cp -r text-merge-pro/* /var/www/html/

# Restart Apache
sudo systemctl restart apache2
```

### Using Docker
```dockerfile
# Dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

```bash
# Build and run
docker build -t text-merge-pro .
docker run -p 80:80 text-merge-pro
```

## 💻 Local Development

### Simple HTTP Server
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server

# PHP
php -S localhost:8000
```

### Live Server (VS Code)
1. Install "Live Server" extension
2. Right-click `index.html`
3. Select "Open with Live Server"

## 🔧 Customization

### Modifying Colors
Update CSS custom properties in the `:root` selector:
```css
:root {
    --purple: #4A2E4D;
    --mauve: #8B5A8C;
    --peach: #F4C2A1;
    --cream: #F5F5DC;
}
```

### Adding File Types
Modify the file input accept attribute:
```html
<input type="file" accept=".txt,.md,.csv,.json,.log" />
```

Update validation in JavaScript:
```javascript
if (file.type === 'text/plain' || 
    file.name.endsWith('.txt') || 
    file.name.endsWith('.md') || 
    file.name.endsWith('.csv') ||
    file.name.endsWith('.json')) {
    // Process file
}
```

## 🐛 Browser Compatibility

- **Chrome**: 60+ ✅
- **Firefox**: 60+ ✅  
- **Safari**: 12+ ✅
- **Edge**: 79+ ✅
- **Mobile Browsers**: iOS Safari 12+, Android Chrome 60+ ✅

## 📱 PWA Enhancement (Optional)

To make it a Progressive Web App, add:

**manifest.json**:
```json
{
  "name": "Text Merge Pro",
  "short_name": "TextMerge",
  "description": "Merge text files efficiently",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#F5F5DC",
  "theme_color": "#4A2E4D",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    }
  ]
}
```

**Service Worker** (basic caching):
```javascript
// sw.js
const CACHE_NAME = 'text-merge-pro-v1';
const urlsToCache = ['/'];

self.addEventListener('install', event => {
  event.waitUntil(
    caches.open(CACHE_NAME)
      .then(cache => cache.addAll(urlsToCache))
  );
});
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🎯 Roadmap

- [ ] Support for .docx and .pdf files
- [ ] Cloud storage integration (Google Drive, Dropbox)
- [ ] Text editing capabilities within the app
- [ ] Batch processing for large file sets
- [ ] Advanced sorting and organization options
- [ ] Export to multiple formats (PDF, Word, etc.)
- [ ] Collaborative editing features
- [ ] API endpoints for programmatic access

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/text-merge-pro/issues) page
2. Create a new issue with detailed information
3. Include browser version and steps to reproduce

## 🏷️ Version History

- **v1.0.0** - Initial release with core merging functionality
- **v1.1.0** - Added custom separators and statistics
- **v1.2.0** - Improved mobile responsiveness and error handling

---

Made with ❤️ for the developer community. Star ⭐ this repo if you find it useful!