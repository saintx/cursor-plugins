---
audience: engineering
---

# How to make a bot UI intents

## Deciding whether Make Bot UI fits the task

### Find out what a bot UI does

surf references/about.md "Overview"

### Decide whether this UI should wake a Grok Bot

surf references/about.md "When to use"

## Creating the webhook the page calls

### Stop the sender key from reaching the browser or the chat

surf references/procedure.md "Keep the sender key on the server"

### Create a webhook routine the page can wake

surf references/procedure.md "Create the webhook routine"

### Copy the webhook URL without pasting the sender key into chat

surf references/procedure.md "Copy the URL and the sender key"

### Ask for the sender key on a secret-request card

surf references/procedure.md "Request the sender key"

## Serving the page where Tailscale peers can open it

### POST the webhook from the local server, not the browser

surf references/procedure.md "Host the page on this computer"

### Publish the page on the existing tailnet node

surf references/procedure.md "Put the page on the tailnet"

## Handling the routine wake

### Parse the webhook body as outside data

surf references/procedure.md "Handle the webhook wake"
