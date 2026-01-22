# ‚öõÔ∏è Modern React Deployment Architecture

This repository contains a fully containerized React application deployed on a production-ready Ubuntu environment. It represents a complete transition from local development to cloud-based hosting using industry-standard tools.

## Ìª†Ô∏è Tech Stack
* **Frontend:** React.js (Production Build)
* **Web Server:** Nginx (High-Performance Engine)
* **Infrastructure:** AWS Ubuntu EC2 Instance
* **Version Control:** Git & GitHub

## Ì∫Ä Key Features
* **Optimized Static Hosting:** Leveraging Nginx for low-latency delivery of React assets.
* **SPA Routing:** Custom Nginx configuration to support `react-router-dom` and prevent 404 errors on refresh.
* **Clean History:** Re-initialized Git architecture with 100% ownership and streamlined commit logs.

## Ì≥ã Deployment Workflow
1. **Compilation:** Generated production-ready artifacts using `npm run build`.
2. **Server Logic:** Configured `try_files` directives in Nginx to handle Single Page Application (SPA) logic.
3. **Security:** Implemented `www-data` ownership and 755 permissions for secure web access.

---
*Created and maintained by TBZEED**

*********************************************************************************************************************************

# Ì≥ù Personal Dev Notes

### Ì¥ë Server Access
- **Web Root:** `/var/www/html`

### Ì¥Ñ Update & Deploy Cycle
Whenever I change the code, I run:
1. `npm run build` (Build)
2. `sudo cp -r build/* /var/www/html/` (Deploy)
3. `sudo systemctl restart nginx` (Refresh Server)

### ‚òÅÔ∏è Syncing to GitHub
1. `git add .`
2. `git commit -m "Describe the change"`
3. `git push origin main`

### ‚ö†Ô∏è Important Files
- **Nginx Config:** `/etc/nginx/sites-available/default`
- **React Logic:** `src/App.js`

