# Base image
FROM qmcgaw/latexdevcontainer:latest-full
# Install additional tools
RUN set -xe \
    && apt-get update \
    && apt-get install -yqq --no-install-recommends \
    imagemagick \
    ghostscript \
    && rm -rf /var/lib/apt/lists/*
# Allow .png to .eps conversion
RUN sed -i '/disable ghostscript format types/,+6d' /etc/ImageMagick-6/policy.xml
# Add a user
ARG UID=1000
ARG GID=1000
ARG UNAME=user
# Create a working directory and a user
RUN groupadd -g $GID $UNAME  \
    && useradd -m -u $UID -g $GID -s /bin/bash $UNAME \
    && chown -R $UID:$GID /workspace
# Set the working directory
WORKDIR /workspace
# Change user
USER $UNAME