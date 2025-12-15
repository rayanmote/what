# What-If Question Platform

## Description

The What-If Question Platform is an interactive web application designed to foster creativity, critical thinking, and intellectual curiosity among students. It provides a space where users can explore hypothetical scenarios across various disciplines including science, technology, history, philosophy, and more.

## Features

- **User Authentication**: Secure login and signup system for students
- **Question Management**: Post, browse, and search through "what-if" questions
- **Categorization**: Organize questions by topics for easy navigation
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Interactive UI**: Engaging animations and user-friendly interface

## Pages

- **Home (index.html)**: Landing page with hero section and navigation
- **About Us (about.html)**: Information about the platform with statistics
- **Features (features.html)**: Detailed platform features with interactive cards
- **Browse Questions (browse.html)**: Search and browse published questions
- **Contact Us (contact.html)**: Contact form and information
- **Login (login.html)**: Student login page
- **Signup (signup.html)**: Student registration page
- **Dashboard (dashboard.html)**: Student dashboard (requires login)

## Files Included

- **HTML Files**: `index.html`, `about.html`, `features.html`, `browse.html`, `contact.html`, `login.html`, `signup.html`, `dashboard.html`
- **CSS**: `css/style.css`, `css/auth.css`
- **JavaScript**: `js/main.js`
- **Assets**: `assets/` (images and additional resources)
- **Configuration**: `netlify.toml` (for Netlify deployment)
- **Documentation**: `README.md`

## Installation

1. Clone or download the project files
2. Place the `what` folder in your web server's root directory (e.g., WAMP's www folder)
3. Start your web server
4. Navigate to `http://localhost/what/` in your browser

## Usage

1. Visit the home page to explore the platform
2. Sign up for a new account or login with existing credentials
3. Browse questions or ask your own "what-if" questions
4. Use the search functionality to find specific topics
5. Contact us through the contact form for feedback

## Sample Data

The platform comes with pre-loaded sample questions and user accounts for demonstration:

- **Sample Students**: student1/student123, student2/student123, etc.

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Contributing

This is an educational project. Feel free to fork and modify for learning purposes.

## License

© 2023 What-If Platform by Ray Airo R. Bapora. All rights reserved.

## Hosting

### Option 1: GitHub Pages (Free)

