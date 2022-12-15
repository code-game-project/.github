# CodeGame

## What is CodeGame?

With CodeGame you can programmatically control a player in a wide variety of multiplayer games by writing
a player controller in your favorite programming language.

CodeGame aims to make this process as easy as possible by standardizing the communication between game servers and clients.

We provde a set of tools and libraries which let you focus on writing the actual controller logic instead of having to worry about
complex networking and communication.

## Who is the target audience?

The CodeGame protocol is very flexible and allows the creation of games ranging from very simple ones like a number guessing game or tic-tac-toe to
complex strategy games or third-person shooters.

Therefore, everyone who is comfortable with writing basic if-statements and is willing to learn (or at least memorize) some more complex syntax for their language of choice can write a player controller or game for CodeGame.

Advanced players can create complex AIs for [Hover Race](https://github.com/code-game-project/hoverrace) utilizing sophisticated neural networks and beginners can write a simple for-loop that tries every number sequentially in [Number Guessing](https://github.com/code-game-project/number-guessing).

## How does it work?

### The protocol

CodeGame is an event driven protocol. After creating and joining a game over a standardized [HTTP API](https://code-game.org/docs/specification/api-routes) all communication happens in JSON form over a [WebSocket connection](https://code-game.org/docs/specification/communication).

Game servers send *event* objects to clients to inform them of any changed state in the game.

Clients take that information to make decisions and send *command* objects to the server, telling it what the player should do.

#### Example

The [Number Guessing](https://github.com/code-game-project/number-guessing) game accepts a `guess` command from the client containing the number it guesses.

Depending on the number the server responds with either a `too_low`, a `too_high` or a `correct` event.

### Tooling

The [CodeGame CLI](https://github.com/code-game-project/codegame-cli) helps you to painlessly develop CodeGame applications. It makes setup very easy and provides a universal interface to launch and build your projects.

## How to get started?

Take a look at the [quick start guide](https://code-game.org/docs/quick-start). It teaches you the basics of CodeGame by walking you through the installation process and the creation of a simple bot for the [Number Guessing](https://github.com/code-game-project/number-guessing) game.

Browse through our collection of [guides](https://code-game.org/docs/category/guides) to learn about diverse topics like [CodeGame Share](https://code-game.org/docs/guides/codegame-share) or [how to create your own game](https://code-game.org/docs/guides/create-game).

To gain a deeper understanding of how CodeGame works internally we recommend reading the [technical specification](https://code-game.org/docs/category/specification).

### List of games

To view a list of games created by us visit [games.code-game.org](https://games.code-game.org). Of course you can create your own games or use ones created by other people.
