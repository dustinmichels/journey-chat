# Journey Chat

Get submodules:

```sh
git submodule update --init
```

## Backend

The backend, called `journeychat`, is built with Python & FastAPI.

It requires python (3.8?), poetry to install Python dependencies, and [sqlite](https://sqlite.org/index.html).

```sh
cd journeychat

# install python deps
poetry install

# setup SQL database
poetry run ./prestart.sh

# run app
poetry run ./run.sh
```

Should start running at `localhost:8000`. API documentation at `localhost:8000/docs`.

## Frontend

The frontend is built with Vue.js / Nuxt.

It requires node 14.

```sh
cd frontend

# switch to proper node?
nvm use 14

# install deps
npm install

# run app
npm run dev
```

Frontend runs at `localhost:3000`.

## Testing App

Once both applications are running, try signing in with an example user at `localhost:3000`.

```sh
email: dustin@dustin.com
password: dustin
```

You should be able to see some rooms with messages!

In another browser or private window try signing in with another person, and you should be able to chat!

```sh
email: joe@joe.com
password: joe
```

You can also register a new user via frontend.
