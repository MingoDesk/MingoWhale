<img width="150" height="150" align="left" style="float: left; margin: 0 10px 0 0;" alt="MingoDeskLogo" src="https://avatars.githubusercontent.com/u/77510075?s=200&v=4">

<h1 style="margin-top:50px">MingoWhale</h1>
<br />
<br />
<br />
<br />

[![Discord Server](https://canary.discord.com/api/guilds/799726621455417374/embed.png)](https://discord.gg/Rr5hGZs)

This repo contains the docker-compose files for production.

Prerequisites:

You need the follownig:

- Docker and Docker compose

`Below files must be located in /backend`

- mingochan.env

Example of a mingochan.env:

```sh
# Basic application configuration

NODE_ENV=DEV
PORT=1928
SESSION_SECRET=7f32646406ea61a3f61b2801b98d8f6ed69e35bbfc2c29c92e3742a0e25f8b2f
INSTANCE_NAME=125i90WQCNWQIFNIASF821io2hnrinf12SFASFasdasdwdaswSGWGFASf
BASEURL=http://localhost:1928
ORGANISATIONID=1eff307b-c25c-4c43-83c0-1752b2ebd7c2
CORS=http://localhost:8080
BASE_REDIRECT_URL=http://localhost:8080/
SESSION_LIFETIME=128000
PAGINATION_LIMIT=40
SIGNING_SECRET=7vybUSb!EYq&(h9/

# Db stuff
DB_NAME=MingoChanProduction
MONGO_URI=mongodb://default:zuft4leak_KASH_pair@mongo:27017/MingoChanProduction
REDIS_URI=redis://SKAW1lil_logh0thox@redis:6379/0

# Google
GOOGLE_CLIENT_ID=ID_HERE
GOOGLE_SECRET=ID_HERE

# Slack
SLACK_CLIENT_ID=ID_HERE
SLACK_SECRET=ID_HERE

# Office 365
```

Note that there is a more detailed explenation of the .env files content in the documentation [here](https://github.com/MingoDesk/MingoChan/blob/master/docs/readme.md#stuff-needed-to-run-the-application)

`Below files must be located in /database`

- redis.conf
- mongo.env

### Redis:

Redis needs a config file that's essentially defualt but **MUST** have a password set. Note that it must be the same as in the mingochan.env config file's password in the URI

### Mongo

```sh
MONGO_INITDB_ROOT_USERNAME=root
MONGO_INITDB_ROOT_PASSWORD=MYPASSWORDHERE
MONGO_INITDB_DATABASE=root

MONGO_NEW_DB=MingoChanProduction
MONGO_NEW_USER=default
MONGO_NEW_PASS=ANOTHERPASSWORDHERE
```

`Only the latter password (MONGO_NEW_PASS) is the one you need in the conection URI, same wiht the username.`

## Author

<img src="https://avatars.githubusercontent.com/u/16852656?v=4" width="100" height="100" align="left" style="float: left; margin: 0 10px 0 0;" alt="Runa" >

**MingoWhale** © [Titus](https://github.com/TitusEntertainment).
Authored by TitusEntertainment.

> GitHub [@TitusEntertainment](https://github.com/TitusEntertainment)

### Other notes

Big thanks to [@MrJvs](https://github.com/MrJvs) for his assistance with this repo
