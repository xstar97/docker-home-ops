FROM caddy:2.10.2-builder-alpine AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare

FROM caddy:2.10.2-alpine

# Install yq and nano for YAML parsing and editing
RUN apk add --no-cache yq nano

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

