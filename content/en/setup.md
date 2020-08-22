---
title: Setup Contenu
description: ""
position: 2
category: Guide
---

Contenu uses [MongoDB](https://mongodb.com) as a DBMS to store the content. You can run the contenu in your local machine but, I highly recommend running it with [docker](http://docker.com).

### Step 1

First, we need to clone Contenu. The Contenu source code is available on [github](https://github.com/contenujs/contenu).

```bash
$ git clone https://github.com/contenujs/contenu
```

### Step 2

Edit the environment variables.

What needs to be done:

- Rename `.env.example` to `.env`
- Fill the value of env variables. - `MONGODB_CONNECTION` is the MongoDB connection string. - `SECRET_KEY` is used for signing JWT tokens. Use a long sequence of random characters - `JWT_EXPIRE_DAYS` is the expire time of JWT tokens. It expressed in seconds or a string describing a time span [zeit/ms](https://github.com/vercel/ms)

### Step 3

Now the only thing we need to do is running the docker.

```bash
$ docker-compose up -d
```

<alert type="warning">

The Contenu app will be run on port 8080 as default. If it is occupied in your machine, change the `Dockerfile` and `docker-compose` ports.

</alert>

### Step 4

Open `localhost:8080` and set up the app.

### Step 5

Now, In the final step, you need to add Contenu client-side library to your website. For this part please check the [Client side libraries](client-libraries)
