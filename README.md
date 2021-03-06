# theMovieDB, theTVDB and OMDB API Wrapper

[![Dependency Status](https://gemnasium.com/badges/github.com/bhutanio/movietvdb.svg)](https://gemnasium.com/github.com/bhutanio/movietvdb)

# Requirements
- [**PHP**](https://php.net) 5.6.4+ (**7.0+** preferred)
- PHP Extensions: openssl, mbstring, phpredis
- [Redis](http://redis.io) Server
- [Composer](https://getcomposer.org)

## API Keys
- theMovieDB: https://www.themoviedb.org/documentation/api
- theTVDB: https://api.thetvdb.com/swagger
- OMDB: http://www.omdbapi.com/

## Usage
```php
$client = new \Bhutanio\Movietvdb\MovieScrapper('TMDB_API_KEY', 'TVDB_API_KEY', 'OMDB_API_KEY');

// Get Movie Information by IMDB ID
$movie = $client->scrape('movie', 'tt0120737');

// Get Movie Information by TheMovieDB ID
$movie = $client->scrape('movie', null, '120');

// Get TV Information by IMDB ID
$tv = $client->scrape('tv', 'tt0944947');

// Get Person information by TheMovieDB's Person ID
$person = $client->person('1327');

```
