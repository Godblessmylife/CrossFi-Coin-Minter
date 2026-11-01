# CrossFi Coin Minter

A web app for creating your own tokens on the CrossFi network without writing code. Connect a wallet, choose a token type, fill in the name, symbol and supply, and deploy.

The current configuration targets **CrossFi Testnet**.

## Features

- Token types:
  - ERC-20 fixed amount
  - ERC-20 burnable
  - ERC-20 mintable
  - ERC-20 pausable
  - ERC-20 capped
  - ERC-20 multi-function
  - ERC-721 full function
  - Stake token
- Configurable name, symbol, supply, cap and admin address.
- Wallet connection through MetaMask or any EVM wallet.
- Extra contract templates in `contracts/`: `TaxToken`, `AntiWhale`, `Blacklisted`, `Cooldown`.
- `router-evm/`: an EVM swap and bridge interface included from the upstream template.

## Network

| Setting | Value |
| --- | --- |
| Network | CrossFi Testnet |
| Chain ID | 4157 |
| RPC | `https://rpc.testnet.ms` |
| Explorer | `https://scan.testnet.ms` |
| Currency | XFI |

Network settings are in [`js/config.js`](js/config.js).

## Run locally

The app is static. No build step is needed.

```shell
git clone https://github.com/Godblessmylife/CrossFi-Coin-Minter
cd CrossFi-Coin-Minter
python3 -m http.server 8000
```

Open `http://localhost:8000`, connect a wallet on CrossFi Testnet and create a token.

## Configuration

In [`js/config.js`](js/config.js) you can change:

- the network parameters (chain ID, RPC URL, explorer URL);
- `FeeReciever`, the address that receives the service fee;
- the fee amount per network.

## Notes

- Use a testnet wallet. Do not use a wallet that holds real funds.
- The contracts in this repository have not been independently audited. Review them before any mainnet use.

## Credits and license

This project is based on the open-source token creator by [CryptoDappRun](https://github.com/CryptoDappRun) and adapted for CrossFi. It is released under the [MIT License](./LICENSE). The original copyright notice is kept.

## Author

Ioannes Avakian, senior software engineer (full-stack, distributed systems, blockchain).
Contact: masterofscience1993@gmail.com
