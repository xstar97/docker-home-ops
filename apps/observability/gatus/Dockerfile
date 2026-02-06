ARG GATUS_VERSION=v5.34.0
FROM ghcr.io/twin/gatus:${GATUS_VERSION}

# Install wget + curl (image is alpine-based)
RUN apk add --no-cache \
    wget \
    curl

# Nothing else changes – keep original entrypoint/cmd
