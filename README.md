# Lakshmi Global IT Solutions - Portfolio Website

A professional portfolio website for Lakshmi Global IT Solutions showcasing our services, expertise, and company information.

## 🚀 Live Demo

Visit the live website: `https://bhaskararao-g.github.io/lgis-portfolio/`

## 📋 Features

- Responsive design with Bootstrap 5
- Interactive carousel hero section
- Service showcase sections
- Contact form
- Smooth scrolling navigation
- Mobile-friendly layout
- Professional styling with custom CSS

## 🛠️ Technologies Used

- HTML5
- CSS3
- Bootstrap 5
- Font Awesome Icons
- JavaScript (Vanilla)

## 📂 Project Structure

```
lgis-portfolio/
├── index.html          # Main HTML file
├── styles.css          # Custom CSS styles
├── README.md           # Project documentation
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions deployment workflow
```

## 🚀 Deployment

This website is automatically deployed to GitHub Pages using GitHub Actions.

### Automatic Deployment Setup

The site automatically deploys whenever changes are pushed to the `main` branch.

### Steps to Enable GitHub Pages:

1. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click on **Settings**
   - Scroll down to **Pages** section (in the left sidebar under "Code and automation")
   - Under **Source**, select **GitHub Actions**
   - The deployment workflow will automatically trigger

3. **Access your site:**
   - After deployment completes (usually 1-2 minutes)
   - Your site will be available at: `https://bhaskararao-g.github.io/lgis-portfolio/`

### Manual Deployment Trigger

You can also manually trigger a deployment:
- Go to **Actions** tab in your GitHub repository
- Select the **Deploy to GitHub Pages** workflow
- Click **Run workflow** button

## 🔄 Making Updates

To update the website:

1. Make changes to your files locally
2. Commit and push to the `main` branch:
   ```bash
   git add .
   git commit -m "Update content"
   git push origin main
   ```
3. GitHub Actions will automatically deploy the changes
4. Wait 1-2 minutes for deployment to complete

## 📝 Local Development

To run this website locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/Bhaskararao-G/lgis-portfolio.git
   cd lgis-portfolio
   ```

2. Open `index.html` in your web browser, or use a local server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (http-server)
   npx http-server
   ```

3. Visit `http://localhost:8000` in your browser

## 📧 Contact

For inquiries, please contact:
- Email: info@lakshmiglobalit.com
- Phone: +91 80 1234 5678

## 📄 License

© 2025 Lakshmi Global IT Solutions. All Rights Reserved.

