FROM registry:2.6
ARG MINIO_URL
COPY minio-config.yml /etc/docker/registry/config.yml
RUN sed -i -e "s/localhost/$MINIO_URL/g" /etc/docker/registry/config.yml
RUN cat /etc/docker/registry/config.yml

EXPOSE 5000
