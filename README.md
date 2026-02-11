# New Marian Dental Clinic Website

A modern, responsive website for New Marian Dental Clinic with smooth scrolling, elegant animations, and a professional design.

## Features

- Smooth scrolling experience with Lenis
- Responsive design for all devices
- Service showcase with detailed information
- Multi-location support
- Contact form with WhatsApp integration
- Gallery section
- Emergency contact banner
- Bilingual support (English/Malayalam)

## Tech Stack

- React 19
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Framer Motion
- Lucide Icons
- Lenis (smooth scroll)

## Getting Started

### Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### Deployment

See [DEPLOYMENT.md](./DEPLOYMENT.md) for detailed deployment instructions.

Quick deploy options:
- **Vercel**: Connect GitHub repo → Auto-deploy
- **Netlify**: Connect GitHub repo → Auto-deploy

## Project Structure

```
├── components/          # Reusable React components
│   ├── Header.tsx
│   ├── Footer.tsx
│   ├── DoctorCard.tsx
│   └── ...
├── pages/              # Page components
│   ├── Home.tsx
│   ├── Contact.tsx
│   └── Gallery.tsx
├── constants.ts        # Clinic data (services, doctors, locations)
├── types.ts           # TypeScript type definitions
├── utils.ts           # Utility functions
└── App.tsx            # Main app component
```

## Customization

### Update Clinic Information

Edit `constants.ts` to update:
- Services offered
- Doctor profiles
- Location details
- Social media links
- Contact information

### Styling

The site uses Tailwind CSS. Color scheme is defined in `index.html`:
- Primary: `#0EA5E9` (Sky Blue)
- CTA: `#10B981` (Green)
- Dark: `#0B1120` (Navy)

### Adding Backend

The contact form currently opens WhatsApp. To add a backend:

1. Create API endpoint (e.g., `/api/appointments`)
2. Uncomment the fetch code in `pages/Contact.tsx`
3. Add environment variables for API keys

See [DEPLOYMENT.md](./DEPLOYMENT.md) for backend integration options.

## Contact

For support or inquiries:
- Phone: +91 88481 98200
- Email: abyjoseph1991@gmail.com
- WhatsApp: [Click here](https://wa.me/918848198200)

## License

Private - All rights reserved by New Marian Dental Clinic
