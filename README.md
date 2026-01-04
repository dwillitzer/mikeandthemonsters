# Mike and the Monsters - Static Site Backup

## Overview
Complete backup and migration of **mikeandthemonsters.com** from Bandzoogle CMS to static HTML.

This is the official website of Mike and the Monsters - a high-energy party band available for weddings, corporate events, and special occasions in the New York tri-state area.

## Migration Details
- **Original Platform**: Bandzoogle CMS
- **New Format**: Static HTML5/CSS3
- **Content**: Band info, member bios, photos, videos, booking information
- **Status**: Fully functional and deployment-ready

## Quick Start

### View Locally
1. Clone this repository
2. Open `index.html` in any web browser
3. Enjoy the fully functional site!

### Deploy to Web Hosting

#### GitHub Pages (Free, Recommended)
1. This repo is already on GitHub
2. Go to Settings → Pages
3. Source: Deploy from branch
4. Branch: `main` / `root`
5. Save - site will be live at `https://dwillitzer.github.io/mikeandthemonsters/`

#### Netlify (Free, Drag & Drop)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop this entire folder
3. Get instant HTTPS and CDN
4. Custom domain setup available

#### Vercel (Free)
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in this directory
3. Follow prompts for instant deployment

#### GoDaddy / Traditional Hosting
1. Purchase hosting plan
2. Upload all files via:
   - File Manager (cPanel)
   - FTP client (FileZilla)
   - SSH access
3. Upload to `public_html/` or `www/` folder
4. Point domain to new hosting
5. Test all pages and links

#### Yahoo Small Business
1. Sign in to Yahoo Small Business
2. Use File Manager or FTP
3. Upload all files to web root
4. Update DNS settings if needed

## File Structure

```
mikeandthemonsters/
├── index.html              # Main homepage
├── monstervideos.html      # Videos page
├── assets/                 # All site assets
│   ├── css/               # Stylesheets
│   │   └── style.css      # Main responsive styles
│   ├── images/            # Band photos and graphics
│   │   ├── 20160520_123508.jpg (and more)
│   │   ├── Band-Logo-B.png
│   │   ├── Band-Logo-W.png
│   │   ├── header-bg.jpg
│   │   ├── icons/
│   │   │   └── play-icon.png
│   │   └── video-posters/
│   │       └── video-poster-1.jpg
│   └── js/                # JavaScript files
│       └── scripts.js      # Interactive functionality
├── README.md              # This file
└── GITHUB_SETUP.md        # GitHub repository details
```

## Assets

### Images
- **17 band photos** from performances and events
- **Band logos** (white and black versions)
- **Video thumbnails** for embedded content
- **Icons** for UI elements

### CSS Features
- Modern responsive design
- Mobile-friendly layout
- Custom color scheme matching band branding
- Smooth transitions and hover effects

### Content
- Complete band information
- Member biographies
- Photo gallery
- Video showcase (embedded YouTube)
- Contact/booking information
- Social media links

## Customization

### Change Band Info
Edit the content directly in `index.html`:
- Band description
- Member bios
- Contact information
- Song lists

### Update Photos
Replace images in `assets/images/`:
1. Add new images to `assets/images/`
2. Update `src` attributes in HTML
3. Maintain responsive sizing

### Modify Styles
Edit `assets/css/style.css`:
- Color variables at the top
- Layout breakpoints
- Typography settings
- Animation effects

## Deployment Checklist

Before deploying to production:
- [ ] Review all content for accuracy
- [ ] Test all links and buttons
- [ ] Verify contact information
- [ ] Check mobile responsiveness
- [ ] Optimize images (if needed)
- [ ] Set up custom domain (optional)
- [ ] Configure SSL certificate (automatic on most platforms)
- [ ] Test booking/contact form

## Next Steps for Traditional Hosting (GoDaddy/Yahoo)

1. **Purchase Hosting Plan**
   - GoDaddy: Shared hosting (~$3-10/month)
   - Yahoo Small Business: Web hosting plans
   - Any cPanel-based hosting works

2. **Upload Files**
   - Option A: Use hosting control panel's File Manager
   - Option B: FTP with FileZilla (use hosting credentials)
   - Option C: SSH access for advanced users

3. **Configure Domain**
   - Log into domain registrar (currently Bandzoogle)
   - Update nameservers to hosting provider
   - Or update DNS A record to hosting IP
   - Wait 24-48 hours for propagation

4. **Test Everything**
   - Visit main domain
   - Check all subpages
   - Test contact forms
   - Verify on mobile devices

5. **Set Up Email (Optional)**
   - Create email accounts via hosting control panel
   - Configure email clients
   - Set up forwarders if needed

## Performance Optimization

The site is already optimized with:
- Lightweight CSS
- Optimized images
- Minimal JavaScript
- Fast loading times

For even better performance:
- Enable Gzip compression on hosting
- Use CDN for static assets
- Implement browser caching
- Consider lazy loading for images

## Support

### For GitHub Issues
If you find issues with the static site:
1. Check GitHub Issues
2. Create new issue with details
3. Include browser and device info

### For Hosting Support
- **GitHub Pages**: [GitHub Support](https://support.github.com)
- **Netlify**: [Netlify Support](https://www.netlify.com/support/)
- **GoDaddy**: [GoDaddy Support](https://godaddy.com/support)
- **Yahoo**: [Yahoo Small Business Support](https://smallbusiness.yahoo.com/help)

## License

This is the official website of Mike and the Monsters. All content, images, and media are property of the band.

---

**Backup Created**: January 4, 2026
**Original Site**: https://mikeandthemonsters.com
**Platform**: Bandzoogle CMS → Static HTML
**Status**: Deployment Ready

---

## Quick Links

- **View Site**: Open `index.html` in browser
- **GitHub Repo**: https://github.com/dwillitzer/mikeandthemonsters
- **Issue Tracker**: https://github.com/dwillitzer/mikeandthemonsters/issues

---

**Need Help Deploying?**
- For free hosting: Use GitHub Pages or Netlify
- For custom domain: Purchase from any registrar
- For professional hosting: GoDaddy, Bluehost, SiteGround
