# CarRental - projekt inzynierski

Projekt jest aplikacja webowa do rezerwacji samochodow napisana w Symfony 6.4.

## Zawartosc paczki

- `src/` - kod aplikacji,
- `templates/` - widoki Twig,
- `assets/` - pliki frontendu,
- `config/` - konfiguracja Symfony,
- `migrations/` - migracje bazy danych,
- `tests/` - testy automatyczne,
- `composer.json` i `composer.lock` - zaleznosci PHP,
- `package.json` i `package-lock.json` - zaleznosci JavaScript,
- `.env.example` - przykladowa konfiguracja srodowiska.

Paczka nie zawiera katalogow generowanych lokalnie, takich jak `vendor/`, `node_modules/`, `var/`, `public/uploads/`, prywatnych plikow `.env`, kluczy SSH ani backupow bazy danych.

## Uruchomienie lokalne

1. Zainstaluj zaleznosci PHP:

```bash
composer install
```

2. Zainstaluj zaleznosci JavaScript:

```bash
npm install
```

3. Przygotuj konfiguracje srodowiska:

```bash
cp .env.example .env
```

4. Uruchom baze danych:

```bash
docker compose up -d
```

5. Wykonaj migracje:

```bash
php bin/console doctrine:migrations:migrate
```

6. Uruchom aplikacje:

```bash
symfony server:start
```

Alternatywnie:

```bash
php -S 127.0.0.1:8000 -t public
```

## Testy

```bash
php bin/phpunit
php bin/console doctrine:schema:validate --env=test
```
