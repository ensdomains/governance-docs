---
description: Ens the $ENS airdrop and EP2 airdrop by transferring tokens and revoking approvals.
---

# \[EP11] \[Executable] End the $ENS and EP2 airdrops

| **Status**            | Active                                                                                                                                      |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Discussion Thread** | [Discuss](https://discuss.ens.domains/t/should-the-dao-end-the-airdrop-on-or-shortly-after-may-4/12047)                                                                                                |
| **Votes**             | [Snapshot](https://snapshot.org/#/ens.eth/proposal/0x718c496b04017fb82749b68570d12f32c839f59b9f9433df127f48bf99121eb7), ends 2022-04-26                                                                                                                                     |

# Abstract
The $ENS airdrop can be terminated at any time on or after May 4, 2022 by a call from the DAO, transferring remaining tokens to an address it specifies. The EP2 airdrop can be terminated at any time by revoking the token approval given to it by the DAO. This EP proposes to execute both of these actions on or shortly after May 4, 2022.

# Specification
 - Call 'sweep' on the ENS token contract, specifying the DAO wallet as target address.
 - Call 'approve' on the ENS token contract, specifying the EP2 airdrop contract and an allowance of 0.

# Transactions
<table>
    <tr>
        <th>Address</th>
        <th>Value</th>
        <th>Function</th>
        <th>Argument</th>
        <th>Value</th>
    </tr>
    <tr>
        <td>0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72</td>
        <td>0</td>
        <td>sweep</td>
        <td>dest</td>
        <td>0xFe89cc7aBB2C4183683ab71653C4cdc9B02D44b7</td>
    </tr>
    <tr>
        <td rowspan=2>0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72</td>
        <td rowspan=2>0</td>
        <td rowspan=2>approve</td>
        <td>spender</td>
        <td>0x4A1241C2Cf2fD4a39918BCd738f90Bd7094eC2DC</td>
    </tr>
    <tr>
        <td>amount</td>
        <td>0</td>
    </tr>
</table>
