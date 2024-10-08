- Dex Screener - https://dexscreener.com/ & https://poocoin.app/
- Api for Google Sheet - https://cryptoprices.cc/
- Gas fee for USDT - https://gasfeesnow.com/ - 
- Insight for Crypto Token - https://token.unlocks.app/
- News Aggregator - https://cryptopanic.com/
- Trading Data Aggregator - https://birdeye.so/ 
- Research websote - https://www.coinbureau.com/review/crypto-research-tools/
- Token Data - https://www.coingecko.com/
- Defi Screener - https://defillama.com/
- Overview of Token - https://cryptobubbles.net/
- Price Chart Rainbow - https://www.blockchaincenter.net/en/bitcoin-rainbow-chart/
- Verify pan of buyer - https://eportal.incometax.gov.in/iec/foservices/#/pre-login/verifyYourPAN
- Crypto Taxation guide - https://cleartax.in/s/cryptocurrency-taxation-guide
- List of All Netowrk Config - https://chainlist.org/
- Code for DIffrenct Token Contract - https://www.cookbook.dev/
- Find RPC - https://rpc.info/

### List of Faucet websites
- https://www.l2faucet.com/
- https://moralis.io/faucets/
- https://faucet.polygon.technology/
- https://app.aave.com/
- https://faucet.triangleplatform.com/
- https://learnweb3.io/faucets/sepolia/
- https://cloud.google.com/application/web3/faucet/ethereum/sepolia
- https://www.sepoliafaucet.io/
- https://www.infura.io/faucet/sepolia
- https://faucet.chainstack.com/sepolia-testnet-faucet
- https://faucets.chain.link/

### Create Custom Token with these Websites
- https://www.welaunchit.org/
- https://createmytoken.com/
- https://coinfactory.app/memecoin-generator
- https://www.pinksale.finance/
- https://www.pump.fun/board

### Other
- https://eportal.incometax.gov.in/iec/foservices/#/pre-login/verifyYourPAN
- https://cleartax.in/s/cryptocurrency-taxation-guide
- https://app.uniswap.org/swap?outputCurrency=`<ReplaceWithContractAddress>`
- How to Set TOken Price - https://www.youtube.com/watch?v=yzdh5RRWxAk&list=WL

```
You are a CryptoTokenGeneratorGPT, an AI specialized in crafting Solidity code to create tokens using OpenZeppelin and Remix. Your objective is to generate robust Solidity code tailored to the user's specified blockchain network. You'll adhere to industry standards to ensure top-notch security. Before finalizing the code, you will inquire about key parameters such as, Token Name, Token Symbol, initial supply, maximum supply, blockchain network (e.g., Polygon Mainnet, Binance Smart Chain Mainnet, Avalanche Mainnet etc), minting support, burning support, pausing support, and the possibility of an unlimited supply. Your goal is to produce optimized, secure Solidity code meeting the user's requirements efficiently.

User's Input are Below:

Token Name: My Token
Token Symbol: TOKN
Initial supply: 7 Millions
Maximum supply: 70 Millions
Blockchain network: Polygon Mainnet
Minting support: No
Burning support: Yes
Pausing support: No
Possibility of unlimited supply: No
```

```
Network name: Amoy
New RPC URL: https://rpc-amoy.polygon.technology/
Chain ID: 80002
Currency symbol: MATIC
Block explorer URL: https://www.oklink.com/amoy

```js
// SPDX-License-Identifier: MIT
// Compatible with OpenZeppelin Contracts ^5.0.0
pragma solidity ^0.8.20;

import "@openzeppelin/contracts@5.0.2/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts@5.0.2/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts@5.0.2/token/ERC20/extensions/ERC20Permit.sol";
import "@openzeppelin/contracts@5.0.2/token/ERC20/extensions/ERC20Votes.sol";
import "@openzeppelin/contracts@5.0.2/access/Ownable.sol";

contract YourTOkenNameWithoutSpace is ERC20, ERC20Burnable, ERC20Permit, ERC20Votes, Ownable {
    constructor(address initialOwner)
        ERC20("YourTokenName", "Your Token Symbol")
        ERC20Permit("YourTokenName")
        Ownable(initialOwner)
    {
        _mint(msg.sender, 7000000 * 10 ** decimals());
    }

    // override the default decimal 18 to 9
    function decimals() public view virtual override returns (uint8) {
        return 9;
    }

    function clock() public view override returns (uint48) {
        return uint48(block.timestamp);
    }

    // solhint-disable-next-line func-name-mixedcase
    function CLOCK_MODE() public pure override returns (string memory) {
        return "mode=timestamp";
    }

    // The following functions are overrides required by Solidity.

    function _update(address from, address to, uint256 value)
        internal
        override(ERC20, ERC20Votes)
    {
        super._update(from, to, value);
    }

    function nonces(address owner)
        public
        view
        override(ERC20Permit, Nonces)
        returns (uint256)
    {
        return super.nonces(owner);
    }
}
```

![image](https://github.com/user-attachments/assets/a89e3242-3188-439a-bee5-0a18de155c1d)
