#ddev-generated
USER $username
ENV FLYCTL_INSTALL="/home/$username/.fly"
RUN curl -LsS https://fly.io/install.sh | sh
USER root

RUN apt-get update && apt-get install -y php8.3-excimer
