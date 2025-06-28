# 🔥 Auto Web Server Deployment with Docker, GitHub Actions & Ansible

This project demonstrates a complete CI/CD pipeline to build, publish, and deploy an Apache web server using Docker, GitHub Actions, and Ansible. The goal is to automate:

✅ Building a Docker image for Apache + static website  
✅ Pushing the image to Docker Hub using GitHub Actions  
✅ Pulling and running the image on target hosts with Ansible  
✅ Easily repeatable deployments to self-hosted infrastructure  

---
## 🚀 What This Project Does

1. **Dockerfile**: Builds a lightweight Apache web server image serving a custom `index.html`.

2. **GitHub Actions Workflow** (`apache2run.yml`):
   - Runs on workflow dispatch.
   - Builds the Docker image from your Dockerfile.
   - Logs in to Docker Hub using a Personal Access Token.
   - Pushes the image to Docker Hub with a specific tag.

3. **Ansible Playbook** (`deploy.yml`):
   - Installs Docker on managed nodes if not already present.
   - Pulls the latest Docker image from Docker Hub.
   - Runs the container mapping port 8080:80.
   - Ensures the container is restarted if needed.

---
🙌 Author
Made with ❤️ by bha5kar

