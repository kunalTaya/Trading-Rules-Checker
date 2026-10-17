# Logic — Trading Rule Checker

A small, always-on-top desktop checklist for keeping trading decisions aligned with a personal plan.

## Run locally

1. Install Node.js 22.12 or newer.
2. Run `npm install`.
3. Run `npm run dev` for the Vite + Electron development app.
4. Run `npm run dist` to create a Windows NSIS installer in `release/`.

The built desktop app can be launched with `npm start` after `npm run build`.

## Save to GitHub

Create an empty repository on GitHub, then run these commands from this project folder (replace the URL with your repository URL):

```powershell
git init
git add .
git commit -m "Add Logic trading rule checker"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

The `.gitignore` keeps installed packages, build output, and installer files out of the source repository. The `package-lock.json` is included so `npm install` uses the project's locked dependency versions.

## Use

- Click the floating Logic badge to open or close the checklist; drag it to reposition.
- Check off rules, choose **Edit rules** to rename/remove items or add a personal rule.
- Expand **Badge appearance** to customize badge fill, text, outline, and running-light colors.
- Rules and appearance are saved in Electron's per-user application data folder.

The renderer has no Node.js access. A context-isolated preload exposes only preference load/save and the window move/resize controls required by the interface.
