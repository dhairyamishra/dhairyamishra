# 🚀 GitHub Profile README Setup Guide

This guide will help you deploy your dynamic GitHub profile README with all features enabled.

## 📋 Prerequisites

- GitHub account (obviously! 😄)
- WakaTime account (for coding stats)
- Git installed locally

---

## 🔧 Step-by-Step Setup

### **Step 1: Repository Setup**

This repository is already named `dhairyamishra` (matching your GitHub username), which makes it a special profile README repo.

1. ✅ Repository is created
2. ✅ Files are in place
3. **Next:** Push to GitHub

```bash
git add .
git commit -m "feat: add comprehensive GitHub profile README with dynamic content"
git push origin main
```

---

### **Step 2: Enable GitHub Actions Permissions**

For the workflows to update your README automatically, you need to grant write permissions:

1. Go to your repository on GitHub: `https://github.com/dhairyamishra/dhairyamishra`
2. Click **Settings** (top right)
3. In the left sidebar, click **Actions** → **General**
4. Scroll to **Workflow permissions**
5. Select **"Read and write permissions"**
6. Check **"Allow GitHub Actions to create and approve pull requests"**
7. Click **Save**

📚 **Reference:** [GitHub Docs - Workflow Permissions](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#setting-the-permissions-of-the-github_token-for-your-repository)

---

### **Step 3: Set Up WakaTime (Coding Activity Stats)**

#### 3.1 Create WakaTime Account
1. Go to [wakatime.com](https://wakatime.com)
2. Sign up (free account is fine)
3. Install WakaTime plugin in your IDE(s):
   - **VS Code:** Search "WakaTime" in extensions
   - **PyCharm/IntelliJ:** Settings → Plugins → Search "WakaTime"
   - **Other IDEs:** Check [WakaTime Plugins](https://wakatime.com/plugins)

#### 3.2 Get Your WakaTime API Key
1. Go to [WakaTime Settings](https://wakatime.com/settings/account)
2. Scroll to **API Key** section
3. Copy your API key (keep it secret!)

#### 3.3 Add API Key to GitHub Secrets
1. Go to your GitHub repo: `https://github.com/dhairyamishra/dhairyamishra`
2. Click **Settings** → **Secrets and variables** → **Actions**
3. Click **New repository secret**
4. Name: `WAKATIME_API_KEY`
5. Value: Paste your WakaTime API key
6. Click **Add secret**

📚 **Reference:** [WakaTime GitHub Action Docs](https://github.com/athul/waka-readme)

---

### **Step 4: Update Personal Information**

Edit `README.md` and replace placeholders:

```markdown
# Line 24: Update contact links
📫 **Get in touch:** [Email](mailto:YOUR_EMAIL@example.com) • [LinkedIn](https://linkedin.com/in/YOUR_PROFILE) • [Website](https://YOUR_WEBSITE.com)

# Lines 129-131: Update footer links
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL@example.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![Website](https://img.shields.io/badge/Website-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://YOUR_WEBSITE.com)
```

---

### **Step 5: Trigger Workflows**

After pushing to GitHub and setting up permissions:

1. Go to **Actions** tab in your repo
2. You'll see three workflows:
   - **Update README with Recent Activity**
   - **Update README with WakaTime Stats**
   - **Generate Snake Contribution Graph**

3. Click on each workflow and click **"Run workflow"** → **"Run workflow"** button

**Note:** The first run might take a few minutes. Subsequent runs are automatic based on the schedule.

---

## 🎨 Customization Options

### **Change Color Theme**

The profile uses the `tokyonight` theme. You can change it to:
- `dark`, `radical`, `merko`, `gruvbox`, `tokyonight`, `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dracula`

Replace `theme=tokyonight` in lines 91-96 of README.md

### **Adjust Update Frequency**

Edit the `cron` schedules in `.github/workflows/`:
- **activity.yml**: Currently every 2 hours (`0 */2 * * *`)
- **wakatime.yml**: Daily at midnight (`0 0 * * *`)
- **snake.yml**: Daily at midnight (`0 0 * * *`)

📚 **Cron Reference:** [Crontab Guru](https://crontab.guru/)

### **Hide Specific Stats**

In the GitHub Stats Card (line 91), you can add parameters:
```markdown
&hide=issues,contribs  # Hide issues and contributions
&show_icons=true       # Show icons
&include_all_commits=true  # Include all commits
```

📚 **Reference:** [GitHub Readme Stats Docs](https://github.com/anuraghazra/github-readme-stats)

---

## 🐛 Troubleshooting

### **Workflows Not Running**
- ✅ Check workflow permissions (Step 2)
- ✅ Ensure `WAKATIME_API_KEY` secret is set correctly
- ✅ Check Actions tab for error messages

### **Stats Cards Not Loading**
- ⏳ Cards are cached (24h for stats, 6 days for languages)
- 🔄 Wait a few hours after first push
- 🔗 Check if URLs are correct (username = `dhairyamishra`)

### **Snake Not Appearing**
- ⏳ First run creates an `output` branch
- 🔄 Wait for workflow to complete (check Actions tab)
- 📝 Snake appears after successful workflow run

### **WakaTime Stats Empty**
- ⏳ Need at least 1 day of coding activity tracked
- 🔌 Ensure WakaTime plugin is active in your IDE
- 🔑 Verify API key is correct in GitHub secrets

---

## 📊 What Each Section Does

| Section | Type | Update Frequency | Requires Setup |
|---------|------|------------------|----------------|
| Banner | Static | Manual | ✅ Done |
| About Me | Static | Manual | ✅ Done |
| Tech Stack Badges | Static | Manual | ✅ Done |
| Featured Projects | Dynamic (cached) | ~24h | ✅ Done |
| GitHub Stats | Dynamic (cached) | ~24h | ✅ Done |
| Streak Stats | Dynamic (cached) | Daily | ✅ Done |
| Top Languages | Dynamic (cached) | ~6 days | ✅ Done |
| WakaTime Stats | Dynamic (Action) | Daily | ⚙️ Needs API key |
| Recent Activity | Dynamic (Action) | Every 2h | ✅ Auto |
| Contribution Snake | Dynamic (Action) | Daily | ✅ Auto |
| Visitor Counter | Dynamic (live) | Real-time | ✅ Done |

---

## 🎯 Next Steps

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "feat: add comprehensive GitHub profile README"
   git push origin main
   ```

2. **Enable workflow permissions** (Step 2)

3. **Set up WakaTime** (Step 3)

4. **Update personal links** (Step 4)

5. **Trigger workflows manually** (Step 5)

6. **Wait 5-10 minutes** and check your profile: `https://github.com/dhairyamishra`

---

## 📚 Resources

- [GitHub Profile README Guide](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
- [GitHub Streak Stats](https://github.com/DenverCoder1/github-readme-streak-stats)
- [WakaTime](https://wakatime.com)
- [Shields.io Badges](https://shields.io)
- [Simple Icons](https://simpleicons.org)

---

## ✨ Tips for Maximum Impact

1. **Keep it updated:** Regularly update your "Currently working on" section
2. **Pin best repos:** Make sure your top 4-6 repos are pinned on your profile
3. **Write good READMEs:** Each project should have a comprehensive README
4. **Stay active:** Consistent contributions = better stats
5. **Engage:** Star, fork, and contribute to interesting projects

---

**Questions?** Check the [GitHub Discussions](https://github.com/dhairyamishra/dhairyamishra/discussions) or open an issue!

Good luck! 🚀
