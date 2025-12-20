# 📝 Quick Reference Guide

## 🚀 Deployment Checklist

- [ ] Push all files to GitHub
- [ ] Enable workflow write permissions (Settings → Actions → General)
- [ ] Add `WAKATIME_API_KEY` to repository secrets
- [ ] Update email/LinkedIn/website links in README.md
- [ ] Manually trigger all workflows once
- [ ] Wait 5-10 minutes for initial setup
- [ ] Visit `https://github.com/dhairyamishra` to see your profile!

---

## 🔗 Important Links to Update

**In README.md:**
- Line 24: Email, LinkedIn, Website
- Lines 129-131: Footer contact badges

**Replace:**
- `your.email@example.com` → Your actual email
- `yourprofile` → Your LinkedIn username
- `yourwebsite.com` → Your website URL

---

## 🎨 Quick Customizations

### Change Theme
Replace `theme=tokyonight` with:
- `dark` | `radical` | `merko` | `gruvbox` | `onedark` | `cobalt` | `synthwave` | `dracula`

### Badge Colors
Current: Various colors (Python=blue, PyTorch=red, etc.)
Change hex codes in badge URLs: `badge/NAME-HEXCOLOR?style=...`

### Update Frequency
Edit cron schedules in `.github/workflows/`:
- `0 */2 * * *` = Every 2 hours
- `0 0 * * *` = Daily at midnight
- `0 */6 * * *` = Every 6 hours

---

## 📊 What Updates Automatically

| Feature | Updates | Frequency |
|---------|---------|-----------|
| GitHub Stats | ✅ Auto | ~24 hours (cached) |
| Streak Stats | ✅ Auto | Daily (cached) |
| Top Languages | ✅ Auto | ~6 days (cached) |
| WakaTime | ✅ Auto | Daily via workflow |
| Recent Activity | ✅ Auto | Every 2 hours via workflow |
| Snake Animation | ✅ Auto | Daily via workflow |
| Visitor Count | ✅ Auto | Real-time |

---

## 🛠️ Common Commands

```bash
# Check status
git status

# Add all changes
git add .

# Commit with message
git commit -m "update: description of changes"

# Push to GitHub
git push origin main

# Pull latest changes
git pull origin main
```

---

## 🐛 Quick Fixes

### Stats not showing?
- Wait 24 hours (caching)
- Check username is correct: `dhairyamishra`
- Verify repo is public

### Workflows failing?
- Check Actions tab for errors
- Verify workflow permissions enabled
- Ensure `WAKATIME_API_KEY` is set

### Snake not appearing?
- Wait for first workflow run to complete
- Check Actions tab → "Generate Snake"
- Verify `output` branch was created

---

## 📱 File Structure

```
dhairyamishra/
├── README.md                    # Main profile (what people see)
├── SETUP_GUIDE.md              # Detailed setup instructions
├── QUICK_REFERENCE.md          # This file
├── assets/
│   ├── banner-light.svg        # Light mode banner
│   ├── banner-dark.svg         # Dark mode banner
│   └── icons/                  # (optional) custom icons
└── .github/
    └── workflows/
        ├── activity.yml        # Recent activity updater
        ├── wakatime.yml        # WakaTime stats updater
        └── snake.yml           # Contribution snake generator
```

---

## 🎯 Next Actions

1. **Now:** Update personal links in README.md
2. **Then:** Push to GitHub
3. **After:** Set up WakaTime API key
4. **Finally:** Trigger workflows and enjoy!

---

## 💡 Pro Tips

- Keep "Currently working on" section fresh
- Update featured projects as you build new ones
- Commit regularly for better contribution graph
- Use meaningful commit messages
- Pin your best 6 repos on GitHub profile

---

**Need help?** Check `SETUP_GUIDE.md` for detailed instructions!
