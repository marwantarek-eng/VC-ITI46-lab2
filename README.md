# GIT Lab 2 project
# 1️⃣ Create a new project locally
mkdir git-lab2
cd git-lab2
git init

# 2️⃣ Create a README file and commit
echo "# Git Lab 2 Project" > README.md
git add .
git commit -m "Initial commit"

# 3️⃣ Connect to remote repository
git remote add origin https://github.com/marwantarek-eng/VC-ITI46-lab2.git
git branch -M main
git push -u origin main

# 4️⃣ Create dev branch and add file
git checkout -b dev
echo "This file is for dev branch" > dev.txt
git add .
git commit -m "Add dev file"
git push origin dev

# 5️⃣ Create test branch and add file
git checkout main
git checkout -b test
echo "This file is for test branch" > test.txt
git add .
git commit -m "Add test file"
git push origin test

# 6️⃣ Merge dev and test into main
git checkout main
git merge dev
git merge test
git push origin main

# 7️⃣ Delete branch locally
git branch -d dev
git branch -d test

# 8️⃣ Delete branch remotely
git push origin --delete dev
git push origin --delete test

# 📦 Checkout Without Committing Changes
# Save changes temporarily:
# git stash
# git checkout branch-name
# Restore changes later:
# git stash pop

# 9️⃣ Create annotated tag
git tag -a v1.7 -m "Version 1.7 release"

# 🔟 Push tag to remote repository
git push origin v1.7

# 1️⃣1️⃣ List tags
git tag

# 1️⃣2️⃣ Delete tag locally
git tag -d v1.7

# 1️⃣3️⃣ Delete tag remotely
git push origin --delete v1.7
<img width="715" height="334" alt="image" src="https://github.com/user-attachments/assets/176afdb5-007e-472f-950b-daa63f6dd94c" />
