# ARG VERSION
# FROM almalinux:${VERSION}

# ARG VERSION
# FROM almalinux:${VERSION:-8}
# ARG GREETING
# RUN echo "$GREETING"
# RUN echo "$VERSION"

ARG VERSION
FROM almalinux:${VERSION:-8}
ARG GREETING="HELLO ANJI"
ENV GREETING=${GREETING}
RUN echo "$GREETING"
RUN echo "$VERSION"
