# Deployment Guide

## Local Development Setup

### 1. Prerequisites
- Node.js 16+ 
- PHP 7.4+
- Modern web browser

### 2. Quick Start
```bash
# Install dependencies
npm install

# Start frontend (Terminal 1)
npm run dev

# Start backend (Terminal 2)  
npm run backend

# Or start both together
npm start
```

### 3. Access Points
- **Frontend**: http://localhost:5173
- **Backend**: http://localhost:8000
- **API Endpoint**: http://localhost:8000/process.php

## Production Deployment

### Frontend (Static Build)
```bash
# Build for production
npm run build

# Preview production build
npm run preview

# Deploy dist/ folder to your web server
```

### Backend (PHP Server)
1. Upload `backend/` folder to your PHP hosting
2. Ensure PHP extensions are enabled:
   - cURL
   - DOM
   - JSON
   - libxml
3. Update CORS headers if needed
4. Configure SSL certificate path

### Environment Variables
Copy `.env.example` to `.env.local` and configure:
```env
VITE_BACKEND_URL="https://your-domain.com"
VITE_API_ENDPOINT="/api/process.php"
```

## Docker Deployment (Optional)

### Dockerfile
```dockerfile
# Frontend
FROM node:18-alpine AS frontend
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Backend
FROM php:8.1-apache
RUN docker-php-ext-install curl dom json
COPY backend/ /var/www/html/
COPY --from=frontend /app/dist /var/www/html/public
EXPOSE 80
```

### Docker Compose
```yaml
version: '3.8'
services:
  app:
    build: .
    ports:
      - "80:80"
    environment:
      - PHP_MEMORY_LIMIT=512M
```

## Security Considerations

1. **CORS Configuration**: Update allowed origins
2. **Rate Limiting**: Implement request throttling
3. **Input Validation**: Sanitize all user inputs
4. **SSL/TLS**: Use HTTPS in production
5. **API Keys**: Secure external service tokens

## Performance Optimization

1. **Frontend**:
   - Enable gzip compression
   - Use CDN for static assets
   - Implement service worker caching

2. **Backend**:
   - Enable PHP OPcache
   - Use connection pooling
   - Implement response caching

## Monitoring

1. **Error Logging**: Configure PHP error logs
2. **Performance Metrics**: Monitor response times
3. **Uptime Monitoring**: Set up health checks
4. **Analytics**: Track usage patterns

## Backup Strategy

1. **Database**: Regular automated backups
2. **Configuration**: Version control all configs
3. **Logs**: Rotate and archive log files
4. **Recovery**: Test restore procedures

---

**Ready for production deployment!** 🚀