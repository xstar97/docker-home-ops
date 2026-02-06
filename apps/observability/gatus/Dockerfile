ARG GATUS_VERSION=v5.34.0
ARG MC_VERSION=v1.3.0

# Stage 1: microcheck binaries
FROM ghcr.io/tarampampam/microcheck:${MC_VERSION} AS microcheck

# Stage 2: distroless gatus runtime
FROM ghcr.io/twin/gatus:${GATUS_VERSION}

# Copy only the HTTP checker
COPY --from=microcheck /bin/httpcheck /usr/bin/httpcheck
