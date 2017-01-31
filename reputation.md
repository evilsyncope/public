
# Reputation System for crypto.camp 

###### motivation 
The main goal of system is to create a community of experts which votes for the projects or any other content is trustful. All symmetric reputation systems are proven to be sybil-vulnerable. So we need to make a sybil creation unaffordably expensive or use some sybil-protection mechanisms.
###### actors 
One of the mechanisms to create sybil-proof system is to set some seed. We need an initial reputation which is set to some actors whose identity is proven.
Such actors can be project owners and some kernel of community.
Every actor should be able to post some content, both articles or comments. Their reputation or karma depends on votes given by other actors to the posted content.
Also, every user, maybe after some preconditions, should be able to review projects and get a recognitions (sort of votes) from project owners.
###### problems 
   -	Sybil attack
	-	Allowance to vote to users who are affilated with some project or content author. How to distinguish opinion from biased vote?
	-	More sophisticated sybil-attack, where sybils are reposting good comments or posts
###### structure
Prove of identity by depositing some currency.
Amount of deposit.
Karma growing curve. Karma can decay depending on time, but it can be gamed by posting some good content in moments when you need your karma. If karma growth slows after some point it will be better to create another actor with pseudonyme, so growth should be linear.
###### terms 
###### problems to solve





***

Last discussion to organize: 

1. Project reviers - content that is valuable and hard to fake
2. Deposit HKG as source of potentical to get karma
3. Grow of the carma is by X^2 formula where X is your deposit - makes it better to develop 1 account
   a. Should we constrain the maximal value?
   b. Will the karma be valuable as representation of user's social activity in reviewing and creating good content? It can became a sort of oligarchy where voice of users with more HKG is much more powerful.
4. The quality of content is validated by projects (we can call it - reveiw recognision)
   a. projects care about their reputation - will not publicly promote bad reviews 
   b. how to prevent fake projects to submit? - possilbe that by approving project submissions.
   c. When it's time to review the project? At the start when there is no commits or any other useful activity, fake project can look like normal one.
   
   
--------
1. Project reviwers - content that is valuable and hard to fake
   a. Can be not so hard, because most maleficient camp was looking normal before the voting bots attack started.
3. Grow of the carma is by X^2 formula where X is your deposit - makes it better to develop 1 account
   a. Should we constrain the maximal value?
   b. Will the karma be valuable as representation of user's social activity in reviewing and creating good content? It can became a sort of oligarchy where voice of users with more HKG is much more powerful.
   c. Formula should be proven by some facts, like how much it will cost to create a bots.
   d. What if such user can be bribed? He can receive some money for himself and for the deposit.
4. The quality of content is validated by projects (we can call it - reveiw recognision)
   c. When it's time to review the project? At the start when there is no commits or any other useful activity, fake project can look like normal one.