1. **Create a GitHub Repository**:
   - Go to [GitHub.com](https://github.com) and create a new repository
   - Name it something like `what-if-platform`
   - Make it public

2. **Upload Your Files**:
   - Upload all files from your `what` folder to the repository
   - Or clone the repository and copy files there

3. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll down to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Select "main" branch and "/ (root)" folder
   - Click "Save"

4. **Access Your Site**:
   - GitHub will provide a URL like: `https://yourusername.github.io/what-if-platform/`
   - It may take a few minutes to deploy

### Option 2: Netlify (Free)

1. **Sign up for Netlify**:
   - Go to [netlify.com](https://netlify.com) and sign up

2. **Deploy**:
   - Drag and drop your entire `what` folder onto the Netlify dashboard
   - Or connect your GitHub repository

3. **Configuration**:
   - The `netlify.toml` file is included and will automatically configure:
     - Publish directory: root (`./`)
     - No build command needed
     - Proper redirects for static site

4. **Get Your URL**:
   - Netlify will provide a random URL like `https://random-name.netlify.app`

#### Netlify Configuration Details

A `netlify.toml` file has been added to your project with the correct settings:

```toml
[build]
  publish = "."
  command = "echo 'No build step required'"

[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200
```

This ensures Netlify serves your static HTML files correctly.

#### Netlify Troubleshooting 404 Errors

If you're getting a 404 error on Netlify:

1. **Check the netlify.toml file**:
   - Ensure `netlify.toml` is uploaded with your files
   - It should contain: `publish = "."`

2. **Publish Directory**:
   - In Netlify dashboard → Site settings → Build & deploy → Publish directory
   - Should be `./` (automatically set by netlify.toml)

3. **File Structure**:
   - All HTML files should be in the root directory
   - `index.html` should be in the root

4. **URL Access**:
   - Root: `https://yoursite.netlify.app/` (serves index.html)
   - Pages: `https://yoursite.netlify.app/about.html`

5. **Redeploy**:
   - Go to Deploys tab → Trigger deploy
   - The netlify.toml file will be automatically detected

**The netlify.toml file handles all the configuration automatically - just make sure it's uploaded with your files!**

### Option 3: Vercel (Free) - Step-by-Step Guide

Vercel is a fast and reliable platform for deploying static websites and frontend applications.

#### Method 1: Deploy via Vercel Dashboard (Easiest)

1. **Sign up for Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Click "Sign Up" and create an account (GitHub, GitLab, or email)
   - Verify your email if needed

2. **Deploy Your Project**:
   - On the Vercel dashboard, click "New Project"
   - Choose "Import Git Repository" if you have GitHub, or "Deploy with Git" for other options
   - If no Git repository, select "Import Third-Party Git Repository" or use drag-and-drop

3. **Upload Files (Alternative)**:
   - If using drag-and-drop: Simply drag your entire `what` folder onto the deployment area
   - Vercel will automatically detect it as a static site

4. **Configure Deployment**:
   - **Framework Preset**: Select "Other" or "HTML"
   - **Root Directory**: Leave as `./` (root)
   - **Build Command**: Leave empty (no build needed)
   - **Output Directory**: Leave empty (static files)

5. **Deploy**:
   - Click "Deploy"
   - Wait for the build process (usually 30 seconds - 2 minutes)
   - You'll get a preview URL like `https://your-project-name.vercel.app`

#### Method 2: Deploy via Vercel CLI

1. **Install Vercel CLI**:
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**:
   ```bash
   vercel login
   ```
   Follow the prompts to authenticate

3. **Navigate to Your Project**:
   ```bash
   cd /path/to/your/what/folder
   ```

4. **Deploy**:
   ```bash
   vercel
   ```
   - Answer the prompts:
     - Set up and deploy? → Y
     - Which scope? → Your account
     - Link to existing project? → N
     - Project name → what-if-platform (or your choice)
     - In which directory is your code located? → ./ (current directory)

5. **Production Deployment**:
   ```bash
   vercel --prod
   ```

#### Vercel Configuration (Optional)

For static sites like yours, you typically **don't need** a `vercel.json` file. Vercel will automatically detect and serve your HTML, CSS, and JS files.

If you're getting the warning about `builds` configuration, either:
- Delete the `vercel.json` file from your project
- Or use this minimal configuration:

```json
{
  "version": 2,
  "name": "what-if-platform"
}
```

**Remove the `builds` section** as it's not needed for static sites and causes the warning.

#### Custom Domain (Optional)

1. Go to your project settings in Vercel dashboard
2. Navigate to "Domains"
3. Add your custom domain
4. Configure DNS records as instructed

#### Testing Your Vercel Deployment

- Visit the provided URL
- Test all pages: Home, About, Features, Browse, Contact, Login, Signup
- Verify search functionality works
- Check responsive design on mobile

#### Vercel Features for Your Project

- **Automatic HTTPS**: SSL certificate included
- **Global CDN**: Fast loading worldwide
- **Custom Domains**: Connect your own domain
- **Analytics**: Built-in performance monitoring
- **Environment Variables**: For future backend integration

Vercel is excellent for static sites like yours and provides great performance out of the box!

#### Troubleshooting 404 Errors

If you're getting a 404 error after deployment, try these solutions:

1. **Check Your Root Directory**:
   - In Vercel dashboard → Project Settings → General → Root Directory
   - Make sure it's set to `./` or empty

2. **Framework Preset**:
   - In project settings, set Framework Preset to "Other" or "HTML"
   - Build Command: leave empty
   - Output Directory: leave empty

3. **File Structure Check**:
   - Ensure `index.html` is in the root directory of your deployment
   - All HTML files should be in the root: `about.html`, `features.html`, etc.
   - Folders: `css/`, `js/`, `assets/` should be included

4. **Redeploy**:
   - Go to your Vercel dashboard → Your project → Deployments
   - Click the three dots on the latest deployment → "Redeploy"

5. **Check Deployment Logs**:
   - Click on the deployment to see build logs
   - Look for errors or warnings
   - Should show "Build succeeded" for static sites

6. **URL Access**:
   - Root URL: `https://your-project.vercel.app/` (should serve index.html)
   - Other pages: `https://your-project.vercel.app/about.html`
   - Don't forget `.html` extensions for subpages

7. **Alternative: No vercel.json**:
   - If issues persist, try removing the `vercel.json` file entirely
   - Vercel should auto-detect static sites

8. **Fresh Deployment**:
   - Delete the current project in Vercel
   - Create a new project
   - Upload/reconnect your files

9. **Check File Permissions**:
   - Ensure all files are readable (no permission issues)

10. **Browser Cache**:
    - Try incognito mode or clear cache
    - Or try a different browser

The updated `vercel.json` should help. If you're still getting 404, check the deployment logs for specific errors.

- **LocalStorage Limitation**: Since this app uses localStorage for data storage, user accounts and questions won't persist across different browsers or devices. For a production site, you'd need a backend database.

- **File Structure**: Make sure all files maintain their relative paths. The `css/`, `js/`, and `assets/` folders should be uploaded along with the HTML files.

- **Testing**: After hosting, test all pages and functionality to ensure everything works correctly.

- **Domain**: For custom domains, most hosting services allow you to connect your own domain (paid plans usually required).

### Recommended: GitHub Pages for Beginners

GitHub Pages is the easiest option if you're new to web hosting. It integrates well with version control and is completely free for public repositories.

#### How to Delete vercel.json from GitHub:

1. **Go to your GitHub repository**:
   - Open [github.com](https://github.com) in your browser
   - Navigate to your repository (the one connected to Vercel)

2. **Find the vercel.json file**:
   - Look in the file list for `vercel.json`
   - If you don't see it, click "Go to file" and search for it

3. **Delete the file**:
   - Click on `vercel.json` to open it
   - Click the trash can icon (Delete this file) in the top right
   - Add a commit message: "Remove vercel.json to fix Vercel build warning"
   - Click "Commit changes"

4. **Automatic Redeployment**:
   - Since your Vercel project is connected to this GitHub repo, it will automatically redeploy
   - The warning should disappear in the next deployment

**If you can't find vercel.json on GitHub:**
- The file might be in a different repository
- Or it was uploaded directly to Vercel without Git
- In that case, go to Vercel dashboard → Delete project → Create new project → Upload files again</content>
<parameter name="filePath">c:\wamp64\www\what\README.md