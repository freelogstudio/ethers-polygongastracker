# ethers-polygongastracker

Use this module to override your ethers.js provider when using the Polygon (MATIC) network.

## Usage

```js
const { createGetGasPrice } = require('ethers-polygongastracker');

provider.getGasPrice = createGetGasPrice('rapid') // available modes are rapid, fast, min, and standard

// after overriding, all transactions sent with this provider (or signer that uses this provider) will use the correct gas price on Polygon
```

## Global Usage

For the cowboys of ethdev, this technique works

```js

const { createGetGasPrice } = require('ethers-polygongastracker');
const BaseProvider = ethers.providers.BaseProvider;

BaseProvider.prototype.getGasPrice = createGetGasPrice('rapid');

// all providers in your runtime will now use the rapid gas price -- Get ETH'd

```


## License

MIT

## Author

Freelog Studio
[https://freelog.studio](https://freelog.studio)
