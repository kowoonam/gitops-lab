# nginx 이미지에 내 페이지를 얹은 이미지
FROM nginx:1.27-alpine

# CI가 빌드할 때 커밋 ID를 넘겨준다 (로컬에서 그냥 빌드하면 dev)
ARG VERSION=dev

COPY index.html /usr/share/nginx/html/index.html
RUN sed -i "s/__VERSION__/${VERSION}/g" /usr/share/nginx/html/index.html
