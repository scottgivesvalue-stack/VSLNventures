# VSLN Ventures GitHub Pages Deployment

## 1) Create a new GitHub repository
Create a public repository, for example: `vslnventures-site`.

## 2) Push this local project
Run these commands from this folder:

```bash
git add .
git commit -m "Launch VSLN Ventures website"
git branch -M main
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPO>.git
git push -u origin main
```

## 3) Enable GitHub Pages
1. In GitHub, open the repository.
2. Go to Settings -> Pages.
3. Source: Deploy from a branch.
4. Branch: `main` and folder `/ (root)`.
5. Save.

## 4) Custom domain
1. In the same Pages settings, set custom domain to:

`vslnventures.com`

A `CNAME` file is already included in this project.

## 5) Update DNS (Squarespace DNS panel)
Remove old Squarespace records and set GitHub Pages records:

A records for root (`@`):
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

CNAME for `www`:
- `<YOUR_GITHUB_USERNAME>.github.io`

## 6) Wait for propagation
- GitHub Pages usually builds in 1-5 minutes.
- DNS can take up to a few hours.

## 7) Verify
- https://vslnventures.com
- https://www.vslnventures.com

If only one works initially, wait for DNS propagation and refresh.
