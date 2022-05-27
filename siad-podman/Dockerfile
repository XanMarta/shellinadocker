FROM xanmarta/lenv:podman

RUN apt-get update -y && \
    apt install -y --fix-missing openssl shellinabox nginx && \
    rm -rf /var/lib/apt/lists

RUN mkdir -p /etc/my_init.d
COPY script.sh /etc/my_init.d/siab.sh
RUN chmod +x /etc/my_init.d/siab.sh

COPY nginx.conf /etc/nginx/nginx.conf
