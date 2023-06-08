---
description: >-
  This proposal requests social approval of ENSIP-15: Normalization Standard.
---

# \[EP3.7] \[Social] Approval of ENS Name Normalization Standard (ENSIP-15)

| **Status**            | Draft |
| --------------------- | --- |
| **Discussion Thread** | [Discuss](https://discuss.ens.domains/t/draft-approval-of-ens-name-normalization-standard/16957/) |
| **Votes**             | Pending |
| **Authors**           | [raffy.eth](https://twitter.com/adraffy), [alisha.eth](https://twitter.com/futurealisha) |

## Abstract
This is a vote to approve [ENSIP-15: Normalization Standard.](https://docs.ens.domains/ens-improvement-proposals/ensip-15-normalization-standard)

## Motivation

### EP3.7 Motivation

* Normalization isn't enforced on-chain. 
* There is no code for the DAO to execute. 
* Approval for ENSIP-15 should be confirmed through a social vote.

### ENSIP-15 Motivation

* Since [ENSIP-1](./ensip-1-ens.md) (originally [EIP-137](https://eips.ethereum.org/EIPS/eip-137)) was finalized in 2016, Unicode has [evolved](https://unicode.org/history/publicationdates.html) from version 8.0.0 to 15.0.0 and incorporated many new characters, including complex emoji sequences. 
* ENSIP-1 does not state the version of Unicode.
* ENSIP-1 implies but does not state an explicit flavor of IDNA processing. 
* [UTS-46](https://unicode.org/reports/tr46/) is insufficient to normalize emoji sequences. Correct emoji processing is only possible with [UTS-51](https://www.unicode.org/reports/tr51/).
* Validation tests are needed to ensure implementation compliance.
* The success of ENS has encouraged spoofing via the following techniques:
	1. Insertion of zero-width characters.
	1. Using names which normalize differently between algorithms. 
	1. Using names which appear differently between applications and devices.
	1. Substitution of confusable (look-alike) characters.
	1. Mixing incompatible scripts.

## Specification
 
* Replace [ENSIP-1 § Name Syntax](https://docs.ens.domains/ens-improvement-proposals/ensip-1-ens#name-syntax) "UTS-46 algorithm" with link to [ENSIP-15](https://docs.ens.domains/ens-improvement-proposals/ensip-15-normalization-standard).
* Agree to normalize names according to ENSIP-15 for a safer end-user experience.
	* Examples:
		1. ![](https://i.imgur.com/VDOnxXe.png)
		1. ![](https://i.imgur.com/tWDRp8H.png)
		1. ![](https://i.imgur.com/OYIigpp.png)
	* Libraries implementing ENSIP-15:
		1. Javascript — [adraffy/ens-normalize](https://github.com/adraffy/ens-normalize.js)
		1. Javascript — [ensdomains/eth-ens-namehash](https://github.com/ensdomains/eth-ens-namehash)
		1. Python — [namehash/ens-normalize-python](https://github.com/namehash/ens-normalize-python)
	* Web Frameworks using ENSIP-15:
		1. Javascript — [ethers/ethers.io](https://github.com/ethers-io/ethers.js/)
		1. Javascript — [web3/web3.js](https://github.com/web3/web3.js)
		1. Javascript — [wagmi-dev/viem](https://github.com/wagmi-dev/viem)
* Names visible to the end-user should be [**beautified**](https://docs.ens.domains/ens-improvement-proposals/ensip-15-normalization-standard#annex-beautification) for a more consistent appearance.
   * Example: These labels are the same:<br><img src="https://i.imgur.com/p7rxUrE.png" width="256">

### Voting 

This vote is a single choice vote. You may vote for one of the following options:
* **For**
* **Against**
* **Abstain**

By voting **For** this proposal, you are voting in favor of approving [ENSIP-15](https://docs.ens.domains/ens-improvement-proposals/ensip-15-normalization-standard).