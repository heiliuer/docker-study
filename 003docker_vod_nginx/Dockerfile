
# Pull base image.
FROM heiliuer/alpine_python_nginx

ENV work_dir /opt/vod-server

ENV ng_confs /etc/nginx/conf.d/

WORKDIR ${work_dir}

COPY nginx.conf /etc/nginx/nginx.conf

COPY vod-server ${work_dir}

COPY nginx-conf ${ng_confs}

ENV PORT 9999

# Expose ports.
EXPOSE ${PORT}

CMD ["nginx"]
