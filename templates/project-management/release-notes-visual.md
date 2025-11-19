<!-- 
  TEMPLATE: Visual Release Notes
  COMPLEXITY: Medium
  FEATURES: Collapsible sections, Emoji categorization, Visual hierarchy
  USE CASE: Making changelogs engaging for end-users.
-->

# 🚀 Release Notes: v2.0.0 "Nebula"

> **Release Date**: November 19, 2025
> **Build**: `2.0.0-stable`

---

## ✨ Highlights

### 🎨 Dark Mode is Here!
We've completely overhauled the UI to support a system-wide dark theme. It's easier on the eyes and looks stunning on OLED screens.

![Dark Mode Preview](https://via.placeholder.com/800x400/1a1a1a/ffffff?text=Dark+Mode+Preview)

### ⚡ Performance Boost
The rendering engine has been rewritten in Rust. Expect **50% faster load times** on large datasets.

---

## 📋 Detailed Changelog

<details open>
<summary><strong>🆕 New Features</strong></summary>

- **UI**: Added a toggle for "Compact Mode" in settings.
- **API**: New endpoint `GET /v2/stats` for real-time analytics.
- **Auth**: Support for GitHub and Google OAuth login.

</details>

<details>
<summary><strong>🐛 Bug Fixes</strong></summary>

- Fixed a crash when uploading images larger than 5MB.
- Resolved an issue where the sidebar would disappear on mobile.
- Corrected timezone calculation for users in UTC+12.

</details>

<details>
<summary><strong>🛠 Improvements</strong></summary>

- Updated all dependencies to latest versions.
- Improved error messages for 404 pages.
- Added tooltips to all icon buttons.

</details>

---

## 🗳️ Community Contributions

A huge thank you to our contributors for this release!

| User | Contribution |
| :--- | :--- |
| <img src="https://github.com/ghost.png" width="20"> **@ghost** | Fixed typo in README |
| <img src="https://github.com/octocat.png" width="20"> **@octocat** | Implemented OAuth flow |

---

## 🔮 What's Next?

We are already working on **v2.1**, which will include:
- [ ] Mobile App (iOS/Android)
- [ ] Offline Mode
- [ ] Plugin System
