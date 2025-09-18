# AI for Peace Statement - Interactive Flashcards

An interactive web application showcasing CMI - Martti Ahtisaari Peace Foundation's principles for responsible AI in peacemaking through engaging flashcards.

## About

This project presents CMI's AI for Peace Statement in an accessible, interactive format. Users can explore six core principles through flipable flashcards that reveal detailed explanations of each principle.

## Features

- **Interactive Flashcards**: Click to flip and explore each principle
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Accessibility**: Keyboard navigation and ARIA labels
- **Modern UI**: Clean, professional design with smooth animations
- **CMI Branding**: Official CMI logo and styling

## Deployment

This project is configured for deployment on Vercel:

### Prerequisites
- Node.js (for local development)
- Vercel CLI (optional, for local testing)

### Deploy to Vercel

1. **Via Vercel Dashboard:**
   - Go to [vercel.com](https://vercel.com)
   - Import this repository
   - Deploy automatically

2. **Via Vercel CLI:**
   ```bash
   npm install -g vercel
   vercel
   ```

3. **Via Git Integration:**
   - Connect your GitHub repository to Vercel
   - Automatic deployments on every push

### Local Development

```bash
# Install dependencies (if any)
npm install

# Serve locally
npx serve .
# or
python -m http.server 8000
# or
php -S localhost:8000
```

## Project Structure

```
├── index.html          # Main HTML file
├── public/
│   └── CMI_25logo.svg  # CMI logo
├── package.json        # Project configuration
├── vercel.json         # Vercel deployment config
└── README.md          # This file
```

## Configuration

The project includes:
- `vercel.json`: Vercel-specific configuration for static site deployment
- `package.json`: Project metadata and scripts
- Security headers for safe deployment
- Optimized caching for static assets

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## License

MIT License - See package.json for details

## About CMI

CMI - Martti Ahtisaari Peace Foundation is an independent, non-governmental organization that works to resolve conflict and build sustainable peace. Founded by Nobel Peace Prize laureate Martti Ahtisaari.

Visit [cmi.fi](https://cmi.fi) for more information.

