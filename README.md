# Tiny Tiny RSS Docker Image

The default login credentials are:

* Username: admin
* Password: password

## Database

This container requires either a PostgreSQL or MySQL database instance. Set the following environment variables:

```
DB_HOST=
DB_PORT=
DB_NAME=
DB_USER=
DB_PASS=
```

If the database is running on a non-standard port, also pass `DB_TYPE`. Specify either `pgsql` or `mysql`.

If you already have a PostgreSQL or MySQL server around off docker you also can go with that.
Instead of linking docker containers you need to provide database hostname and port like so:

```
-e DB_HOST=172.17.42.1
-e DB_PORT=3306
```

## Other Environment Variables

The `SELF_URL_PATH` config value should be set to the URL where this container will be accessible at. 

```
SELF_URL_PATH=https://example.org/ttrss
```

## Plugins

This image includes the following plugins:

- [News+ plugin](https://github.com/voidstern/tt-rss-newsplus-plugin)
- [oneclickpocket](https://github.com/fxneumann/oneclickpocket)
- [Fever API plugin](https://github.com/DigitalDJ/tinytinyrss-fever-plugin/)

## Themes

This image includes the following themes:

- [Feedly theme](https://github.com/levito/tt-rss-feedly-theme)
