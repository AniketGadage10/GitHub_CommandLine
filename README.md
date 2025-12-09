# 🚀 Git Command Line Notes  
Complete Git reference guide — formatted for GitHub documentation.

## **1. Configure Git User**
```sh
git config --global user.name "AniketGadage10"
git config --global user.email "xyz@gmail.com"
```

### **Check Configured User**
```sh
git config --global user.name
git config --global user.email
```

## **2. Initialize a Repository**
```sh
git init .
```

## **3. Staging Area Operations**
The staging area is where you prepare files before committing.

### **Add Files**
```sh
git add ./GitCommand.docx    # Single file
git add .                    # All files
```

### **Remove Files from Staging**
```sh
git reset ./GitCommand.docx
git restore --staged ./GitCommand.docx
```

## **4. Commit Changes**
```sh
git commit -m "comment message"
```

### **Remove File from Local Commit (Uncommit)**
```sh
git reset ./GitCommand.docx
```

## **5. Check Repository Status**
```sh
git status
```

## **6. View Commit History**
```sh
git log
```

## **7. Compare Changes**
### Working Directory → Staging
```sh
git diff
```
### Staging → Local Repository
```sh
git diff --staged
```
### Working Directory → Local Repository
```sh
git diff HEAD
```

## **8. Push Code to Remote**
```sh
git push
git push origin master
```

## **9. Clone a Remote Repository**
```sh
git clone https://github.com/AniketGadage10/GitHub_CommandLine
```

## **10. Pull vs Clone**
| Command | Purpose | When to Use |
|--------|---------|-------------|
| `git clone` | Download entire repository | First time setup |
| `git pull` | Get updates & merge | Daily updates |

`git pull = git fetch + git merge`

## **11. Fetch Updates Without Merging**
```sh
git fetch
git fetch origin
git fetch origin main

git diff main origin/main
git log main..origin/main
```

### What `git fetch` does:
- Downloads latest commits  
- Updates `origin/main`  
- Does not modify working directory  
- Needs manual merge  

## **12. What is `origin`?**
Alias to your GitHub repository URL.

## **13. Connect Local Repo to GitHub**
```sh
git remote add origin https://github.com/user/myproject.git
```

## **14. Git File Stages**
| Stage | Meaning |
|-------|---------|
| Untracked | Not in Git |
| Staged | Added to Git |
| Committed | Saved locally |
| Pushed | Uploaded to GitHub |

# Undoing Mistakes in Git

## Unstage Wrong File
```sh
git reset wrongfile.txt
git restore --staged wrongfile.txt
```

## Restore File to Last Commit
```sh
git restore app.js
```

## Undo Last Commit (Keep Changes)
```sh
git reset --soft HEAD~1
```

## Delete Last Commit (Permanent)
```sh
git reset --hard HEAD~1
```

# Git Workflow Summary
```
Working Directory → Staging → Local Repo → Remote Repo
git add → git commit → git push
```
