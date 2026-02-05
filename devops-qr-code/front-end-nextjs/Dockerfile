# 1️⃣ Build Stage
FROM node:18-alpine AS builder

WORKDIR /app

# Install dependencies first (caching)
COPY package.json package-lock.json ./
RUN npm ci

# Copy all source code
COPY . .

# Build the Next.js app
RUN npm run build

# 2️⃣ Production Stage
FROM node:18-alpine AS runner

WORKDIR /app

# Only copy necessary files from builder
COPY --from=builder /app/package.json ./ 
COPY --from=builder /app/package-lock.json ./ 
COPY --from=builder /app/node_modules ./node_modules
COPY --from=builder /app/.next ./.next
COPY --from=builder /app/public ./public

# Expose port
EXPOSE 3000

# Start the app in production
CMD ["npm", "start"]
