# GitHub Repository Setup

## Repository Information

**Repository**: mikeandthemonsters
**Owner**: dwillitzer
**Visibility**: Public
**Created**: January 4, 2026
**Status**: Live and Active

## Repository URLs

### HTTPS (Recommended)
```
https://github.com/dwillitzer/mikeandthemonsters.git
```

### SSH
```
git@github.com:dwillitzer/mikeandthemonsters.git
```

### GitHub CLI
```bash
gh repo view dwillitzer/mikeandthemonsters
```

## Quick Access Links

- **Repository**: https://github.com/dwillitzer/mikeandthemonsters
- **Issues**: https://github.com/dwillitzer/mikeandthemonsters/issues
- **Pull Requests**: https://github.com/dwillitzer/mikeandthemonsters/pulls
- **Actions**: https://github.com/dwillitzer/mikeandthemonsters/actions
- **Settings**: https://github.com/dwillitzer/mikeandthemonsters/settings

## GitHub Pages Setup

### Option 1: Automatic GitHub Pages (Free Hosting)

1. **Enable GitHub Pages**:
   - Go to: https://github.com/dwillitzer/mikeandthemonsters/settings/pages
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/ (root)`
   - Click Save

2. **Access Your Site**:
   - URL will be: `https://dwillitzer.github.io/mikeandthemonsters/`
   - Takes 1-2 minutes to deploy initially
   - Auto-updates on every push to `main` branch

3. **Custom Domain (Optional)**:
   - Add `CNAME` file in root with domain name
   - Update DNS at domain registrar
   - Enable HTTPS in GitHub Pages settings
   - Full guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

### Option 2: GitHub Actions for Deployment

For advanced deployment automation:

```yaml
# .github/workflows/deploy.yml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/configure-pages@v3
      - uses: actions/upload-pages-artifact@v2
        with:
          path: '.'
      - uses: actions/deploy-pages@v2
```

## Local Repository Management

### Clone Repository
```bash
# HTTPS
git clone https://github.com/dwillitzer/mikeandthemonsters.git

# SSH
git clone git@github.com:dwillitzer/mikeandthemonsters.git

# With GitHub CLI
gh repo clone dwillitzer/mikeandthemonsters
```

### Push Updates
```bash
# After making changes locally
git add .
git commit -m "Update site content"
git push origin main
```

### Pull Latest Changes
```bash
git pull origin main
```

## GitHub CLI Commands

### Repository Management
```bash
# View repository
gh repo view

# View repository in browser
gh repo view --web

# Create issue
gh issue create --title "Bug report" --body "Description"

# List issues
gh issue list

# Create pull request
gh pr create --title "Update content" --body "Changes made"
```

### Repository Settings
```bash
# Update description
gh repo edit --description "Mike and the Monsters - Party Band Website"

# Add topics
gh repo edit --add-topic "website" --add-topic "music" --add-topic "band"

# Change visibility
gh repo edit --visibility public
```

## Deployment Workflow

### Making Updates

1. **Local Changes**:
   ```bash
   cd /path/to/mikeandthemonsters
   # Edit files
   git add .
   git commit -m "Descriptive commit message"
   git push origin main
   ```

2. **Automatic Deploy**:
   - If GitHub Pages is enabled: Site updates automatically in 1-2 minutes
   - Check Actions tab for deployment status

3. **Verify Deployment**:
   ```bash
   # Open in browser
   gh repo view --web
   ```

### Branching for Updates

For safer updates, use branches:

```bash
# Create new branch
git checkout -b update-content

# Make changes and commit
git add .
git commit -m "Update band photos"

# Push branch
git push origin update-content

# Create pull request
gh pr create --title "Update band photos" --body "Updated photo gallery"

# After review, merge and deploy
```

## Collaboration

### Adding Collaborators
1. Go to Settings → Collaborators
2. Add people by username
3. Choose permission level (Write, Admin, Maintain)

### Issue Templates

Create `.github/ISSUE_TEMPLATE/bug_report.md`:
```markdown
---
name: Bug report
about: Report a problem with the website
title: '[BUG] '
labels: bug
---

**Describe the bug**
A clear description of what the problem is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'

**Expected behavior**
What should happen.

**Screenshots**
If applicable, add screenshots.

**Browser and device info**
 - Browser: [e.g. Chrome, Safari]
 - Device: [e.g. iPhone, Laptop]
```

## Backup and Security

### Repository Backup

GitHub already provides backup, but for extra safety:

```bash
# Create bare backup
git clone --bare https://github.com/dwillitzer/mikeandthemonsters.git mikeandthemonsters-backup.git

# Or mirror to another location
git clone --mirror https://github.com/dwillitzer/mikeandthemonsters.git
```

### Security Best Practices

1. **Don't commit sensitive data**:
   - No API keys
   - No passwords
   - No personal emails (unless intended)

2. **Use .gitignore** (if needed):
   ```
   # OS files
   .DS_Store
   Thumbs.db

   # Editor files
   .vscode/
   .idea/
   *.swp
   ```

3. **Regular updates**:
   - Keep repository active
   - Merge security updates
   - Review access logs

## Monitoring and Analytics

### GitHub Traffic

View repository traffic:
- Go to Insights → Traffic
- See views and clones
- Track popular content

### External Analytics

Add analytics to site:

**Google Analytics**:
1. Create GA4 property
2. Add tracking script to `index.html`
3. Paste before `</head>`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## Common Tasks

### Update Content
```bash
# Edit files locally
git add .
git commit -m "Update content"
git push origin main
```

### Add New Images
```bash
# Add to assets/images/
git add assets/images/new-image.jpg
git commit -m "Add new photo"
git push origin main
```

### Change Styles
```bash
# Edit assets/css/style.css
git add assets/css/style.css
git commit -m "Update styling"
git push origin main
```

### Revert Changes
```bash
# View recent commits
git log --oneline

# Revert to specific commit
git revert <commit-hash>
git push origin main
```

## Resources

- **GitHub Docs**: https://docs.github.com
- **GitHub Pages Docs**: https://docs.github.com/en/pages
- **GitHub CLI Docs**: https://cli.github.com/manual/
- **Git Handbook**: https://guides.github.com/introduction/git-handbook/

## Support

For issues with:
- **Git**: https://git-scm.com/docs
- **GitHub**: https://support.github.com
- **GitHub Pages**: https://docs.github.com/en/pages

---

**Last Updated**: January 4, 2026
**Repository Status**: Active
**Deployment**: GitHub Pages Ready
