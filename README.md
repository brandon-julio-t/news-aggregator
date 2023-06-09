# News Aggregator

## News Aggregator API

Powered by Laravel.

How to run:

```bash
cd news-aggregator-api
composer i
./vendor/bin/sail up
```

## News Aggregator UI

Powered by React.js & Next.js.

How to run (Development):

```bash
cd news-aggregator-ui
npm i
docker-compose -f docker-compose.development.yml up --build
```

How to run (Production):

```bash
cd news-aggregator-ui
npm i
docker-compose -f docker-compose.production.yml up --build▬
```
