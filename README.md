# 🍂 Stale Git Branch Report

A PowerShell script that scans your Git repository and generates a styled **HTML report** showing stale branches, their metadata, and merge status — helping you keep your Git history clean and healthy.

[![PowerShell Gallery Version](https://img.shields.io/powershellgallery/v/Get-StaleGitBranches.svg?style=flat-square&logo=powershell)](https://www.powershellgallery.com/packages/Get-StaleGitBranches)
![Made with PowerShell](https://img.shields.io/badge/Made%20with-PowerShell-012456?style=flat-square&logo=powershell&logoColor=white)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg?style=flat-square)](https://creativecommons.org/licenses/by/4.0/)


![Report Screenshot](https://raw.githubusercontent.com/gmcnickle/stale-branches/main/assets/gitTools-dk.png)

## 📋 Features

- Detects **stale branches** (not merged to `master`)
- Includes **author, age, commit stats, last message**
- Detects **open pull requests**
- Flags **fully merged** vs. **pointer merged** branches
- Filter by **author** or **branch name**
- Generates a **responsive HTML report** with dark theme
- Supports local and remote branches
- Optional **caching** for fast repeated runs

## 🚀 Installation

Install it from the PowerShell Gallery:

```powershell
Install-Script -Name Get-StaleGitBranches -Scope CurrentUser -Force
```

> 💡 Add `-AllowClobber` if you already have a script with the same name.

---

## 🔧 Parameters

```
Get-StaleGitBranches.ps1 [-OlderThanDays <int>] [-IncludeRemote] [-CleanCache]
                         [-Limit <int>] [-OutputPath <string>] [-Location <string>]
```

| Parameter        | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `-OlderThanDays` | Only include branches whose latest commit is older than this many days.    |
| `-IncludeRemote` | Include remote branches (default: false).                                  |
| `-CleanCache`    | Clears the local cache before running.                                     |
| `-Limit`         | Only process up to this many branches (for faster testing).                |
| `-OutputPath`    | Path to save the HTML report. If not specified, saves to Documents folder. |
| `-Location`      | Path to the Git repo. Optional if script is run from within the repo.      |

### 📄 Example

```powershell
.\Get-StaleGitBranches.ps1 -IncludeRemote -OlderThanDays 30 -CleanCache
```

---

## 📁 Output

The report is saved as an HTML file (e.g. `stale-branches.html`) and includes:

- Scrollable, filterable table of stale branches
- Author summary with counts
- GitHub links to each branch
- Merge status and open PR indicators

---

## 🔍 Requirements

- PowerShell 5.1+ or PowerShell Core
- Git CLI installed and available in PATH

---

## 🧹 Why?

Over time, Git branches accumulate — many of them forgotten after being merged or abandoned. This tool helps you **audit**, **track**, and **clean** them up safely.

---

## 📷 Screenshots

![Report Screenshot](https://raw.githubusercontent.com/gmcnickle/stale-branches/main/assets/stalebranches-screenshot.png)

---

## 🤝 Contributions

Feel free to fork, submit PRs, or suggest improvements via GitHub Issues.

---

## 📜 License

Creative Commons Attribution 4.0 International (CC BY 4.0)  
© 2025 Gary McNickle

This work is licensed under the Creative Commons Attribution 4.0 International License.  
To view a copy of this license, visit [creativecommons.org/licenses/by/4.0](http://creativecommons.org/licenses/by/4.0/).

---

## ✒️ Attribution

**Primary Author:** Gary McNickle ([gmcnickle@outlook.com](mailto:gmcnickle@outlook.com))  
**Co-Author & Assistant:** ChatGPT (OpenAI)

This script was collaboratively designed and developed through interactive sessions with ChatGPT, combining human experience and AI-driven support to solve real-world development challenges.

---

## 🌐 Connect

[![GitHub](https://img.shields.io/badge/GitHub-%40gmcnickle-181717?style=flat-square&logo=github)](https://github.com/gmcnickle)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Gary%20McNickle-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gmcnickle)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--7161--0992-A6CE39?style=flat-square&logo=orcid)](https://orcid.org/0009-0002-7161-0992)
[![RogueCivilian](https://img.shields.io/badge/RogueCivilian-Articles%20%26%20Projects-552B75?style=flat-square)](https://roguecivilian.net)
