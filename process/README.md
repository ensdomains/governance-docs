---
description: >-
 An overview of the ENS DAO's governance processes and how you can get involved.
---

# Governance Processes

This document is the suggested process for developing and advancing ENS Governance Proposals. It is a living document intended to be owned, modified and enforced by the ENS community.

There are thee working groups categories: [Meta-Governance](https://discuss.ens.domains/c/meta-governance/28),  [ENS Ecosystem](https://discuss.ens.domains/c/ens-ecosystem/32), and [Public Goods](https://discuss.ens.domains/c/public-goods/37). These working groups and ENS DAO members operate according to these governance processes.

## Governance Venues

There are several venues to discuss proposals create, and manage voting on proposals.

### Governance Discussions Venues
- [discuss.ens.domains](https://docs.ens.domains) is a Discourse forum for governance-related discussion. This is the primary channel for governance discussions. Community members must register for an account before sharing or liking posts. Registering for the forum allows community members to post in the general forum, access the working groups, and fill out the [participant request form](https://airtable.com/shrv2xP39SmuCcd5j).

**Note:** The DAO discord also has dedicated social channels for governance discussions, but this is an informal venue. Please refer to the governance forum to initiate and participate in governance discussions.
  
### Proposal Voting Venues
Voting may occur on or off-chain, depending on the nature of the proposal or the governance stage. The official venue for 
  
#### Off-Chain Voting
- [Snapshot](https://snapshot.org/#/ens.eth/) is a simple voting interface that allows users to signal sentiment off-chain. Votes on Snapshot are weighted by the number of ENS delegated to the address used to vote.
-  [Sybil](https://sybil.org/#/delegates/ens) is another alternative interface for managing delegations and conducting off-chain voting.
  
#### On Chain voting
- [Tally](https://www.withtally.com/governance/ens) is a governance portal that allows token holders to delegate their votes and allows delegates to create and vote on binding proposals. This is a popular portal in the ENS DAO.

#### ENS Agora
-  [ENS Agora](https://agora.ensdao.org/) is a bespoke tool created for the ENS DAO that enables members to vote on all types of proposals and manage their delegations. 

\*Note: this is not a complete list and should be updated by the community frequently.
    
## Types of Proposal

There are three main types of governance proposals you can make:

1. **[Social Proposal](social-proposal-template.md)**: This is a proposal that asks for the agreement of the DAO on something that cannot be enforced on chain. Examples of this include a proposal to change the royalty percentage for the ENS secondary market on OpenSea, or a petition to the root keyholders. Social proposals have a quorum requirement of 1% and require a minimum approval of 50% to pass.
3.  **[Executable Proposal](executable-proposal-template.md):** This is a proposal for a series of smart contract operations to be executed by accounts the DAO controls. These can include transfers of tokens as well as arbitrary smart contract calls. Examples of this include allocating funding to a working group multisig wallet, or upgrading an ENS core contract. Executable proposals have a quorum requirement of 1% and require a minimum approval of 50% to pass.
4. **[Constitutional Amendment](constitutional-amendment-template.md)**: This is a social proposal that asks the DAO to amend the constitution. Your draft proposal should include a [diff](https://en.wikipedia.org/wiki/Diff) showing the exact changes you propose to make to the constitution. Rules for amending the constitution are set in the constitution itself, and currently require a quorum of 1% and a minimum approval of two thirds to pass.

## Proposal Phases

### **Phase 1: Temperature Check — Discourse**
The purpose of the Temperature Check is to determine if there is sufficient will to make changes to the status quo.

To create a Temperature Check, ask a general, non-biased question to the community on [discuss.ens.domains](https://docs.ens.domains) about a potential change (example: "Should ENS decrease registration costs for 3-letter domains?"). Forum posts should be in the "DAO-wide -> Temperature Check" category.

Temperature checks are informal and optional; it's up to you to use the feedback to decide if you want to proceed further with your proposal.

### **Phase 2: Draft Proposal — GitHub**
The purpose of the Draft Proposal is to establish formal discussion around a potential proposal.

To create a Draft Proposal, [create a new governance proposal](https://github.com/ensdomains/governance-docs/new/main/governance-proposals) in the governance-docs repository on GitHub. Start by copying the template for an [executable proposal](executable-proposal-template.md), [social proposal](social-proposal-template.md), or [constitutional amendment](constitutional-amendment-template.md), as appropriate. Once you have written your proposal, create a Draft Pull Request for it. Start a new post in the DAO-wide -> Draft Proposals" category with a link to the PR for discussion.

Reach out to your network to build support for the proposal. Discuss the proposal and solicit delegates to provide feedback on it. Be willing to respond to questions on the Draft Proposal topic and in comments on the pull request. Share your viewpoint, although try to remain as impartial as possible.

If your proposal is an executable proposal, you will need to specify the actions your proposal will take while it is in draft stage. You may wish to wait until the proposal is stable before doing this. The executable proposal template explains how to do this.

If your proposal is a constitutional amendment, you must produce a [diff](https://en.wikipedia.org/wiki/Diff) showing the exact changes you are proposing to make. The easiest way to do this is to go to the [constitution](../ens-dao-constitution.md), click "Edit on GitHub", then click the pencil icon to edit the document in a fork. You can then create a pull request via the GitHub UI and include this in your proposal. You should do this in a separate branch to your draft proposal; while the proposal will be merged as soon as it goes to a vote, the amendment will only be merged if the proposal passes.

Once you are confident the proposal is in a stable state, you can proceed to phase 3.

### **Phase 3: Active Proposal — Snapshot / Governance Portal**
Use GitHub to flag your PR as Ready for Review. A contributor will:

1. Merge your PR if it meets the requirements.
2. Assign your proposal a proposal number in the form EP###.
3. Schedule the proposal for a snapshot vote.

If your proposal is a Social Proposal or a Constitutional Amendment, that's it! If the snapshot vote passes, the proposal is passed and you are done.

If your proposal is an Executable Proposal, you will now need to submit it to the governor contract for voting on-chain.

To enact an Executable Proposal:
1. Ensure at least 100k ENS is delegated to your address in order to submit a proposal, or find a delegate who has enough delegated ENS to meet the proposal threshold to propose on your behalf.
2. Call the propose() function of the ENS governor (at [governor.ensdao.eth](https://etherscan.io/address/0x323a76393544d5ecca80cd6ef2a560c6a395b7e3)) to deploy your proposal.

Once the propose() function has been called, a seven-day voting period is started. Ongoing discussion can take place on your proposal post. If the proposal passes successfully, a two-day timelock will follow before the proposed code is executed.

## Getting Work Done
The proposal mechanism by which the DAO gets things done is via a "Request for Proposal" (RFP). An RFP is a request from the DAO for contributors to perform work on its behalf and receive compensation in return.

These are generally competitive with a selection process identified within the RFP. An RFP is appropriate when there is a well-defined task, and a fair process is needed to select one from many persons or organizations to complete it. 

Anyone who identifies a need can write an RFP, and if the RFP is passed, anyone can write a proposal in response and be awarded the work. Even if you believe you can do the work yourself, you will still need to pass an RFP to be awarded the work (and corresponding compensation) by the DAO.

RFPs vary in detail and complexity. An RFP for improving the DAO's documentation may only be a paragraph or two long, and proposals for it will be equally short. At the other extreme, an RFP for managing the DAO's funds may be lengthy, and a successful proposal could be multiple pages justifying the proposer's ability to take on the job. An example RFP that was followed through to completion is the [ENS Endowment RFP](https://discuss.ens.domains/t/ep2-2-4-social-rfp-ens-endowment/14069).


### The RFP Process
All RFPs should follow this process:
 
 1. Write a draft RFP ([template here](rfp-template.md)) and post it as a discussion thread in the appropriate working group on [the DAO forum](https://discuss.ens.domains/). At a minimum, RFPs must contain:

    a. The scope of work and deliverables - Explains the need for the RFP and describes the work to be completed 
    
    b. Criteria for selection- This specifies the requirements for a winning bid.
    
    c. Timeline - Provides a timeline for submissions and completion of the work.
    
    d. RFP Manager - A party who will select a winning bid and approve & disburse compensation. Normally, this will be the working group that adopts the RFP.
    
    e. Budget - A maximum budget for the RFP. 

 3. Incorporate feedback from DAO participants into your draft. When you believe it is ready, tag the stewards of the working group and request they consider adopting it.
 4. If the stewards agree to adopt your RFP, they will decide if it can be paid out of working group funds or necessitates being paid directly from DAO. This latter will require an on-chain executable proposal.

     a. If the RFP can be paid out of WG funds, they will set a submission period and post it as an active RFP.
     
     b. Otherwise, the stewards will create an executable proposal (or, they may ask you to do this) asking the DAO to approve the RFP. The proposal should contain the RFP. The executable component should specify approvals from the DAO funds to the RFP manager in the amount of the maximum budget for the proposal.
 5. Once the RFP is approved - either by the WG or by a DAO-wide vote - the submission period begins. You or a WG steward should create a post on the DAO forum for proposals, and anyone can submit a proposal to this thread.
 6. Once the submission period is concluded, the RFP manager selects a winning bid. Normally the manager will be the stewards of the working group who has adopted your RFP.
 7. The author of the winning proposal commences the work. As they meet milestones specified in the RFP and their proposal, they can request compensation from the RFP manager, who disburses it from the allocated funds.

## Governance Questions
For inquiries about this governance process, please refer to the search tool in the governance forum. You may pose a question in the Meta-Governance or DAO Wide forum category if an answer is not discovered using the search function.


##  **Governance Glossary**

##  Proposal Timelines
Proposalsmust be active for specific durations during the voting process.

| Type of Proposal | Status | Duration of Vote | Timelock |
| ---- | ---- | ---- | ---- |
| Snapshot | Off Chain | 5 Days | N/A |
| Executable | On Chain | 7 days | 2 days |

##  Proposal Quorums
Quorums ensure that the only proposals that pass have adequate voter participation. For quorum to have been reached, an action in the proposal must have over 1M ENS cast.

| Type of Proposal | Quorum % | Amount |
| ---- | ---- | ---- |
| Executable Proposal | 1% | 1M ENS |
| Social Proposal | 1% | 1M ENS |
| Constitutional Amendments | 1% | 1M ENS |

### Terms and Definitions

**Delegation**: ENS holders can only vote or create proposals once they delegate their voting rights to an address. Delegation can be given to one address at a time, including the holder's own address. Note that delegation does not lock tokens; it simply adds votes to the chosen delegation address.

**ENS**: An ERC-20 token that designates the weight of a user's voting rights. The more ENS a user has in their wallet, the more weight their delegation or vote on a proposal holds.

**Executable Proposal**: An executable proposal is a type of proposal that is executed by the governance contract through timelock. It can replace the governance contract, transfer tokens from the community treasury, or perform an almost infinite range of other on-chain actions. In order to create a proposal, an address must have at least 0.1% (100k ENS) of all ENS delegated to their address. Proposals are stored in the "proposals" mapping of the Governor smart contract. All proposals are subject to a 7-day voting period.

**Quorum**: For a vote to pass, a certain percentage of ENS tokens must vote in the affirmative. The current quorum requirements are:

* Executable Proposals: 1%
* Social Proposals: 1%
* Constitutional Amendments: 1%

The purpose of this quorum is to ensure that the only measures that pass have adequate voter participation.

**Timelock**: All governance actions are delayed for a minimum of 2 days by the timelock contract before they can be executed.

**Voting on Executable Proposals**: Users can vote for or against single proposals once they have voting rights delegated to their address. Votes can be cast while a proposal is in the "Active" state. Votes can be submitted immediately using "castVote" or submitted later with "castVoteBySig" (For more info on castVoteBySig and offline signatures, see EIP-712). If the majority of votes (and a 1% quorum of ENS) vote for a proposal, the proposal may be queued in the Timelock.


**Voting Period**: Proposals on Snapshot have a 5-day voting period. Once an executable proposal has been put forward, ENS community members will have a seven-day period (the Voting Period) to cast their votes.
