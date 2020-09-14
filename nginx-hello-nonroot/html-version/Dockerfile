FROM quay.io/redhattraining/hello-world-nginx:v1.0

# We need to give all user groups write permission on folder /var/cache/nginx/ and file /var/run/nginx.pid.
# So users with random uid will be able to run NGINX.
COPY index.html /usr/share/nginx/html/
EXPOSE 8080
USER nginx
