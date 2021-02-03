FROM gitpod/workspace-full:latest

USER gitpod

# This installs all required libs (https://github.com/SBFspot/SBFspot/wiki/Installation-Linux-SQLite#%EF%B8%8F-installation):
#  - bluetooth (required, even with Speedwire)
#  - required boost libs
#  - sqlite
RUN sudo apt-get update \
    && sudo apt-get install -yq --no-install-recommends \
        bluetooth \
        libbluetooth-dev \
        libboost-date-time-dev \
        libboost-system-dev \
        libboost-filesystem-dev \
        libboost-regex-dev \
        sqlite3 \
        libsqlite3-dev \
    && sudo apt-get clean \
    && sudo rm -rf /var/lib/apt/lists/* /tmp/*

RUN sudo mkdir /usr/local/bin/sbfspot.3/ && \
    sudo chown -R gitpod:gitpod /usr/local/bin/sbfspot.3/
ENV PATH "/usr/local/bin/sbfspot.3:$PATH"