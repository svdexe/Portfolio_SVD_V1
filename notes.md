# Portfolio Setup and Customization Notes

## Initial Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/bchiang7/v4.git
   cd v4
   ```

2. **Remove original Git connection**
   ```bash
   # Remove the existing git history
   rm -rf .git
   ```

3. **Initialize as your own Git repository**
   ```bash
   # Initialize a new git repository
   git init
   
   # Add all files to the new repository
   git add .
   
   # Make your initial commit
   git commit -m "Initial commit for my portfolio"
   ```

4. **Connect to your remote repository (when ready)**
   ```bash
   # Replace with your GitHub username and repository name
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   
   # Set the main branch
   git branch -M main
   
   # Push to your GitHub repository
   git push -u origin main
   ```

5. **Install/use the correct Node.js version**
   ```bash
   nvm use 16.20.2  # Using 16.20.2 instead of 14.16.0 due to installation issues
   ```

6. **Install Gatsby CLI globally**
   ```bash
   npm install -g gatsby-cli
   ```

7. **Install Yarn globally**
   ```bash
   npm install -g yarn
   ```

8. **Install dependencies**
   ```bash
   yarn
   ```
   (Alternative: `npm install` if yarn fails)

9. **Start the development server**
   ```bash
   npm start
   ```
   This runs at http://localhost:8000

## Customization Guide

### Content Modification
- Edit files in the `content` folder for different sections:
  - `content/featured/` - Featured projects
  - `content/jobs/` - Work experience
  - `content/projects/` - Other projects
  - `content/about/` - About me section
  - `content/hero/` - Hero section (landing page)
  - `content/contact/` - Contact information

### Visual Customization
- Replace images in the `static` folder
- Update site metadata in `gatsby-config.js`
- Modify colors in `src/styles/theme.js` 
  - Default colors: 
    - Navy `#0a192f`
    - Light Navy `#112240`
    - Lightest Navy `#233554`
    - Slate `#8892b0`
    - Light Slate `#a8b2d1`
    - Lightest Slate `#ccd6f6`
    - White `#e6f1ff`
    - Green `#64ffda`

### Production and Deployment

1. **Build for production**
   ```bash
   npm run build
   ```

2. **Preview the production build**
   ```bash
   npm run serve
   ```

3. **Deployment options**
   - Netlify (original setup)
   - GitHub Pages
   - Vercel
   - Other static site hosting

## Important Reminders

- Remember to give proper attribution to Brittany Chiang by linking back to her site (brittanychiang.com) in your footer
- Keep the MIT license intact
- Update the resume PDF in the `static` folder
- Test on mobile devices before final deployment

## Useful VS Code Extensions

- ESLint
- Prettier
- Gatsby.js
- React Snippets
- Markdown All in One

## Troubleshooting

If you encounter build errors:
1. Check Node.js version compatibility
2. Clear cache: `gatsby clean`
3. Delete node_modules and reinstall: `rm -rf node_modules && yarn`