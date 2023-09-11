#ddev-generated
ENV FLYCTL_INSTALL="/.fly"
RUN curl -L https://fly.io/install.sh | sh
ENV PATH="$FLYCTL_INSTALL/bin:$PATH"

RUN curl -LsS https://download.civicrm.org/cv/cv.phar -o /usr/local/bin/cv
RUN chmod +x /usr/local/bin/cv
