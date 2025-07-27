# MarkItUp – Markdown Editor

***MarkItUp** is a lightweight, modern Markdown editor built with Next.js. It features live preview, file storage, dark/light themes, and responsive design — all self-hosted and privacy-respecting.*

![Screenshot](/docs/screenshot.png)

## 🚀 Features

### Markdown Editing

* Real-time editor with syntax highlighting
* GitHub Flavored Markdown (GFM) support
* Split view: edit and preview side by side
* Clean, monospace editing experience

### Theme Support

* Light and dark modes with smooth transitions
* Auto-detects system theme on first load
* Respects system theme preference on first visit

### File Management

* Save/load/delete `.md` files from the `/markdown` directory
* Auto-generated file list with timestamps
* Server-side storage with secure access

### Technical Highlights

* Built with **Next.js 15** and **TypeScript**
* Fully responsive across devices
* Syntax highlighting for code blocks
* Accessible via ARIA labels and keyboard navigation

## 📁 File Structure

```
markitup/
├── markdown/                  # Server-side Markdown file storage
├── public/                    # Static assets
├── src/
│   ├── app/                   # App and API routes
│   ├── components/            # Reusable UI components
│   └── contexts/              # Theme context
├── docker-compose.yml         # Docker Compose configuration
├── Dockerfile                 # Dockerfile for building the image
├── package.json
└── tailwind.config.js
```

## ⚙️ Getting Started

### Requirements

* Node.js 18+
* npm / yarn / pnpm

### Setup

```bash
git clone https://github.com/xclusive36/MarkItUp.git
cd MarkItUp
npm install
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000)

## 🐳 Deployment

### Docker Compose (Recommended)

```bash
# Copy the example compose file
docker compose up -d
```

### Docker CLI

```bash
docker run --name markitup -p 3000:3000 -v ./markdown:/app/markdown --restart unless-stopped -e NODE_ENV=production -e PORT=3000 -e HOSTNAME=0.0.0.0 markitup:latest
```

## 🔐 Security

* File path validation
* Input sanitization
* Basic CORS protection

## 🤝 Contributing

Contributions are welcome via issues or pull requests.

## 📄 License

MIT – see `LICENSE` file for details.
