# Rules for ENS Service Provider Streams

## 1. Objective
To support service providers contributing to the advancement and sustainability of the Ethereum Name Service (ENS).

## 2. Application and Selection Process
### 2.1 Eligibility and Submission
- Participants must have expertise in blockchain and ENS-related development.
- Submissions must be made on the ENS Forum and include a detailed proposal with objectives, milestones, timelines, and financial requirements.
- For increased transparency and accountability the main receiving address must be an ethereum contract or secure wallet that is directly controlled by the entity and must have its primary ENS name set.
- A Service Provider candidate must alert on their submission any potential conflict of interest or already existing financial relationship to the DAO other related entities. This includes (but is not limited to): a team member is also a Steward or Steward candidate (since Stewards are supposed to oversee Providers); a team member who already receives financial compensation for work related to ENS from another entity already being compensated by the DAO (ENS Labs, Karpatkey, other service providers or service provider candidates) and others. The Meta-Governance Working Group may, at their sole discretion, elect to impose conditions for the participation of the team in the case it is selected.

### 2.2 Calendar and Deadlines
- The first election will take place by a vote of governance token holders using signed messages and will be open for 120 hours, commencing at 9am UTC on December 10, 2023.
- New elections must be held every year, during any period between December 10 of the year following the last election, to May 10 of the next year. The exact dates will fall under the responsibility of the Meta-governance working group, which needs to announce the chosen dates at least 30 days before the election takes place.
- If by May 10 of any given year, a new election has not been announced, then any person can hold a social vote using the ENS Governance tokens to choose the new date, cancel the streams or change the format of the program in any way.
- All active service providers must apply again for the next elections, to show their continuous commitment and have the opportunity to reconsider their requested budget

### 2.3 Proposal Requirements
- The meta-governance working group will release and may amend requirements and a prescribed format for applications.

## 3. Funding Rules and Budget Allocation
### 3.1 Stipulations on Service Fees
- Fees are to be proposed in increments of $100,000 USD per annum, with a cap of $1 million annually.
 - Service providers must commit to operating for at least one year.
 - A service provider who intends to cease operation after a specific date or deliverable must specify this in their application.

### 3.2 Voting Procedure
- The meta-governance working group will, at their sole discretion, curate proposal submissions and determine which will proceed to a vote. They will not unreasonably deny a vote on a valid proposal. 
- In order to be included in the ballot, candidates must include in their submission proof of endorsement of their candidacy of at least 10,000 ENS.
- The meta-governance working group will post a snapshot vote at the end of the application period.
- The snapshot vote will use approval voting, and include every service provider who submitted a valid application for consideration.
- Proposals must secure a minimum of 1 million ENS in approvals.
- A None of the Above option will also exist. Candidates with less approval than the NOTA should be disqualified.
- The meta-governance working group has the right at their own discretion, to change these procedures in minor ways, like switching to another multiple choice voting system (like ranked choice or STAR voting) as they see fit to improve the usability of the procedure, before opening the candidate nomination window for future elections. 

### 3.3 Project Selection
Selection of winning proposals uses the following process:
 - Sort proposals in descending order by the number of votes they received. For each proposal:
   - If the proposal has fewer than 1 million votes, halt and do not consider any further proposals.
   - If the proposal has less votes than the "None of the Above" option, halt and do not consider any further proposals.
   - If the proposal’s requested budget exceeds the remaining budget, skip the proposal and proceed to the next one.
   - Otherwise, add the proposal to the set of selected proposals, and deduct its requested budget from the remaining budget.


## 4. Implementation 

The Stream will be conducted using the SuperFluid protocol. When the selection vote concludes, the following steps will be taken:
A transaction will be prepared that enables the dao to wrap USDC into Super-USDC at an amount that is enough to cover the current budget for 18 months and to create streams for all the winners
The transaction will be put to vote as an Executable Proposal as soon as there has been enough time to properly verify and assert that it is working
If the proposal fails to pass, then a new social vote shall take place later to ratify both the new projects and the Service Providers rules here listed. If it is ratified then a new executable proposal will take place at a later date, if it fails then the election is considered cancelled and a new one, with new rules must be organized.

## 5. Oversight
### 5.1 Responsibility for Implementation
- The Meta-Governance Working Group will be responsible for overseeing the application process, funding distribution, and adherence to these rules starting on 2024, unless they elect to delegate that responsibility to another party.

### 5.2 Oversight
- **The Meta-Governance Working Group holds responsibility for** questions regarding the overall stream and budget allocations. This includes:
- Approval of budget allocations for the service streams.
- Reassessment of budget allocations based on performance reviews and community feedback.
- Addressing any financial discrepancies or concerns raised by the overseeing working groups or community.

- **The Ecosystem working groups holds responsibility for** overseeing the work completed by each provider. These responsibilities include but are not limited to:
  	- Monitoring the progress of the service provider in relation to the goals set out in the proposal.
  	- Facilitating communication between the service provider and the ENS DAO community as a whole.
	- Making sure these meetings are regular and publicly documented ensuring transparency and accountability.
  	- Initiating the termination procedure if the Service provider becomes unresponsive, insolvent, or encounters any major legal or ethical issue that makes the Working Group consider them unfit.
- The Ecosystem Working Group may delegate these responsibilities to other Working Groups if the nature of the service is more aligned with their mandate.

- **The Service Providers holds responsibilities to** commit to their work in their best possible manner and to provide updates on the team progress and goals at least once a quarter in a textual format.


### 5.3 Early Termination procedure
If a Service Provider becomes unresponsive or is deemed unfit by its oversight committee, and attempts to solve the issue privately have failed, then it may initiate the termination process as follows:
Raise the issue on a Working Group call and give a minimum 1 week period for the provider to respond publicly
If the issue is still unresolved, initiate a snapshot vote to remove the Service Provider, with a minimum of 5 days.
If the above vote passes, then an Executable proposal will be made to terminate the stream.

## 6. Output and Licensing
### 6.1 Open Source Requirement
- Service Providers Commit to build projects aligned with the ENS DAO values of Openness and Decentralization, follow proper ENS governance procedure on any major proposal and halt any feature that the community indicates strong objection to.
- All outputs will be licensed under MIT
