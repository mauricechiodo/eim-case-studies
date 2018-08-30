---
Title: Futures
Template: ListSubPages
---

# Futures

A futures contract is a contract between two parties where both parties agree to buy and sell a particular 
asset at a specified time in the future.  Financial futures fix the price for interest rates, bonds, 
equities and so on, but trade in the same manner as commodity futures [1].

One common type of futures contract is a Eurodollars futures contract. Eurodollars are time deposits 
denominated in U.S. dollars and held at banks outside the United States. A time deposit is an 
interest-yielding bank deposit with a specified date of maturity. The paper "Understanding Eurodollar Futures" 
helps us to see how Libor and eurodollar futures are related [2]. 
The example the paper gives on page 10 is as follows:

A corporation may arrange a commercial bank loan at Libor rates plus some (fixed) premium that reflects 
the credit status of the corporation, e.g., Libor+50 basis points (0.50%), Libor+125 basis points (1.25%).
As such, the corporation faces the risk of rising rates. On the other hand, an investor or asset manager
planning to purchase the loan, may be concerned about the prospect of declining rates. Say the corporation
anticipates it will require a $\$100$ million loan for a 90-day period beginning in 6 months that will be based 
on the 3-month Libor value, plus a fixed premium. We can calculate the Basis Point Value (BPV) as follows:


$$\text{Basis Point Value} = \text{Face Value} \times (\frac{\text{days}}{360}) \times 0.0001$$ 

$$= $100,000,000 \times \frac{90}{360} \times 0.0001$$ 

$$= $2500$$

where $0.0001 = 0.01% = 1\text{BP}$. Therefore the interest is $\text{Libor}\times\$2500+\text{premium}$. The corporation is concerned that rates may rise before the loan is needed and that it will be required to pay higher interest rates. This exposure may be hedged by selling Eurodollar futures that mature in six months from the current date. One Eurodollar future is based on $\$1$ million face-value, 3-month maturity Eurodollar Time Deposit. If the value of the futures contract should change by one basis point, this equates to $\$25$ movement in the contract value:


$$\text{Basis Point Value} = \text{Face Value}\times(\frac{\text{days}}{360})\times0.0001$$
$$= $1,000,000 \times \frac{90}{360} \times 0.0001$$
$$= $25$$


Therefore if the corporation sells 100 Eurodollar futures, they have counteracted the concern with a rise in Libor which raises the interest rate on the loan by benefiting from a rise in Libor by selling the Eurodollar futures. Similarly, the asset manager planning to purchase the $\$100$ million loan may be concerned that rates will decrease. Thus, the asset manager might buy 100 Eurodollar futures as a hedge. 

A small change in Libor can have a large affect on the money received through interest on a Eurodollar future. Eurodollar future is priced as follows:

$$\text{Price of Eurodollar Future}=$(100-\text{Libor})$$


Say an investor buys a Eurodollar future when Libor is at 4%, so one future costs $\$96$. If Libor changes to 3.98% so that the value of the future is now $\$96.02$, Libor has changed by two basis points, meaning the investor has gained $\$50$ from the interest in the time deposit. As discussed on [another page](https://cueimps.soc.srcf.net/course/course/finance/libor/Scandal/distort), it has been suggested that the value of Libor was manipulated by 8 basis points. It is not difficult to see how much this will have affected the Eurodollars futures market. 

### References
[1] Interest Rate Futures Contracts, Moorad Chourdhry, 2004

[2] Understanding Eurodollar Futures, John W Labuszewski, *CME Group*
