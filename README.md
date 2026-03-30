This is an example app to help install [Tollerus](https://tollerus.tools) if you don't already have a Laravel app.

# Installation

```
git clone https://github.com/petermarkley/tollerus-example-app
cd tollerus-example-app
cp .env.example .env
docker run --rm -v $(pwd):/app -w /app composer install
./vendor/bin/sail up -d
./vendor/bin/sail artisan key:generate
./vendor/bin/sail artisan migrate --seed
./vendor/bin/sail npm install
./vendor/bin/sail npm run build
```

That's it! You can now visit `localhost:8080/tollerus/admin` in your browser (or whatever port is set by `APP_PORT` in your `.env` file).

Log in with:
- Email `test@example.com`
- Password `password`

Happy conlanging!
