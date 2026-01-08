# 🚀 GitHub Profile README Setup Guide

This guide will help you deploy your minimalist GitHub profile README with snake animation.

## 📋 Prerequisites

- GitHub account
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
git commit -m "feat: add minimalist GitHub profile with snake animation"
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

### **Step 3: Trigger Workflows**

After pushing to GitHub and setting up permissions:

1. Go to **Actions** tab in your repo
2. You'll see two workflows:
   - **Update README with Recent Activity**
   - **Generate Snake Contribution Graph**

3. Click on each workflow and click **"Run workflow"** → **"Run workflow"** button

**Note:** The first run might take a few minutes. Subsequent runs are automatic based on the schedule.

---

## 🎨 Customization Options

### **Adjust Update Frequency**

Edit the `cron` schedules in `.github/workflows/`:
- **activity.yml**: Currently every 2 hours (`0 */2 * * *`)
- **snake.yml**: Daily at midnight (`0 0 * * *`)

📚 **Cron Reference:** [Crontab Guru](https://crontab.guru/)

---

## 🐛 Troubleshooting

### **Workflows Not Running**
- ✅ Check workflow permissions (Step 2)
- ✅ Check Actions tab for error messages

### **Snake Not Appearing**
- ⏳ First run creates an `output` branch
- 🔄 Wait for workflow to complete (check Actions tab)
- 📝 Snake appears after successful workflow run

---

## 📊 What Each Section Does

| Section | Type | Update Frequency | Requires Setup |
|---------|------|------------------|----------------|
| Recent Activity | Dynamic (Action) | Every 2h | ✅ Auto |
| Contribution Snake | Dynamic (Action) | Daily | ✅ Auto |

---

## 🎯 Next Steps

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "feat: add minimalist GitHub profile with snake animation"
   git push origin main
   ```

2. **Enable workflow permissions** (Step 2)

3. **Trigger workflows manually** (Step 3)

4. **Wait 5-10 minutes** and check your profile: `https://github.com/dhairyamishra`

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

1. **Stay active:** Consistent contributions = better snake animation
2. **Pin best repos:** Make sure your top repos are pinned on your profile
3. **Write good READMEs:** Each project should have a comprehensive README

---

**Questions?** Check the [GitHub Discussions](https://github.com/dhairyamishra/dhairyamishra/discussions) or open an issue!

Good luck! 🚀
