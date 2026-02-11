# Push to New GitHub Repository

Follow these steps to push your code to a new GitHub repository:

## Step 1: Create a New Repository on GitHub

1. Go to https://github.com/new
2. Repository name: `new-marian-dental-clinic` (or your preferred name)
3. Description: "Modern website for New Marian Dental Clinic"
4. Choose: Private or Public
5. **DO NOT** initialize with README, .gitignore, or license
6. Click "Create repository"

## Step 2: Push Your Code

Open your terminal in this project folder and run:

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: New Marian Dental Clinic website"

# Add your GitHub repository as remote
# Replace YOUR_USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR_USERNAME/new-marian-dental-clinic.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Deploy to Vercel (Recommended)

1. Go to https://vercel.com
2. Sign in with GitHub
3. Click "New Project"
4. Import your `new-marian-dental-clinic` repository
5. Vercel will auto-detect Vite settings
6. Click "Deploy"
7. Your site will be live in ~2 minutes!

## Step 4: Deploy to Netlify (Alternative)

1. Go to https://netlify.com
2. Sign in with GitHub
3. Click "Add new site" → "Import an existing project"
4. Select your repository
5. Build settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Click "Deploy site"

## Troubleshooting

### If you get "remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/new-marian-dental-clinic.git
```

### If you need to update your code later
```bash
git add .
git commit -m "Description of your changes"
git push
```

## Next Steps After Deployment

1. **Custom Domain**: Add your domain in Vercel/Netlify settings
2. **Analytics**: Add Google Analytics code to `index.html`
3. **Backend**: Set up Formspree or API endpoints for contact form
4. **SEO**: Update meta tags in `index.html`

Your site will auto-deploy whenever you push changes to GitHub!
