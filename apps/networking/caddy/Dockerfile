FROM caddy:2.10.2-builder-alpine AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare 
    # \--with github.com/abiosoft/caddy-yaml
# Install yq for YAML parsing
RUN apk add --no-cache py3-pip \
    && pip3 install --no-cache-dir yq

FROM caddy:2.10.2-alpine

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

