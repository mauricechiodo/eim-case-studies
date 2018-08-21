---
Title: Facebook
Template: LeafPage
---

#Facebook

##Patent
In 2012, Facebook filed a patent entitled 'Authorization and Authentication Based on an Individual's Social Network', which was then issued in 2015 [1]. 

The primary purpose of the invention described in the patent is to allow an individual to access content through a social network identification. The patent says:
>*"The invention provides a method of authorizing transmission of content to an individual as a way to filter out unwanted communication such as SPAM or content that the individual might find to be offensive, and a method of authenticating individuals for access to content or service that makes the content or service available to more users while limiting access to potentially abusive users of the content or service."*

This is describing **Facebook-Connect**, a single sign-on application that allows users to interact on other websites through their Facebook account. 

The part involving credit rating is only a small section in the patent application:
>*"FIG. 9 is a flow diagram that illustrates the steps carried out in authenticating B for access to a loan. In Step 910, the lender receives a request for a loan from B. The request includes certain identifying information of B, such as B’s e-mail address. In Step 920, in accordance with the methods described in the application, “Method of Sharing Social Network Information with Existing User Databases,” (U.S. patent application Ser. No. 10/854,610, issued as U.S. Pat. No. 8,478,078), filed Jun. 14, 2004, this lender makes a request to a social network database for a graph representation of B’s social network and receives the graph representation of B’s social network. In Step 930, a black list that is maintained for B is requested and received from the social network database in the same manner as in Step 920. In Step 940, a gray list is derived from the black list and B’s social network In Step 950, a breadth first search (or alternatively, a depth first search) is conducted on B’s social network to generate a white list. All members of B’s social network who are connected to B along a path that does not traverse through any unauthorized nodes (i.e., individuals identified in the gray list) get included on this white list. Optionally, the lender may specify a maximum degree of separation value (e.g., N.sub.max). If it is specified, the white list will include only those members of B’s social network who are within N.sub.max degrees of separation from B. In Step 960, the credit ratings of individuals in the white list are retrieved and weighting factors are applied to the credit ratings based on the degree of separation between the individual and B. As an example, a weighting factor of 1/10.sup.N may be applied to the credit ratings, where N is the degree of separation between the individual and B. If the average credit rating is above a minimum score, B is authenticated and the processing of B’s loan application is permitted to proceed (Steps 970 and 980). If not, B is not authenticated, and B’s loan application is rejected (Steps 970 and 990)."*

Below is Fig. 9 in Facebook Patent Application [1].

![Fig. 9 in Facebook Patent Application](http://db716.user.srcf.net/eim/media/Figure9.png "Fig. 9 in Facebook Patent Application")


But what does the above really mean? There are three main steps:
  1. Someone applies for a loan. The application contains the email address.
  2. The bank uses this email address to get a visual representation of the applicant's social network and their friends' credit ratings. 
  3. A decision is taken by the bank to accept or reject the loan based on the friends' credit ratings within a given degree of separation. 
A credit score based soley on your social media network is highly questionable. Can the people who you're friends with on Facebook accurately determine how creditworthy you are? Should we be concerned about the invasion to our privacy that such an invention will cause?  

Unlike other big data applications that collect and anonymise information, "the use of social intelligence for financial ranking is dependent upon personal identification";  the user's entire activity is scanned, including "not only visible online footprints but also private exchanges" [4].

Further, the patent claims that *"a black list that is maintained for B is requested and received from the social network database”*. This means that a bank may be requested to upload the credit ratings of its customers onto Facebook servers. This list will then be maintained by Facebook so the bank will never be allowed to own the results - it will always depend on Facebook to visualise the results.

##Partnership with Banks

On August 6th 2018, The Wall Street Journal published an article [2] claiming that over the past year Facebook has asked JPMorgan Chase & Co., Wells Fargo & Co., Citigroup Inc. and U.S. Bancorp to discuss "potential offerings it could host for bank customers on Facebook Messenger". As an example, Facebook has suggested it could implement a feature on Messenger that would allow uses to check their checking-account balances. 
As part of the deals, Facebook has asked banks for information about "where their users are shopping with their debit and credit cards outside purchases they make using Facebook Messenger". These paternerships are an attempt to increase user engagement by transforming Messenger "into a hub for customer serivce and commerce". 

They have already partnered with PayPal Holdings Inc. which allows users to send money through Messenger [2].

**Why would Facebook want this?** This would allow Facebook to collect data on how users spend their money [3]. This could be paired up with data collected using their patented invention and applied to targeted advertising or even credit scoring.

##References

[1] Christopher Lunt. Authorization and authentication based on an individual's social network, August 2015. 

[2] Emily Glazer, Deepa Seetharaman, and AnnaMaria Andriotis. Facebook to Banks: Give Us Your Data, We'll Give You Our Users. *The Wall Street Journal Online*, August 2018. 

[3] Justin Mauldin. The Bank of Facebook. *TechCrunch*, May 2015. 

[4] Nizan Geslevich Packin and Yafit Lev-Aretz. On Social Credit and the Right to be Unnetworked. *Columbia Business Law Review,* 339, February 2016. 
