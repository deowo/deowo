FROM scratch as builder
WORKDIR /source/
COPY index.html *.css .

FROM nginx:mainline-alpine
WORKDIR /usr/share/nginx/html
COPY $PWD/docker/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /source/ ./

