# The CodeGame Project

## About

The CodeGame project is an ecosystem of fun and interesting games that can be played using self-written programs.
Most games are multiplayer-enabled and don't require much programming knowledge or skill, so everyone can play.
Of course, this doesn't prevent advanced players from creating insane AIs that play flawlessly. That would be awesome!

Here's a link to the [getting started guide](./getting-started.md).

## How does it work?

Game servers host games with prebuilt game logic. They can be accessed via a few HTTP endpoints and a WebSocket endpoint.
We provide server libraries for a variety of programming languages to make it easy for anyone to create a CodeGame compliant game.

Clients connect to a server's WebSocket endpoint for a bidirectional TCP connection to the server.
They receive events from the server informing them of things that happened and can send events to the server to make things happen in-game.
As with server libraries, we provide client libraries for as many programming languages as possible.

Please view the [docs](https://github.com/code-game-project/docs) for more detailed information on how CodeGame works.
