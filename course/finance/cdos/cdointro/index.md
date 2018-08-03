---
Title: CDO Intro and Construction (Jack)
---
[embed "https://www.youtube.com/watch?v=S73swRzxs8Y"] placeholder



For the full in depth document click here (link to full report)

###CDOs DRAFT

In this section, we try to explain some of the basics of CDO structure, and how CDOs are predominantly constructed, as well as delving a little bit into the murkier waters of synthetic CDOs and CDO^2. sources.

The construction method is usually a ‘trial and error’ back-and-forth between the issuer and the ratings agency. Crucial then are the ratings agencies, who determine the risk associated with the asset, via computational simulations, and applications of mathematical models such as the Gaussian Copula. This as we know (link to marias page) was an inappropriate and oversimplified model to use, ultimately leading to a myopic oversight of the actual risk and crude overvaluation of the assets.

The overvaluation of CDOs is at least in part due to inappropriate use mathematics. However, there are widespread claims of human misconduct, in the form of manipulation, and accusation of straight out fraud. 

###The Basics

How are CDOs made? First, the mortgages (assets) are collated and bundled together (usually in the order of hundreds). There may be hundreds of individual mortgages here. The asset pool, is sold and then repackaged into tranches. The idea of the tranches is to create products of differing risk, from the asset pool. First is the senior tranche – these are the secure products, unlikely to default, next the mezzanine tranche, which is slightly riskier, and then the Equity tranche which is the riskiest. These tranches are then sold off to investors.

CDO payments work in a waterfall: The senior tranche will always get paid first, and only after the senior tranche has been made whole, does the mezzanine tranche get paid, and so on. In addition, if there are losses in the asset pool, for example lots of people default on their mortgage payments, the losses are beared by the lower tranches first. This makes the lower tranches much riskier, and so they have a higher yield compared to more senior tranches. NOTE: in video presentation, can use a ‘waterfall’ demonstration to illustrate this. Also, add attachment/detachment points to the diagram, as well as ‘vertical mortgages’

The tranches are constructed by considering total accumulated loss. Say for example if you want the equity tranche to bear 5% of the losses. The first 5% of losses are all beared by the equity tranche, but once losses exceed this, they go to the next tranche up. We call the lower and upper bound of the loss bearing area the attachment/detachment point respectively.

The asset pool does not have to be made up of mortgages, it can be any fixed income asset e.g. credit card loans, bonds etc.

Whilst the asset pool considered as a whole might be a risky BB credit rating, once pool and sliced up, many different products can be made, with varying risk ratings, which can be sold to wider range of investors.

###Synthetic CDOs and CDO2

A synthetic CDO is a CDO whose asset pool has no real cash flow, it is made up of non-cash flow assets. A lot of synthetic CDOs are made up of credit default swaps (CDS). CDSs are insurance against default on credit, for example, if homebuyers default on their mortgaged, a CDS owner will get a payment. Synthetic CDOs can be thought of as a side bet, on the actual mortgages.

A CDO2 is a CDO made from the tranches of other CDOs. This process can then be repeated. If say you have $50 million in sub primes loans being invested in, in reality many times this amount of money may be riding on it through these synthetic CDOs and CDO2.

###How are CDOs constructed?

There is no one way of constructing a CDO, in the same way as say building a house – first you lay the foundations then the bricks etc. Instead, there are different objectives to prioritize, and different lines of approach you can take. Frustratingly, the details of the CDOs we most want to see – that of the big investment banks who were so frequently selling these products – are not publicly available. Since there construction is of vast financial value, they are kept secret. 

Building synthetic CDOs and CDO^2s
CDO^2 are often made out of the “hard-to-sell pieces of the original CDOs” i.e. the riskiest tranches[9]. Moreover, many banks are buying their own CDOs.[9] 

ProPublica also found 85 instances during 2006 and 2007 in which two CDOs bought pieces of each other. These trades, which involved $107 billion worth of CDOs, underscore the extent to which the market lacked real buyers.[9] 

In the past, many banks have been fined for defrauding people into buying low quality mortgage backed securities in the run up to the 2008 financial crisis. [10][11]


Building and risk assessing CDOs is tricky, but not compared to doing that for synthetic CDOs and CDO^2. A 2005 computational study using Monte Carlo simulations done by Nomura (an investment bank) shows that the loss distributions of CDO^2s are very sensitive to small changes in underlying assumptions. This makes intuitive sense, given that the reference pool of a CDO^2 has complex interdependence:

A CDO-squared is very sensitive to the shape of loss distributions of the underlying CDO tranches. The shape of loss distribution reveals the degree of "tail risk," or the likelihood of extreme outcomes. In a CDO-squared, credit risk in the underlying CDO tranches is already "tranched" and another round of tranching is made at the master CDO level. Accordingly, the double-layer structure amplifies the sensitivity of a tranche to various parameters, such as default probability, subordination, etc.[8, pg 4]

This creates issues as seemingly negligible alterations in the underlying assumptions of a credit rating agencies model can have a huge effect on the overall loss distributions, and therefore the ratings. In addition, since different agencies rate based on different things, and underlying assumptions can change agency to agency.

(input the graph)



