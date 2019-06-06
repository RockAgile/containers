# Build Base image
FROM ruby:2.6.3 as base

# Install Postgres
RUN apt-get update -qq && apt-get install -y \
  build-essential \
  libpq-dev \
  netcat \
  postgresql-client \
  postgresql-contrib

# Install node 12
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs

# Install latest yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install -y yarn
