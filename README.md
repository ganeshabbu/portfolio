# Abbu Ganesh - AI/ML Developer Portfolio

A modern, responsive portfolio website showcasing AI/ML projects, skills, and experience with dynamic animations and email functionality.

## 🚀 Features

- **Responsive Design** - Works perfectly on all devices
- **Dynamic Animations** - Smooth transitions and interactive elements
- **Email Integration** - Working contact form using EmailJS
- **Project Showcase** - Direct links to GitHub repositories and live demos
- **Skills Visualization** - Animated progress bars and statistics
- **Modern UI/UX** - Glass-morphism effects and gradient designs

## 📧 Email Setup (Required for Contact Form)

To enable the contact form to send emails to your inbox, you need to set up EmailJS:

### Step 1: Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

### Step 2: Create Email Service
1. In your EmailJS dashboard, go to **Email Services**
2. Click **Add New Service**
3. Choose your email provider (Gmail recommended)
4. Follow the setup instructions
5. Note down your **Service ID**

### Step 3: Create Email Template
1. Go to **Email Templates**
2. Click **Create New Template**
3. Use this template content:

```html
Subject: New Portfolio Contact - {{subject}}

Hello Abbu,

You have received a new message from your portfolio website:

Name: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This message was sent from your portfolio contact form.
```

4. Save the template and note down your **Template ID**

### Step 4: Get Public Key
1. Go to **Account** settings
2. Find your **Public Key**
3. Copy it for the next step

### Step 5: Update Configuration
Edit the `script.js` file and update the EMAIL_CONFIG object:

```javascript
const EMAIL_CONFIG = {
    serviceID: 'your_service_id_here',     // Replace with your Service ID
    templateID: 'your_template_id_here',   // Replace with your Template ID
    publicKey: 'your_public_key_here'      // Replace with your Public Key
};
```

## 🛠️ Setup Instructions

1. **Download/Clone the files**
   ```bash
   # If using git
   git clone <repository-url>
   cd portfolio
   ```

2. **Configure Email (See Email Setup section above)**

3. **Open the website**
   - **Simple:** Double-click `index.html`
   - **Recommended:** Use a local server:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Python 2
     python -m SimpleHTTPServer 8000
     
     # Node.js (if you have live-server installed)
     npx live-server
     ```

4. **Access your portfolio**
   - Direct: Open `index.html` in your browser
   - Server: Visit `http://localhost:8000`

## 📁 File Structure

```
portfolio/
├── index.html          # Main HTML file
├── styles.css          # All styling and animations
├── script.js           # JavaScript functionality and EmailJS
└── README.md           # This file
```

## 🎨 Customization

### Colors
Update the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #667eea;      /* Main theme color */
    --secondary-color: #764ba2;    /* Secondary color */
    --accent-color: #f093fb;       /* Accent highlights */
}
```

### Content
- **Personal Info**: Update contact details in `index.html`
- **Projects**: Add/modify project cards in the projects section
- **Skills**: Update skill percentages and categories
- **Experience**: Modify timeline content

### Social Links
Update social media links in the footer section of `index.html`.

## 🌐 Deployment Options

### GitHub Pages (Free)
1. Create a new repository on GitHub
2. Upload all files
3. Go to Settings > Pages
4. Select source branch (main/master)
5. Your site will be available at `username.github.io/repository-name`

### Netlify (Free)
1. Create account at [Netlify.com](https://www.netlify.com/)
2. Drag and drop your portfolio folder
3. Get instant deployment with custom domain options

### Vercel (Free)
1. Create account at [Vercel.com](https://vercel.com/)
2. Connect your GitHub repository
3. Auto-deploy with every push

## 📱 Browser Support

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ IE11+ (limited animation support)

## 🐛 Troubleshooting

### Email Form Not Working
1. Check console for errors (F12 > Console)
2. Verify EmailJS configuration
3. Ensure internet connection for EmailJS API
4. Check EmailJS usage limits (free tier has limits)

### Animations Not Smooth
1. Test on different browsers
2. Check if hardware acceleration is enabled
3. Reduce `particleCount` in `script.js` for better performance

### Mobile Display Issues
1. Test on different devices/screen sizes
2. Check viewport meta tag is present
3. Verify responsive CSS media queries

## 📞 Support

If you need help setting up the portfolio:
- Check the browser console for error messages
- Verify all file paths are correct
- Ensure EmailJS configuration is properly set up

## 🔮 Future Enhancements

- [ ] Blog section integration
- [ ] Dark/Light theme toggle
- [ ] Multi-language support
- [ ] Advanced animations
- [ ] CMS integration
- [ ] Analytics integration

---

**Built with ❤️ by Abbu Ganesh**

*This portfolio showcases modern web development techniques including responsive design, CSS animations, JavaScript interactions, and third-party API integration.*
