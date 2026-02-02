# ──────────────
# Build Caddy with Cloudflare plugin
# ──────────────
FROM caddy:2.10.2-builder-alpine AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare

# ──────────────
# Final image
# ──────────────
FROM caddy:2.10.2-alpine

# Copy built Caddy binary
COPY --from=builder /usr/bin/caddy /usr/bin/caddy

# Install yq for YAML parsing
RUN apk add --no-cache py3-pip \
    && pip3 install --no-cache-dir yq
