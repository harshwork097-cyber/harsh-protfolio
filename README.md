# Harsh Raj — Portfolio Website

A responsive static portfolio built with HTML, CSS, and vanilla JavaScript. It can run in a lightweight Nginx Docker container and deploy to Render as a static site.

## 1. Run locally

Open `index.html` in a browser, or run a local server:

```bash
python -m http.server 8080
```

Then visit http://localhost:8080.

## 2. Run with Docker

Install and start Docker Desktop first. From the project folder:

```bash
docker build -t harsh-portfolio .
docker run -d --name harsh-portfolio -p 8080:80 --restart unless-stopped harsh-portfolio
```

Open http://localhost:8080.

Useful checks:

```bash
docker ps
docker logs harsh-portfolio
```

To stop/remove the container:

```bash
docker stop harsh-portfolio
docker rm harsh-portfolio
```

The Docker image uses `nginx:alpine` and copies only the three files required to serve the site.

## 3. Publish to GitHub

Create an empty repository on GitHub, then run from this folder:

```bash
git init
git add .
git commit -m "Build responsive portfolio"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the URL with your own GitHub repository URL.

## 4. Deploy to Render with automatic redeploys

1. Sign in at https://render.com and choose **New + → Static Site**.
2. Connect GitHub and select this repository.
3. Use branch `main`.
4. Set **Build Command** to blank and **Publish Directory** to `.`.
5. Create the site. Render will provide a public `https://....onrender.com` URL.
6. Future pushes to `main` trigger a new deployment automatically.

`render.yaml` is included as a Blueprint configuration, but the easiest first deployment is through the dashboard steps above.

## 5. Before submitting

- Replace `your.email@example.com` in `index.html` with your actual email.
- Update GitHub and LinkedIn links to your profiles.
- Verify the page on a phone-sized viewport.
- Capture your own screenshots after Docker is running and after the Render deployment is live.

### Required submission items

- GitHub repository URL
- Live Render URL
- Screenshot of the site at `http://localhost:8080` while the Docker container is running
- Screenshot of the deployed site at the public Render URL

Do not submit placeholder URLs as if they were live.
"# harsh-protfolio" 
