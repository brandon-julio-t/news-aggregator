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

4. Update environment variables (`.env`) for News API, frontend app, and Laravel Sail database.

```bash
# ...
NEWSAPI_API_KEY=8ff458ef1b004dc1884447752950b816
THE_GUARDIAN_API_KEY=3523b1b5-e18c-4b8e-bebe-10ecf8f0290d
NEW_YORK_TIMES_API_KEY=DE4tUCzb77G0DwzF0yWRlmQvA3HQ4LoL
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

6. Migrate database and seed the application (~10s - 20s).

```bash
./vendor/bin/sail php artisan migrate --seed
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
docker compose up --build
```
