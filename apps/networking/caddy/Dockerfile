ARG CADDY_VERSION=2.10.2-alpine
FROM caddy:${CADDY_VERSION}-builder AS builder

RUN xcaddy build \
    --with github.com/lucaslorentz/caddy-docker-proxy/v2 \
    --with github.com/caddy-dns/cloudflare 

FROM caddy:${CADDY_VERSION}-alpine

RUN apk add --no-cache yq nano

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

CMD ["caddy", "docker-proxy"]
