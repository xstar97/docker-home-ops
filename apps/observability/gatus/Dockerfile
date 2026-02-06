ARG GATUS_VERSION=v5.34.0

# Stage 1: grab tools from Alpine
FROM alpine:3.20 AS tools
RUN apk add --no-cache \
    wget \
    curl

# Stage 2: real runtime image (distroless gatus)
FROM ghcr.io/twin/gatus:${GATUS_VERSION}

# Copy binaries + required certs
COPY --from=tools /usr/bin/wget /usr/bin/wget
COPY --from=tools /usr/bin/curl /usr/bin/curl
COPY --from=tools /etc/ssl/certs /etc/ssl/certs
