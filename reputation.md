
# Reputation System for crypto.camp 

###### motivation 
The main goal of system is to create a community of experts which votes for the projects or any other content is trustful. All symmetric reputation systems are proven to be sybil-vulnerable. So we need to make a sybil creation unaffordably expensive or use some sybil-protection mechanisms.

###### actors 
One of the mechanisms to create sybil-proof system is to set some seed. We need an initial reputation which is set to some actors whose identity is proven.
Such actors can be project owners and some kernel of community.
Every actor should be able to post some content, both articles or comments. Their reputation or karma depends on votes given by other actors to the posted content.
Also, every user, maybe after some preconditions, should be able to review projects and get an approves from the project owners.

###### problems 
   -	Sybil attack
   -	Allowance to vote to users who are affilated with some project or content author. How to distinguish opinion from biased vote?
   -	More sophisticated sybil-attack, where sybils are reposting good comments or posts
   
###### structure
- Ways to prove an identity.
- Karma growing curve.


###### terms 
*describe each*

- Project (camp)
- User
- Karma
- Vote
- Kudos

###### problems to solve

Second season of hack.ether.camp was using the links to social accounts as primary prove of identity. Using the platforms like microworkers.com camp owners could create bot-like voting accounts for 0.5-1 USD each. Let's take that we need sybil cloud size larger then than half of honest voting community.
If we will require more sophisticated proof of identity and the price will increase up to 10 USD, attacker will need to pay around 1500 USD to perform his attack.
We need to determine if sybil attack price is high enough.

Also, most of the votes for the top camps were given by users which were registered at less then one day before vote. Obviously, most of them were affilated with project in some way. Such way of voting helps to win heavily promoted camps which are not always the best. So, we need to put some barrier for the newcomers. They have to prove their potential value for the community before receiving voting rights.


##### Content posting and upvoting rewards

Good content should be rewarded. 


##### Karma gain system

Statuses:
1. Newcomer, karma 0-99, max gain daily 20.
2. Voter, karma 100-5000, can vote for the projects and content, max gain daily 100.
3. Elder, karma >5000, can also downvote content or even punish the untrustful users. Karma >5000 cannot affect your project voting power, it's only applyable to content moderation.

Every normal person starts with 0 karma. It should be quite hard to get a voter status, because newcomers cannot harm the system badly. They only can create a number of spam posts which can be easily hidden by other users. 
There should be some automated spam filter which can be optionally enabled by any user to hide
**Should there be a mechanism of automated massive downvote of spammers gang?

To get some karma you have to get at least 2 upvotes. 
Karma gain formula: **(voter karma) / 25**

There can be activity coefficient which will reward constantly high activity, like +2% to karma if there were upvoted content in the last days, up to 10%, or decrease up to 10% if there was no activity in last 5 days.

Social accont link can be some prove of your identity, so it will give you **+5%** to karma grow per each linked account with more than 100 followers.

After 3 days in a row of upvoting specific person by another specific person there should be cooldown for 1 or 2 days. So one user cannot be upvoted too much by single voter or even elder. 

Karma growth can be boosted during the first weeks or months after the system launch to help the community grow more intensively.

**Hide button**
If voter considers that some content is spam or offensive, he can press 'Hide' button, so he will not see this comment or post in the future. After getting *(voters karma) / 25 == 100* the author of content gets a cooldown for karma acquiring for 1 day. (Effect can be worse if he will get more 'spam' flags).

##### Kudos as karma function

Kudos amount is a linear function from karma.

*kudos = karma / 10

##### Project reviews
Every user can write a review to any published project. Any owner of this project can approve the review and make it visible to other community members (*should the review be hidden before the approve or there should be another tab for unapproved reviews?*). An author of the review receives some fixed amount of karma in the case of approve. It can be max daily amount for a newcomer, 20 karma.
All the reviews can recieve normal votes from the community after the approval like any other post or comment.

Project reviews suppose to be a mechanism which will help to accumulate initial karma value by community new members. 

**Should there be overall karma daily limit? Can there be some attack on it if many bots drain all the daily karma?






##### Notes on technical implementation
Speaking of implementation of this system it looks that best option will be pluggable contracts system. All the karma and kudos gain coefficients should be stored in separate structures. System should be changeable by submitting proposals which can be accepted or declined by the community. Approved proposal will be inserted in an array of proposals. Proporsal can be removed from an array by similiar procedure.

**External tools**

All contract data is open, so any user is able to analyze the interactions between actors. External social graph analyzing tool can be a good help for an ordinary user who wants to see if there are exist evidences of unfair interaction. E.g. user can see if there are sybil clusters and who is a owner of this cluster. None of this tools can be a automated judge which changes some user karma, but it may advise to do so. 
