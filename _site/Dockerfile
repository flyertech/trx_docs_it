FROM ruby:2.1
MAINTAINER mrafayaleem@gmail.com

RUN apt-get clean \
  && mv /var/lib/apt/lists /var/lib/apt/lists.broke \
  && mkdir -p /var/lib/apt/lists/partial

RUN apt-get update

# Install program to configure locales
RUN apt-get install -y locales
RUN dpkg-reconfigure locales && \
  locale-gen C.UTF-8 && \
  /usr/sbin/update-locale LANG=C.UTF-8

# Install needed default locale for Makefly
RUN echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen && \
  locale-gen

# Set default locale for the environment
ENV LC_ALL C.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8

RUN apt-get install -y \
    node \
    python-pygments \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/

WORKDIR /tmp
ADD Gemfile /tmp/
ADD Gemfile.lock /tmp/
RUN bundle install

VOLUME /src
EXPOSE 4000

WORKDIR /src
ENTRYPOINT ["jekyll", "serve", "-H", "0.0.0.0"]
