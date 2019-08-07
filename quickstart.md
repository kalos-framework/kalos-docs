# Getting Started

**Kalos** is based on Node, so make sure to have it in your system.

To verify your Node installation and version, use following command:

```sh
node -v
```

## Create your first project

Let's get your hand dirty with the `Hello World` project using Kalos framework.

First, we need to create project directory.

```sh
$ mkdir hello-world && cd hello-world
$ npm init -y
```

Then we need to install `kalos`.

```sh
$ npm i --save kalos
```

Create your entry point for project, named it like `index.js` and try following hello world code:

```js
import Kalos from 'kalos';

const router = new Kalos.Router();
const server = new Kalos.Server();

router.get('/', (req, res) => {
    res.send('Hello World');
});

server.configRouter(router);
server.start((ip, port) => {
    console.log('Server started at: ' + ip + ':' + port);
});
```

Next is to start the server by issuing following command:

```
node index.js
```

You can access the web now in browser at `http://127.0.0.1:8080`.

**Congratulation!**. You just just your first project work and running using **kalos** framework.