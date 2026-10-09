# Photoroom browser deployment

## Vercel project settings

- Git repository: `gearsganesh/Photoroom`
- Production branch: `main`
- Root Directory: repository root (`.`); do not set it to `apps/photocraft-web`
- Framework Preset: Other
- Install Command: `true` (the committed `vercel.json` controls this)
- Build Command: `bash deploy/vercel-build.sh`
- Output Directory: `dist/web`
- Environment variables: none required by the build script

Import or redeploy only after the latest `main` commit containing `deploy/vercel-build.sh` is available. The build compiles `apps/photocraft-web` with Trunk for WebAssembly. Check that `dist/web/index.html` exists in the build logs before assigning the public domain.
