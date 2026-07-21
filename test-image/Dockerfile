FROM alpine:3.19

# A tiny stand-in for a "private" container action: prints a recognizable
# banner, the alpine version, and whatever args it was invoked with, then exits 0.
RUN printf '%s\n' \
      '#!/bin/sh' \
      'echo "[compliance-check] private image pulled from GHCR — auth OK"' \
      'echo "[compliance-check] alpine-release: $(cat /etc/alpine-release)"' \
      'echo "[compliance-check] args: $*"' \
      > /entrypoint.sh \
 && chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
