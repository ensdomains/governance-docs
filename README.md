---
description: >-
  An overview of the ENS DAO's governance processes, and how you can get
  involved.
---

# Governance Process



This document is a suggested process for developing and advancing ENS Governance Proposals. It is a living document intended to be owned, modified and enforced by the ENS community.

## Venues

[discuss.ens.domains](./#process) is a Discourse forum for governance-related discussion. Community members must register for an account before sharing or liking posts. Registering for the forum allows community members to post in the general forum; for access to the working groups, fill out the [participant request form](https://airtable.com/shrv2xP39SmuCcd5j).

There are four workstream categories: [Meta-Governance](https://discuss.ens.domains/c/meta-governance/28), [Community](https://discuss.ens.domains/c/community/12), [ENS Ecosystem](https://discuss.ens.domains/c/ens-ecosystem/32), and [Public Goods](https://discuss.ens.domains/c/public-goods/37). Each category has subcategories for each of the steps of the governance process described below.

### Snapshot

[Snapshot](https://snapshot.org/#/ens.eth/) is a simple voting interface that allows users to signal sentiment off-chain. Votes on snapshot are weighted by the number of ENS delegated to the address used to vote.

### Governance portals

[Tally](https://www.withtally.com/governance/ens) is a governance portal that allows token holders to delegate their votes, and allows delegates to create and vote on binding proposals.

There are also other governance interfaces that users can use to cast their votes:

* [Sybil](https://sybil.org/#/delegates/ens)

\*Note: this is not a complete list, and should be updated by the community frequently.

## Process

### Types of Proposal

There are three main types of governance proposal you can make:

1. **Executable Proposal:** This is a proposal for a series of smart contract operations to be executed by accounts the DAO controls. These can include transfers of tokens as well as arbitrary smart contract calls. Examples of this include allocating funding to a workstream multisig wallet, or upgrading an ENS core contract. Executable proposals have a quorum requirement of 1% and a require a minimum approval of 50% to pass.
2. **Ordinary Proposal**: This is a "social proposal" that asks for the agreement of the DAO on something that cannot be enforced onchain. Examples of this include a proposal to change the royalty percentage for the ENS secondary market on OpenSea, or a petition to the root keyholders. Ordinary proposals have a quorum requirement of 1% and require a minimum approval of 50% to pass.
3. **Constitutional Amendment**: This is a "social proposal" that asks the DAO to amend the constitution. Your draft proposal should include a [diff](https://en.wikipedia.org/wiki/Diff) showing the exact changes you propose to make to the constitution. Rules for amending the constitution are set in the constitution itself, and currently require a quorum of 1% and a minimum approval of two thirds to pass.

### **Phase 1: Temperature Check — Discourse**

The purpose of the Temperature Check is to determine if there is sufficient will to make changes to the status quo.

To create a Temperature Check, ask a general, non-biased question to the community on [discuss.ens.domains](./#venues) about a potential change (example: “Should ENS decrease registration costs for 3-letter domains?”). Forum posts should be in the "Temperature Check" subcategory of the appropriate workstream.

Temperature checks are informal; it's up to you to use the feedback to decide if you want to proceed further with your proposal.

### **Phase 2: Draft Proposal — Discourse**

The purpose of the Draft Proposal is to establish formal discussion around a potential proposal.

To create a Draft Proposal, create a new topic in the Draft Proposals subcategory of the appropriate workstream, using the template pinned to the top of the category. Link to your temperature check thread in the proposal draft; draft proposals that were not preceded by a temperature check may be removed by moderators.

Reach out to your network to build support for the proposal. Discuss the proposal and solicit delegates to provide feedback on it. Be willing to respond to questions on the Consensus Check topic. Share your view point, although try to remain as impartial as possible.

If your proposal is an exectuable proposal, you will need to write the code for your proposal while it is in draft stage. You may wish to wait until the proposal is stable before doing this. Documentation on composing a proposal can be found [here](https://docs.openzeppelin.com/contracts/4.x/governance#proposal\_lifecycle).

If your proposal is a constitutional amendment, you will need to produce a diff showing the exact changes you are proposing to make. The easiest way to do this is to go to the [constitution](ens-dao-constitution.md), click "Edit on GitHub", then click the pencil icon to edit the document in a fork. You can then create a pull request via the GitHub UI and include this in your proposal.

Once you are confident the proposal is in a stable state, you can proceed to phase 3.

### **Phase 3: Governance Proposal — Discourse / Governance Portal**

The first step in passing your governance proposal is to create a vote on [snapshot](https://snapshot.org/#/ens.eth). Request that an editor advance your proposal to a vote. They will:

1. Move your proposal from Draft Proposals to Active Proposals.
2. Assign your proposal a proposal number in the form EP###.
3. Create a snapshot vote for your proposal with a duration of 5 days, and link to it from your proposal post.

If your proposal is an Ordinary Proposal or a Constitutional Amendment, that's it! If the snapshot vote passes, the proposal is passed and you are done.

If your proposal is an Executable Proposal, you will now need to submit it to the governor contract for voting onchain.

To enact an Executable Proposal:

1. Ensure at least 1 million ENS is delegated to your address in order to submit a proposal, or find a delegate who has enough delegated ENS to meet the proposal threshold to propose on your behalf.
2. Call the propose() function of the ENS governor (at [governor.ensdao.eth](https://etherscan.io/address/0x323a76393544d5ecca80cd6ef2a560c6a395b7e3)) to deploy your proposal.

Once the propose() function has been called, a seven day voting period is started. Ongoing discussion can take place on your proposal post. If the proposal passes successfully, a two day timelock will follow before the proposed code is executed.

## **Governance Glossary**

**ENS**: An ERC-20 token that designates the weight of a user’s voting rights. The more ENS a user has in their wallet, the more weight their delegation or vote on a proposal holds.

**Delegation**: ENS holders cannot vote or create proposals until they delegate their voting rights to an address. Delegation can be given to one address at a time, including the holder’s own address. Note that delegation does not lock tokens; it simply adds votes to the chosen delegation address.

**Executable Proposal**: An executable proposal is a type of proposal that is executed by the governance contract through timelock. It can replace the governance contract, transfer tokens from the community treasury, or perform an almost infinite range of other on-chain actions. In order to create a proposal, an address must have at least 0.1% (100k ENS) of all ENS delegated to their address. Proposals are stored in the “proposals” mapping of the Governor smart contract. All proposals are subject to a 7-day voting period.

**Quorum**: In order for a vote to pass, a certain percentage of ENS tokens must vote in the affirmative. The current quorum requirements are:

* Executable Proposals: 1%
* Ordinary Proposals: 1%
* Constitutional Amendments: 1%

The purpose of this quorum is to ensure that the only measures that pass have adequate voter participation.

**Voting on Executable Proposals**: Users can vote for or against single proposals once they have voting rights delegated to their address. Votes can be cast while a proposal is in the “Active” state. Votes can be submitted immediately using “castVote” or submitted later with “castVoteBySig” (For more info on castVoteBySig and offline signatures, see EIP-712). If the majority of votes (and a 1% quorum of ENS) vote for a proposal, the proposal may be queued in the Timelock.

**Voting Period**: Proposals on Snapshot have a 5 day voting period. Once an executable proposal has been put forward, ENS community members will have a seven day period (the Voting Period) to cast their votes.

**Timelock**: All governance actions are delayed for a minimum of 2 days by the timelock contract before they can be executed.
