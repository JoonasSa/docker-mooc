FROM ruby:2.6.0

# INSTALL NODEJS
RUN apt-get update \
  && apt-get install -y apt-transport-https \
  && curl --silent --show-error --location https://deb.nodesource.com/gpgkey/nodesource.gpg.key | apt-key add - \
  && echo "deb https://deb.nodesource.com/node_6.x/ stretch main" > /etc/apt/sources.list.d/nodesource.list \
  && apt-get update \
  && apt-get install -y nodejs

# INSTALL RAILS DEPENDENCIES AND RUN DB MIGRATIONS
COPY . .
RUN gem install bundler && bundle install
RUN rails db:migrate
CMD ["rails", "s"]
