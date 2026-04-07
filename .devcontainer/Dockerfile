# Use the Arch Linux base image
FROM archlinux:latest

# Enable privileged mode
USER root

# Set up environment variables
ENV LANG=en_US.UTF-8

# Update and install necessary packages
RUN pacman -Syu --noconfirm && \
    # Install KDE Plasma and VNC
    pacman -S --noconfirm \
        tigervnc \
        plasma-desktop \
        plasma-workspace \
        dbus \
        x11vnc \
        xorg-server \
        xorg-xkbcomp \
        konsole \
        dolphin \
        firefox \
        python \
        python-numpy \
        git \
        base-devel \
        htop \
        vim && \
    # Install websockify for noVNC
    python -m pip install --break-system-packages websockify numpy
