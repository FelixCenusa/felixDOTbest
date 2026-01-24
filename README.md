# Personal Link Hub

A minimal, self-contained single-page website featuring a parallax starfield background and smooth animations. Built with vanilla HTML/CSS/JavaScript - no frameworks, no build steps, no external dependencies.

## Features

- **Parallax Star Background** - Three-layer animated starfield with responsive performance optimization
- **Profile Photo Popup** - Click to expand with bio information
- **Rotating Messages** - Customizable motivational messages that fade in/out
- **Copy Email Button** - One-click clipboard copy with confirmation toast
- **Responsive Design** - Optimized for all screen sizes (320px to 4K+)
- **Light/Dark Mode** - Automatic theme switching based on system preference
- **Accessibility** - Semantic HTML, keyboard navigation, proper ARIA labels
- **Link Analytics** - Console logging for click tracking (easily replaceable with real analytics)

## Customization

All customization can be done by editing `index.html`:

### Personal Information
- **Profile picture**: Update the GitHub avatar URL (line 6 for favicon, lines throughout for images)
- **Name & title**: Edit the `<h1>` and `.subtitle` elements
- **Bio text**: Modify the popup paragraph content
- **Links**: Update href values in the `<nav>` section

### Rotating Messages
Find the `MESSAGES` array in the JavaScript section:
```javascript
const MSG_INTERVAL=8000; // Change rotation speed (milliseconds)
const MESSAGES=[
'Keep building 🚀',
// Add or modify messages here
];
```

### Colors
Modify CSS variables in the `:root` selector:
```css
:root{
  --bg:#0d0d1a;        /* Background color */
  --text:#e6edf3;      /* Text color */
  --portal3:#581c87;   /* Accent color */
  /* ... more variables */
}
```

### Star Count
Adjust star density in the JavaScript (affects performance on mobile):
```javascript
const d=[700,200,100]; // Desktop: [layer1, layer2, layer3]
if(window.innerWidth<768)d[0]=400,d[1]=100,d[2]=50; // Mobile
```

## Deployment

### GitHub Pages
1. Push to a GitHub repository
2. Go to Settings → Pages
3. Select branch and root folder
4. Your site will be live at `https://username.github.io/repo-name`

### Netlify/Vercel
Simply drag and drop the `index.html` file, or connect your Git repository.

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## License

MIT License - feel free to use and modify for your own projects.
