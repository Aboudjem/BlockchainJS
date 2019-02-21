# BlockchainJS
Simple implementation of JS Blockchain

## Installation

Use the package manager [npm](https://www.npmjs.com/) to install Bitcoin Wallet Generator.

```bash
npm install
```

## Usage

Open two terminals
#### Run first Server on first terminal:
```sh
$ HTTP_PORT=3001 P2P_PORT=6001 npm start
```

#### And run second Server on second terminal:
```sh
$ HTTP_PORT=3002 P2P_PORT=6002 PEERS=ws://localhost:6001 npm start
```

#### On a 3rd terminal:
##### display all blocks 
```sh
$ curl http://localhost:3001/blocks
```

##### display all peer nodes
```sh
$ curl http://localhost:3001/peers
```

##### add a peer
```sh
$ curl -H "Content-type:application/json" --data '{"peer" : "ws://localhost:6001"}' http://localhost:3001/addPeer
```

## Modules

```javascript
    - body-parser
    - crypto-js
    - Express
    - ws    
```
