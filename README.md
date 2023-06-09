# News Aggregator

## News Aggregator API

Powered by Laravel.

### How to run:

1. Install dependencies.

```bash
cd news-aggregator-api
composer i
```
2. Copy `.env.example` into `.env`.

```bash
cp .env.example .env
```

3. Generate Laravel key.

```bash
php artisan key:generate
```

4. Update environment variables (`.env`) for frontend app and Laravel Sail database.

```bash
# ...
FRONTEND_URL=http://localhost:3000
# ...
DB_HOST=mysql
DB_DATABASE=laravel
DB_USERNAME=sail
DB_PASSWORD=password
# ...
```

5. Build and run the containers.

```bash
./vendor/bin/sail up
```

## News Aggregator UI

Powered by React.js & Next.js.

### How to run:

1. Install dependencies.

```bash
cd news-aggregator-ui
npm i
```

2. Update environment variables (`.env.local`) to match backend.

```bash
NEXT_PUBLIC_BACKEND_URL=http://localhost
```

3. Build and run container.

```bash
# Development (next dev + hot reload)
docker-compose -f docker-compose.development.yml up --build

# Production (next start)
docker-compose -f docker-compose.production.yml up --build
```
