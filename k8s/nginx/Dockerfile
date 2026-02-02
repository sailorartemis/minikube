# Schlankes offizielles NGINX-Image
FROM nginx:alpine

# (optional) Entferne die Standard-Seite
RUN rm -rf /usr/share/nginx/html/*

# Deine Website in den NGINX-Webroot kopieren
COPY website/ /usr/share/nginx/html/

# (optional) Healthcheck
HEALTHCHECK --interval=30s --timeout=5s --retries=3 CMD wget -q -O- http://127.0.0.1/ || exit 1

# Expose Port (informativ)
EXPOSE 80