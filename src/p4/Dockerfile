FROM nginx
WORKDIR /home
HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 \
CMD curl -f http://localhost:80 || exit 1
COPY /server/miniserver.c /home/
COPY nginx/nginx.conf /etc/nginx/
COPY start.sh .
RUN apt update && apt install gcc spawn-fcgi libfcgi-dev -y && rm -rf /var/lib/apt/lists \
    && gcc miniserver.c -lfcgi -o miniserver
RUN chown -R nginx:nginx /usr && \
    chown -R nginx:nginx /etc/nginx/nginx.conf && \    
    chown -R nginx:nginx /var/cache/nginx && \
    chown -R nginx:nginx /home && \    
    touch /var/run/nginx.pid && \
    chown -R nginx:nginx /var/run/nginx.pid
    
USER nginx
ENTRYPOINT ["sh", "start.sh"]