FROM ruby:2.5-alpine as jekyll-base

RUN apk add --no-cache build-base gcc bash cmake git

RUN gem install jekyll
COPY Gemfile ./
EXPOSE 4000

WORKDIR /site

ENTRYPOINT [ "bundle", "exec", "jekyll", "serve" ]

CMD [ "--help" ]
