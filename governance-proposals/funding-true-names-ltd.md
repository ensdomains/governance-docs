---
Description: A proposal to fund TNL for continuing development and improvement of the ENS system.
---

# [Executable] Funding True Names Ltd

| **Status**            | Pending                                                                                                                                      |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Discussion Thread** | [Discuss](https://discuss.ens.domains/t/...)                                                                                                |
| **Votes**             | Pending                                                                                                                                     |

# Abstract

  True Names Ltd (“TNL”) developed the Ethereum Name Service (“ENS”) protocol; continues to manage the development of the ENS Protocol and solely focuses on this work. TNL initiated the creation of the ENS DAO with the object of 1) furthering the development of the ENS Protocol and 2) funding public goods projects.
 
In consideration of the work completed thus far in calendar year 2022 and the work in the months and years to come, per Article III of the ENS Constitution, True Names Ltd respectfully requests a monthly grant of $350,000 USD for continuing development and improvement of the ENS system.

# Specification
We request that the ENS DAO approve a daily grant of $11,500 USDC to True Names Ltd, backdated to January 1st, 2022.

This will be accomplished by approving a dedicated token streaming contract at `0xB1377e4f32e6746444970823D5506F98f5A04201` to spend USDC on behalf of the DAO.

# Transactions
<!-- The transactions section describes all the calls that should be encoded in the onchain version of this proposal. Use the table below as a starting point. -->
<table>
    <tr>
        <th>Address</th>
        <th>Value</th>
        <th>Function</th>
        <th>Argument</th>
        <th>Value</th>
    </tr>
    <tr>
        <td rowspan=2>0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48</td>
        <td rowspan=2>0</td>
        <td rowspan=2>approve</td>
        <td>spender</td>
        <td>0xB1377e4f32e6746444970823D5506F98f5A04201</td>
    </tr>
    <tr>
        <td>value</td>
        <td>0xffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff</td>
    </tr>
</table>
