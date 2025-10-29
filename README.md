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


