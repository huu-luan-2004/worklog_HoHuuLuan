---
title: "Build frontend React/Vite"
date: 2026-07-19
weight: 1
chapter: false
pre: " <b> 5.5.1. </b> "
---

## Objective

Build the frontend into static files that can be uploaded to S3.

## Steps

1. Open the frontend source folder.
2. Install dependencies.
3. Confirm environment variables.
4. Run the production build.
5. Check the generated `dist/` folder.

```bash
cd Fronted
npm ci
npm run build
ls -la dist
```

Do not store secrets in `VITE_` variables because they are embedded into the frontend bundle.

![Build frontend](/images/5-Workshop/5.5-Frontend-deployment/build-frontend.png)

## Result Checklist

- `dist/` exists.
- Static files are generated.
- API endpoint values are intentional and do not include secrets.
