# Deploy this gym website to GitHub Pages

This copy is prepared for GitHub Pages. The Vite build uses relative asset paths, so you do not need to hard-code the repository name.

1. Create a GitHub repository.
2. Upload **all files and folders from this ZIP**, including the hidden `.github` folder, to the repository root.
3. Make sure the default branch is `main`.
4. In GitHub open **Settings > Pages**.
5. Under **Build and deployment > Source**, choose **GitHub Actions**.
6. Open the **Actions** tab. The `Deploy to GitHub Pages` workflow should run automatically after the push.
7. When it succeeds, the deployment job shows the public Pages URL.

## Local test

```powershell
npm.cmd install
npm.cmd run dev
```

Production build test:

```powershell
npm.cmd run build
npm.cmd run preview
```

## Notes

- This project is currently a client-side React/Vite website. No server/database is required for the pages and UI found in the supplied source.
- `.env` files are ignored by Git and should not contain secrets committed to GitHub.
- If GitHub Actions fails, open the failed workflow and copy its error log for debugging.
