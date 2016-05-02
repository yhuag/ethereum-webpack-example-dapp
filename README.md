# Ethereum Webpack Example Dapp
Example Ethereum (Solidity) smart contract decentralized app with Webpack, demonstrating the following features and behaviors:

- Simple Ethereum decentralized app (dapp) with:
  - Smart contract written in Solidity
  - A simple viewer written in Vanilla JavaScript.
- Smart contract is based on The Coin [from a tutorial on ethereum.org](https://www.ethereum.org/token).
- Direct importing of Solidity code and instantiation of smart contract via [Webpack](https://webpack.github.io) through [solc-loader](https://github.com/uzyn/solc-loader) and [web3-loader](https://github.com/uzyn/web3-loader).
  - Interfacing with smart contracts is as simple as `import { My Token } from './contract/MyToken.sol'`.
  - See [`index.js`](https://github.com/uzyn/ethereum-webpack-example-dapp/blob/master/index.js) for more details.
- A template or very simple starter kit for creating Ethereum decentralized app.


## How to run

1. Run a local Ethereum node with JSON-RPC listening at port 8545 _(default)_. [testrpc](https://github.com/ethereumjs/testrpc) would be the most straight-forward way.

  ```bash
  # Using testrpc (recommended)
  testrpc

  # If you are running Geth, 
  # make sure to run in testnet or private net and enable rpc
  geth --testnet --rpc
  ```

1. Install dependencies

  ```bash
  npm install
  ```

1. Run, during development

  ```bash
  npm start
  ```

  Once webpack build is done (`bundle.js` is generated), open `index.html` in your favorite web browser.

  Webpack is now started in `--watch` mode, any changes done at the JavaScript or Solidity files would automatically rebuild the affected modules.

1. Build, for deployment

  ```bash
  npm run build
  ```

  Upload just `index.html` and `bundle.js` to your server.

## Additional notes

1. web3-loader can be further configured, for example to reuse a deployed contract instead of reploying at every build. See [web3-loader's README](https://github.com/uzyn/web3-loader) for more details.

1. Similarly for [solc-loader](https://github.com/uzyn/solc-loader).

## Comments, bugs & collaborations

Pull requests, bug reports are welcomed.

This example dapp is put together by [U-Zyn Chua](http://uzyn.com). Say hi to me at Twitter ([@uzyn](http://twitter.com/uzyn)) or Freenode IRC (my handle: uzyn, usually at #ethereum).

Tips: `0xFfA57D3e88A24311565C9929F180739E43FBD0aA`
