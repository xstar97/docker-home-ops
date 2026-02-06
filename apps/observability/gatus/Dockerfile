ARG GATUS_VERSION=v5.34.0

# Stage 1: grab + verify tools
FROM alpine:3.20 AS tools
RUN apk add --no-cache wget curl \
 && command -v wget >/dev/null \
 && command -v curl >/dev/null

# Stage 2: distroless runtime
FROM ghcr.io/twin/gatus:${GATUS_VERSION}

# Copy binaries
COPY --from=tools /usr/bin/wget /usr/bin/wget
COPY --from=tools /usr/bin/curl /usr/bin/curl
