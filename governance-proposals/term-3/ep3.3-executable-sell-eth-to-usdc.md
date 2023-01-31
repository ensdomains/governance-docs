---
description: >-
  This proposal executes a swap of 10,000 ETH into USDC, to ensure ENS DAO has
  enough to cover operating expenses for 18 - 24 months.
---

# \[EP3.3] \[Executable] Sell ETH to USDC

| **Status**            | Pending                                          |
| --------------------- | ------------------------------------------------ |
| **Discussion Thread** | Discuss                                          |
| **Votes**             | Tally                                            |
| **Author**            | [James.eth](https://twitter.com/blockchainjames) |

## Abstract

This proposal executes a swap of 10,000 ETH into USDC, to ensure ENS DAO has enough to cover operating expenses for 18 - 24 months.

## Motivation

The DAO currently keeps almost 100% of its spendable treasury in ETH. While ENS generates protocol revenue in ETH, having so much exposure to a single volatile asset places the DAO in a vulnerable position.

This is a proposal to convert 10,000 ETH into USDC through a Cowswap swap.

10,000 ETH is approximately 25% of the total amount of ETH held by the ENS DAO (wallet.ensdao.eth) and register controller (controller.ens.eth) as of January 18, 2023.

It is hoped that this sale will generate in excess of $13m in USDC. The goal is to ensure that the DAO has enough USDC to cover operations for the next 18 - 24 months.

## Specification

1. Call `withdraw()` on controller.ens.eth (0x283af0b28c62c092c9727f1ee09c02ca627eb7f5)
2. Call `deposit()` on WETH9 (0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2), sending 10,000 ETH
3. Call `approve(<milkman>, 10000 ETH)` on WETH9 (0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2)
4. Call `requestSwapExactTokensForTokens(10000 ETH, <WETH9>, <USDC>, wallet.ensdao.eth, <milkman sushiswap 2% price checker>, 0x)` on milkman (0x11C76AD590ABDFFCD980afEC9ad951B160F02797)

**Addresses:**

* 0xfe89cc7abb2c4183683ab71653c4cdc9b02d44b7 - wallet.ensdao.eth
* 0x283af0b28c62c092c9727f1ee09c02ca627eb7f5 - controller.ens.eth
* 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2 - WETH9
* 0x11C76AD590ABDFFCD980afEC9ad951B160F02797 - milkman
* 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48 - USDC
* 0x00e577093BEA1eb273bc497a61E3F2658369b226 - milkman 2% slippage sushiswap price checker

## Transactions

| Address                                    | Value     | Function                        | Argument          | Value                                      |
| ------------------------------------------ | --------- | ------------------------------- | ----------------- | ------------------------------------------ |
| 0x283Af0B28c62C092C9727F1Ee09c02CA627EB7F5 | -         | withdraw                        |                   |                                            |
| 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2 | 10000 ETH | deposit                         |                   |                                            |
| 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2 | -         | approve                         | guy               | 0x0b7fFc1f4AD541A4Ed16b40D8c37f0929158D101 |
|                                            |           |                                 | wad               | 100000000000000000000000000                |
| 0x11C76AD590ABDFFCD980afEC9ad951B160F02797 | -         | requestSwapExactTokensForTokens | \_auctioningToken | 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2 |
|                                            |           |                                 | amountIn          | 100000000000000000000000000                |
|                                            |           |                                 | fromToken         | 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2 |
|                                            |           |                                 | toToken           | 0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48 |
|                                            |           |                                 | to                | 0xfe89cc7abb2c4183683ab71653c4cdc9b02d44b7 |
|                                            |           |                                 | priceChecker      | 0x00e577093BEA1eb273bc497a61E3F2658369b226 |
|                                            |           |                                 | priceCheckerData  | 0x                                         |
