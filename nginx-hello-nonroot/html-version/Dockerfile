#FROM quay.io/infraresearch/nginx:1.19.2-alpine
FROM quay.io/infraresearch/nginx:1.14.2-alpine
#1.19.2-alpine=PASSED
#1.14.2-alpine=2 High-level vulnerabilities
# We need to give all user groups write permission on folder /var/cache/nginx/ and file /var/run/nginx.pid.
# So users with random uid will be able to run NGINX.
RUN chmod -R a+w /var/cache/nginx/ \
        && touch /var/run/nginx.pid \
        && chmod a+w /var/run/nginx.pid \
        && rm /etc/nginx/conf.d/*

COPY hello.conf /etc/nginx/conf.d/
COPY index.html /usr/share/nginx/html/
EXPOSE 8080
USER nginx
