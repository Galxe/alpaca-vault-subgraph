# Alpaca Vault Subgraph

Alpaca Finance is the largest lending protocol allowing leveraged yield farming on Binance Smart Chain. It helps lenders to earn safe and stable yields, and offers borrowers undercollateralized loans for leveraged yield farming positions, vastly multiplying their farming principals and resulting profits.‌ Furthermore, Alpacas are a virtuous breed. That’s why, we are a fair-launch project with no pre-sale, no investor, and no pre-mine. This is a product built by the Alpacas, for the Alpacas.

Deployed at: https://thegraph.com/legacy-explorer/subgraph/nftgalaxy/alpaca-ibalpaca-subgraph

## Contracts:
* ibBNB - 0xd7D069493685A581d27824Fc46EdA46B7EfC0063  5213456
* ibBUSD - 0x7C9e73d4C71dae564d41F78d56439bB4ba87592f 5213616
* ibETH - 0xbfF4a34A4644a113E8200D7F1D79b3555f723AfE  6322674
* ibALPACA - 0xf1bE8ecC990cBcb90e166b71E368299f0116d421 6865780
* ibUSDT - 0x158Da805682BdC8ee32d52833aD41E74bb951E59 7732507
* ibBTCB - 0x08FC9Ba2cAc74742177e0afC3dC8Aed6961c24e7 7771427
* ibTUSD - 0x3282d2a151ca00BfE7ed17Aa16E42880248CD3Cd 8494541

### Model

#### User

* id: User address
* mintCount: User mint times


### Example Queries

- Each address will get a chance to draw from Burger NFT cards for more than 100 BURGER or xBURGER liquidity provided by any one of following trading pairs for 10 days on Liquidity.

Query:
```graphql
{
  user(id: "0x005557a4d27714a764eed9afb2b2e86ac35d6f00") {
    id
    tx
  }
}
```

Sample response data:
```json
{
  "data": {
    "user": {
      "id": "0x00064a106d0596817a9f697f7c5cce32e8286d55",
      "tx": "0xa66005ffc522ef59ad95f745623948ab6cd82a959a2282c719b60242b9a8c291"
    }
  }
}
```

Get claim count expression: 
```javascript
function(data) {
  if (data.user == null) {
    return 0
  }
  return 1
  
}
```
