# DevOps Lab

A simple Node.js application containerized with Docker to demonstrate DevOps fundamentals including Dockerization, version control, and automation.

## 🎯 Project Overview

This project showcases:
- **Node.js Application**: A minimal JavaScript app that outputs version information
- **Docker**: Containerization of the Node.js application using Alpine Linux
- **Version Control**: Git workflow with commits, tags, and remote pushes
- **Automation**: Makefile tasks for building, running, and cleaning up containers

## 📋 Prerequisites

- **Docker**: [Install Docker Desktop](https://www.docker.com/products/docker-desktop)
- **Git**: Version control system
- **Make** (optional): For running Makefile targets directly
- **Node.js** (optional): Only needed if running locally without Docker

## 📁 Project Structure

```
devops-lab/
├── app.js          # Node.js application entry point
├── Dockerfile      # Docker configuration for containerization
└── README.md       # This file
```

## 🚀 Quick Start

### Using Docker (Recommended)

```bash
# Build the Docker image
docker build -t devops-hello ./devops-lab

# Run the container
docker run --rm devops-hello

# Clean up the image
docker rmi devops-hello
```

### Using Makefile (from parent directory)

```bash
make build    # Build the Docker image
make run      # Run the container
make clean    # Remove the Docker image
```

## 📝 File Details

### `app.js`
A simple Node.js script that outputs:
```
Hello, DevOps!
v2
```

### `Dockerfile`
- **Base Image**: `node:18-alpine` (lightweight Node.js runtime)
- **Operation**: Copies `app.js` into the container and executes it with Node.js

## 🏗️ Docker Image Details

- **Image Name**: `devops-hello`
- **Base Image**: `node:18-alpine` (Alpine Linux with Node.js 18)
- **Image Size**: Minimal footprint using Alpine
- **Execution**: Automatically runs the Node.js application when started

## 📦 Version History

- **v1.0.0**: First release with app.js v2 and Docker containerization

```bash
# View commit history
git log --oneline --decorate
```

## 🔄 Git Workflow

The project includes:
- Semantic versioning via git tags
- Descriptive commit messages following conventional commits
- Remote tracking with GitHub

```bash
# Push commits
git push origin main

# Push specific tag
git push origin v1.0.0

# View all tags
git tag -l
```

## 🛠️ Development

### Building Locally

```bash
# Install dependencies (if any)
# node-alpine has Node.js pre-installed

# Run locally (optional)
node app.js
```

### Modifying the Application

1. Edit `app.js`
2. Rebuild the Docker image: `docker build -t devops-hello ./devops-lab`
3. Run the updated container: `docker run --rm devops-hello`

## 📚 Learning Resources

This project demonstrates:
- Docker basics and containerization
- Git version control and tagging
- Build automation with Makefile
- CI/CD pipeline foundations

## 🔗 Resources

- [Docker Documentation](https://docs.docker.com/)
- [Node.js Documentation](https://nodejs.org/)
- [Git Documentation](https://git-scm.com/doc)
- [Conventional Commits](https://www.conventionalcommits.org/)

## 📄 License

MIT License - Feel free to use this project for learning purposes.

---

**Repository**: https://github.com/vicky131-tech/devops-lab

**Version**: 1.0.0
