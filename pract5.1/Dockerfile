# Используем образ Fedora
FROM fedora:latest

# Обновляем репозитории и устанавливаем необходимые библиотеки для X11 и OpenJDK
RUN dnf -y install \
    xorg-x11-server-Xvfb \
    libXext \
    libXrender \
    libX11 \
    libXtst \
    libXi \
    java-17-openjdk && \
    rm -rf /var/cache/dnf

# Создаем рабочую директорию
WORKDIR /app

# Копируем проект в контейнер
COPY . /app

# Указываем команду для запуска приложения
CMD ["java", "-cp", "/app", "com.github.calc.Calc"]

