# Postgresql-zhparser
Postgres 14.2 with zhparser

## Docker Build
```
docker -D build --tag postgresql-zhparser --no-cache --progress=plain .
```
or without debug log
``` docker build --tag postgresql-zhparser . ```

## Docker Run
``` docker run --name postgresql-zhparser -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=not_a_secret -p 5432:5432 -d postgresql-zhparser ```

## Usage
``` CREATE EXTENSION zhparser; ```
``` CREATE TEXT SEARCH CONFIGURATION example (PARSER = zhparser); ```
``` ALTER TEXT SEARCH CONFIGURATION example ADD MAPPING FOR n,v,a,i,e,l WITH simple; ```
