# Real-Time Chat with Laravel, Vue.js, and Pusher

## Table of contents
- [About Application](#about-application)
- [Technologies](#technologies)
- [API Endpoints](#api-endpoints)
- [Setup Docker](#setup-docker)
- [Configuration](#configuration)
- [Install Dependencies](#install-dependencies)
- [Run Migration](#run-migration)
- [Run Application](#run-application)
- [Testing](#testing)

## About Application

- The app allows chatting between 2 signed-in users.
- The app allows chatting in different chat rooms.

## Technologies

- [Laravel](https://laravel.com/)
- [Vue.js](https://vuejs.org/)
- [Laravel Sanctum](https://laravel.com/docs/8.x/sanctum/)
- [Laravel Sail](https://laravel.com/docs/8.x/sail/)
- [Laravel Jetstream](https://jetstream.laravel.com/2.x/introduction.html/)
- [Laravel Echo](https://laravel.com/docs/8.x/broadcasting)
- [Pusher](https://pusher.com/)
- [MySQL](https://www.mysql.com/)
- [PHPUnit](https://phpunit.de/)
- [Docker](https://www.docker.com/)

## API Endpoints
Method | Route | Description
--- | --- | ---
`GET` | `/chat/rooms` | Fetch all the chat rooms
`GET` | `/chat/room/:roomId/messages` | Fetch the current room's messages
`POST` | `/chat/room/:roomId/message` | Create a message in the current room

## Setup Docker

```
$ git clone https://github.com/orkhanigidov/ChatApp.git
$ cd ChatApp
$ docker-compose up
$ cp .env.example .env
```

## Configuration

Fill out relevant items in your `.env` file, including:

```
DB_DATABASE=
DB_USERNAME=
DB_PASSWORD=

BROADCAST_DRIVER=pusher

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=
```

## Install Dependencies

```
$ composer install
$ npm install
```

## Run Migration

```
$ php artisan migrate
```

## Run Application

```
$ php artisan serve
$ npm run watch
```
Open http://127.0.0.1:80/ in the browser

## Testing

```
$ ./vendor/bin/phpunit
```

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
