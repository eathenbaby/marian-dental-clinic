# Deployment Guide for New Marian Dental Clinic

## Quick Deploy to Vercel

1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/new-marian-dental-clinic.git
   git push -u origin main
   ```

2. **Deploy on Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will auto-detect Vite and configure build settings
   - Click "Deploy"

## Alternative: Deploy to Netlify

1. **Push to GitHub** (same as above)

2. **Deploy on Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect to GitHub and select your repo
   - Build settings:
     - Build command: `npm run build`
     - Publish directory: `dist`
   - Click "Deploy"

## Backend & Data Handling

### Contact Form Submissions

The contact form currently logs to console. To make it functional:

**Option 1: Use Formspree (Easiest)**
```tsx
// In pages/Contact.tsx, update the form:
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <input type="email" name="email" required />
  <input type="text" name="name" required />
  <textarea name="message" required></textarea>
  <button type="submit">Send</button>
</form>
```

**Option 2: Use Netlify Forms**
```tsx
// Add data-netlify="true" to your form:
<form data-netlify="true" name="contact">
  {/* form fields */}
</form>
```

**Option 3: Custom API**
Create a serverless function in `/api/contact.ts`:
```typescript
export default async function handler(req, res) {
  // Send email using SendGrid, Resend, or similar
  // Store in database if needed
}
```

### Content Management

All clinic data is in `constants.ts`. To update:
- Services, doctors, locations: Edit `constants.ts`
- Images: Replace URLs in constants or upload to `/public` folder
- Commit and push changes - site will auto-redeploy

### Adding a Database (Optional)

For appointment booking or patient records:
1. Use Supabase (free tier available)
2. Add environment variables in Vercel/Netlify
3. Install: `npm install @supabase/supabase-js`
4. Create API routes for CRUD operations

## Environment Variables

If you add backend features, set these in your deployment platform:

- `VITE_FORMSPREE_ID` - For contact form
- `VITE_SUPABASE_URL` - If using Supabase
- `VITE_SUPABASE_KEY` - Supabase anon key

## Custom Domain

After deployment:
1. Go to your project settings
2. Add custom domain (e.g., newmariandental.com)
3. Update DNS records as instructed
4. SSL certificate is auto-generated

## Monitoring

- Vercel/Netlify provide analytics
- Add Google Analytics by including script in `index.html`
- Monitor form submissions via email or dashboard
