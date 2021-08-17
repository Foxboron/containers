FROM docker.io/archlinux:latest

ENV NAME=archlinux-toolbox VERSION=rolling
LABEL com.github.containers.toolbox="true" \
      name="$NAME" \
      version="$VERSION"

RUN pacman -Sy sudo git zsh flatpak-xdg-utils --noconfirm
RUN pacman -Scc --noconfirm
RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/toolbox

CMD /bin/zsh
