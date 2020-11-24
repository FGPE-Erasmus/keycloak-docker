# fgpe-keycloak-docker

Docker setup for FGPE Identity and Access Management powered by [Keycloak](https://www.keycloak.org/).

## Running

### Setup Your Environment

Start from the sample

```bash
cp .env.sample .env
```

Change the values of `.env` as you wish.

### Run

```bash
docker-compose up -d
```

This will start Keycloak, available at `http://localhost:10001`, and a mail catcher running  SMTP server starts on port 1025 and the HTTP server starts on port 8025.

### Configuration

There are two clients in the FGPE realm:

* `fgpe-gamification-service` client for the gamification service. 
* `fgpe-learning-platform` client for the learning platform.

Open Keycloak Admin Console > Clients > <client> > Credentials > Regenerate Secret
