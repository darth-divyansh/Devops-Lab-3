# DevOps Lab 4
## Using Git Submodules and Hosting on GitHub Pages

## Objective
To understand and practice using Git submodules and hosting a website on GitHub Pages.

## Prerequisites
- A GitHub account with three repositories:
  - **Repo1**: Contains `index.html`
  - **Repo2**: Contains CSS file
  - **Repo3**: Contains JavaScript file
- Basic knowledge of Git and GitHub Pages.

## Steps to Use Git Submodules and Host on GitHub Pages

### 1. Clone the Main Repository (Repo1)
To begin, clone the repository where submodules will be added:
```sh
git clone https://github.com/user/Repo1.git
cd Repo1
```

### 2. Add Submodules (Repo2 and Repo3)
To add Repo2 as a submodule:
```sh
git submodule add https://github.com/user/Repo2.git css
```
To add Repo3 as a submodule:
```sh
git submodule add https://github.com/user/Repo3.git js
```

### 3. Initialize and Update Submodules
After cloning Repo1, initialize and update the submodules:
```sh
git submodule init
```
```sh
git submodule update
```

### 4. Commit and Push Changes
To save the submodule links in the repository:
```sh
git add .
git commit -m "Added submodules for CSS and JS"
git push origin main
```

### 5. Enable GitHub Pages
1. Go to the **Repo1** repository on GitHub.
2. Navigate to **Settings > Pages**.
3. Under **Branch**, select `main` and save the settings.
4. The website will be available at:
   ```
   https://user.github.io/Repo1/
   ```

### 6. Updating Submodules
To pull the latest changes from submodules:
```sh
git submodule update --remote
```
To push the updates:
```sh
git add .
git commit -m "Updated submodules"
git push origin main
```

## Conclusion
This lab demonstrated how to use Git submodules to manage dependencies across multiple repositories and how to host a live website using GitHub Pages.

