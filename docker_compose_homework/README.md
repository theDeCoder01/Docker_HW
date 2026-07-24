# Guestbook App 🚀

A tiny Docker Compose app for recording guestbook messages.

## Start the app

This command launches the app and the database in the background, so you can keep using your terminal.

```bash
docker-compose up -d
```

## Record a message

Use this command to send a new guestbook message to the app. It posts JSON data to the `/sign` endpoint.

```bash
curl -X POST http://localhost:8080/sign \
  -H "Content-Type: application/json" \
  -d '{"message": "Type your msg here"}'
```

## Review all messages

Run this to fetch every message stored in the guestbook. The app returns the collected entries in JSON format.

```bash
curl http://localhost:8080/messages
```

## Shut down the app

This stops the running containers and removes the network, but keeps the database data unless you remove volumes.

```bash
docker-compose down
```

Have fun! 😊
