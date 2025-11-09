# Deployment Guide

## Deploy to Vercel (Recommended)

The easiest way to deploy this Next.js application is through Vercel:

### Option 1: Deploy from GitHub

1. Push your code to GitHub
2. Visit [vercel.com](https://vercel.com)
3. Click "Import Project"
4. Select your GitHub repository
5. Vercel will automatically detect Next.js and configure settings
6. Click "Deploy"

### Option 2: Deploy via Vercel CLI

1. Install Vercel CLI:
\`\`\`bash
npm i -g vercel
\`\`\`

2. Run deployment command:
\`\`\`bash
vercel
\`\`\`

3. Follow the prompts

## Deploy to Other Platforms

### Netlify

1. Build the application:
\`\`\`bash
npm run build
\`\`\`

2. Deploy the `.next` folder to Netlify

### Docker

1. Create a `Dockerfile`:
\`\`\`dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
\`\`\`

2. Build and run:
\`\`\`bash
docker build -t stock-analyzer .
docker run -p 3000:3000 stock-analyzer
\`\`\`

## Environment Variables

This application doesn't require environment variables for basic functionality. If you add features that need API keys or secrets, create a `.env.local` file:

\`\`\`env
# Example
NEXT_PUBLIC_API_URL=your-api-url
\`\`\`

## Production Checklist

- [ ] Update `package.json` name and version
- [ ] Test build locally: `npm run build && npm start`
- [ ] Check all links and images work
- [ ] Verify responsive design on mobile
- [ ] Test all calculations with various inputs
- [ ] Update README with your GitHub username
- [ ] Add Google Analytics (optional)
- [ ] Set up error monitoring (optional)

## Performance Optimization

- The app uses Next.js App Router for optimal performance
- Static generation where possible
- Tailwind CSS for minimal bundle size
- Optimized component rendering

## Monitoring

Consider adding:
- Vercel Analytics (built-in)
- Error tracking (Sentry)
- User analytics (Google Analytics, Plausible)
