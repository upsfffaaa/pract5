#оф образ Fedora
FROM fedora:latest

# Обновляем репозитории и устанавливаем xeyes
RUN dnf -y update && \
    dnf -y install xeyes xorg-x11-server-Xvfb

# Настроим X11 для запуска
ENV DISPLAY=:0

# Запускаем xeyes
CMD ["xeyes"]

