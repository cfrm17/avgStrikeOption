# Average Strike Option Valuation



This article examines the pricing model for Average Strike Option (AVR). For an AVR, the payoff at expiration is determined by an average price and an average strike of the underlying asset over some period prior to expiration.

If average strike is obtained only from historical rates ( ), the AVS option is equivalent to an Average Rate (AVR) option with the strike price equals to the effective strike of the AVS option. 

Some AVR cases can be further reduced to vanilla foreign exchange option (FXO) by choosing one averaging date for the rate. The comparison of AVS and FXO option pricing and USD Delta calculations are done. Note, in FXO pricing window, the only delta calculation is Delta/USD. For comparison with AVS USD Delta, this Delta/USD in FXO is converted into USD Delta by using the relation USD Delta =  Delta/USD. All cases show internal consistency.

Consider a path-dependent European type option.  Notations used as follows.

t	Current time
T	Maturity of the option
 
Base currency
 
Underlying foreign currency
 
Risk free interest rate of the base currency
 
Risk free interest rate of the underlying currency

 
Exchange Rate at time t and   for direct quote
 
Averaging strike start date 
 
Averaging strike end date 
 
Averaging rate start date 
 
Averaging rate end date 
N	Notional

Assuming that   follows a geometric Brownian motion, in  -risk-neutral world, the underlying rate   follows the equation below

                                                           (1)

where  is the volatility of the exchange rate. 

Let the arithmetic averages   and   as

 	,	 

where   and  ’s,  ’s are normalized weights, i.e.  ,   and   ,  . Let the valuation date t = 0. Thus, the underlying rates are known if   for some   or   for some  . 


The currency exchange rate can be either in direct quote (e.g. USD/EUR) or indirect quote (e.g. CAD/USD). Pricing and delta calculations of each case are discussed below. 

Direct quote:   

The payoff currency for direct quote is USD. The notional can be either in EUR or USD.

a.	Notional in EUR:
	
		The payoff of the option at the settlement date is given by

                                                          (2)

where   (1 or –1) is the call/put indicator and the current value of the contract in base currency can be expressed as 

                                          (3)	

where  is the USD risk-free discounting factor and   is the expectation operator in the same world.   explicitly depends on the spot exchange rate  .
The dollar value Delta in USD (called USD Delta) is computed as

USD Delta                                         (4)

where the perturbation on the spot price   is set to be 0.00005. This dollar value delta is used for daily hedging. The Delta/EUR in pricing window does not have any relation to USD Delta value and should not be used in any analysis.

b.	 Notional in USD:
	
	USD Notional is divided by the effective strike,  , to get the payout in USD. The effective strike is the average of historical and/or forward rates of strike averaging dates, and it is also called Avg 1 in the pricing window. Thus, the payoff of the option at the settlement date is given by

 

and the current value of the contract in base currency can be expressed as 

 

USD Delta is computed in the same way using the equation (4). However, the values are different from the ones calculated for EUR notional since   depends on the spot price. 


Indirect quote:   
The payoff currency for indirect quote is USD. The notional can be either in CAD or USD.

c.	Notional in CAD

		The payoff of the option at the settlement date is given by

 

The current value of the contract in base currency can be expressed as 

                                      (5)

The price of the contract and the perturbation of the spot price in delta calculation is in USD/CAD. Thus, the perturbation of the spot is done as   and   where  . Thus, the USD Delta is defined by

USD Delta =                                          (6)

d.	 Notional in USD:
	
	USD notional is multiplied by the effective strike,  , to get the payout in USD. Thus, the payoff of the option at the settlement date is given by

 

the current value of the contract in base currency can be expressed as 

 

USD Delta is computed in the same way as in the equations (6). However, the values are different from the ones calculated for CAD notional since   depends on the spot price. 

You can check other pricing model at https://finpricing.com/lib/FiBond.html 

