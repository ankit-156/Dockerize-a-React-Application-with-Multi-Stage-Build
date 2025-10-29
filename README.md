# React Docker Multi-Stage Build 🐳

A production-ready React application demonstrating Docker multi-stage build optimization.

## Features

- ✅ Multi-stage Docker build
- ✅ Optimized image size (~50-100MB vs 1GB+)
- ✅ Nginx web server for production
- ✅ Security headers configured
- ✅ Gzip compression enabled
- ✅ React Router support
- ✅ Docker Compose ready

## Prerequisites

- Docker installed on your machine
- Docker Compose (optional)

## Quick Start

### 1. Clone the Repository
\`\`\`bash
git clone <your-repo-url>
cd react-docker-app
\`\`\`

### 2. Build the Docker Image
\`\`\`bash
docker build -t react-docker-app:latest .
\`\`\`

### 3. Run the Container
\`\`\`bash
docker run -d -p 80:80 --name react-app react-docker-app:latest
\`\`\`

### 4. Access the Application
Open your browser and navigate to:
\`\`\`
http://localhost
\`\`\`

## Using Docker Compose

\`\`\`bash
# Start the application
docker-compose up -d

# Stop the application
docker-compose down
\`\`\`

## Local Development

### Install Dependencies
\`\`\`bash
npm install
\`\`\`

### Run Development Server
\`\`\`bash
npm start
\`\`\`

The app will open at `http://localhost:3000`

### Build for Production
\`\`\`bash
npm run build
\`\`\`

## Docker Commands

### View Running Containers
\`\`\`bash
docker ps
\`\`\`

### View Logs
\`\`\`bash
docker logs react-app
\`\`\`

### Stop Container
\`\`\`bash
docker stop react-app
\`\`\`

### Remove Container
\`\`\`bash
docker rm react-app
\`\`\`

### Check Image Size
\`\`\`bash
docker images | grep react-docker-app
\`\`\`

## Project Structure

\`\`\`
react-docker-app/
├── public/              # Static files
├── src/                 # React source code
├── Dockerfile           # Multi-stage build configuration
├── .dockerignore        # Files to exclude from Docker build
├── nginx.conf           # Nginx server configuration
├── docker-compose.yml   # Docker Compose configuration
└── package.json         # Node.js dependencies
\`\`\`

## Multi-Stage Build Explained

### Stage 1: Build
- Uses Node.js 18 Alpine image
- Installs dependencies
- Builds the React application

### Stage 2: Production
- Uses Nginx Alpine image
- Copies only the built files
- Configured for optimal performance

## Benefits

1. **Smaller Image Size**: Only production files included
2. **Better Security**: Fewer dependencies = fewer vulnerabilities
3. **Faster Deployment**: Smaller images deploy quicker
4. **Production Optimized**: Nginx configured for static file serving

## Nginx Configuration

The included `nginx.conf` provides:
- Gzip compression
- Security headers
- Static asset caching
- React Router support
- Optimized performance

## Customization

### Change Port
Edit the port mapping in the docker run command:
\`\`\`bash
docker run -d -p 3000:80 --name react-app react-docker-app:latest
\`\`\`

### Modify Nginx Configuration
Edit `nginx.conf` and rebuild the Docker image.

## Troubleshooting

### Port Already in Use
Change the host port:
\`\`\`bash
docker run -d -p 8080:80 --name react-app react-docker-app:latest
\`\`\`

### Build Errors
Ensure all dependencies are properly listed in `package.json`

### Container Won't Start
Check logs:
\`\`\`bash
docker logs react-app
\`\`\`

## License

MIT

## Contributing

Pull requests are welcome!

---

**Built with ❤️ using React and Docker**
\`\`\`

---

## 🚀 Setup Instructions

1. Create a new folder: `mkdir react-docker-app && cd react-docker-app`
2. Copy all the files above into their respective locations
3. Run `npm install` to install dependencies
4. Build and run with Docker commands provided in README.md

## 📦 GitHub Upload

Simply push this folder structure to your GitHub repository:

\`\`\`bash
git init
git add .
git commit -m "Initial commit: React Docker Multi-Stage Build"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
\`\`\`
