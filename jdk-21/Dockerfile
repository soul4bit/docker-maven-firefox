FROM maven:3.9.10-eclipse-temurin-21

# Firefox 147.0
ARG FIREFOX_VERSION=147.0
RUN apt-get update -qqy \
 && apt-get -qqy install bzip2 xz-utils libgtk-3-0 libx11-xcb1 libdbus-glib-1-2 libxt6 libasound2t64 wget ca-certificates \
 && rm -rf /var/lib/apt/lists/* /var/cache/apt/* \
 && wget -q -O /tmp/firefox.tar.xz https://download-installer.cdn.mozilla.net/pub/firefox/releases/$FIREFOX_VERSION/linux-x86_64/en-US/firefox-$FIREFOX_VERSION.tar.xz \
 && tar xJf /tmp/firefox.tar.xz -C /opt \
 && rm /tmp/firefox.tar.xz \
 && mv /opt/firefox /opt/firefox-$FIREFOX_VERSION \
 && ln -s /opt/firefox-$FIREFOX_VERSION/firefox /usr/bin/firefox

# Geckodriver - простая установка в /usr/local/bin
ARG GECKODRIVER_VERSION=v0.36.0
RUN wget -q -O /tmp/geckodriver.tar.gz https://github.com/mozilla/geckodriver/releases/download/$GECKODRIVER_VERSION/geckodriver-$GECKODRIVER_VERSION-linux64.tar.gz \
 && tar -xzf /tmp/geckodriver.tar.gz -C /usr/local/bin/ \
 && rm /tmp/geckodriver.tar.gz \
 && chmod +x /usr/local/bin/geckodriver