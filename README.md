Quadratic programming - Portfolio optimisation

The given assignment is being solved using the Markowitz model for portfolio optimisation, a quadratic optimisation problem using gurobipy library where methods like model and GRB are imported from gurobipy package. The model's components are the objective function, which is used to Minimise the total risk and a convex quadratic function. The constraint issues the budget, if the budget is 1, then it is total investment, the given equation for the Markowitz model is 

minimise    	𝒙 𝑇𝐶𝒙 
subject to   	𝝁 𝑇𝒙 = 𝑟 
		𝒆 𝑇𝒙 = 1, where e = (1, …, 1) T
		 𝒙 ≥ 𝟎
Where is n*n matrix... which measures the covariance among the stocks created from the code using the correlation of i th and j th terms from the (n=8) given assets. Whereas mu is the expected returns, sigma is the portfolio risk of the target returns. There are 25 different targeted return values, and thereby, in the initial task, we have to use these values to plot Sigma on the horizontal axes and mmu on the vertical axis and define its maximum return to minimise the given risk constraints. 

Task 1 
The primary task is to minimise the given level of risk and maximise the returns, which involves selecting the number of each asset in the given portfolio based on their expected returns, variance, and covariance.  


The given returns are arranged from 3 to 9, thereby applying to create a portfolio model, adding variables to the model for spotting the points using addMVar function where n is the number of stocks, Thereby calculating the portfolio risk and setting budget constraints and excepted return constants. The model is optimised for the best point for minimum expected returns and risk values, which are appended for further plotting. 

The plot above illustrates the efficient frontier, curved vertically and along the y-axis. It displays the minimum risk. The horizontal axis displays the portfolio risk, while the second axis interprets the excepted return. The red dot represents the portfolio with the lowest risk with a minimum risk of a standard deviation of 0.72 and an expected return of 5. The blue line is prominent cause it helps determine critical decisions for an investor.  Therefore, a risk-aversive investor would choose a point near the red dot, while a risk-tolerant might choose a point from the graph within its fair site. 

Task 2 
The change done in task 2 is an inequality sign assigned to the budget constraint, where the entire allocated capital is not computed. Although there is a small profit, it's safe to take this strategy as an investor will perceive a low amount of risk. 


The red dot indicates the minimum risk sigma as 0.41, which is very low from the previous graph and 0.72 for the maximum capital allocation, but the expected return is around 3. A risk-aversive investor would look towards the left-hand side rather than the right one since the area displays the least risk. The investor for higher risk will choose the higher efficient frontier with high excepted returns and high portfolio risk. 

Task 3 
In task 3, the inequality is assigned for the expected return, which is greater than and equal to the targeted return.  The change more inclines on the investor’s desire to meet a specific return target but also tends to seek opportunities for potentially higher returns without taking any risk. 




The graph portrays the least risk for achieving the least target return and producing high returns without increasing some fraction of the risk. The main risk point is at sigma 0.72, and mmu is 4.50 as the threshold. It can also benefit from the lower outlining points, which can have better return values. The efficient frontier extends in the first vertical half and consists of several degrees of risks with lower returns. 


Task 4 
Tasks 1 and 4 are the same with minimum risk, even with short selling, which is possible in this scenario by establishing a lower bound. However, the implication is that the maximum risk in task one is higher than that in task 4. Short-selling assets are those that one can take opposing positions in some situations and bet against the time in selling on it in the open market. 




The graph displays minimum risk at 0.65 and an expected return of 5.25. Task 4 is better than Task 1 since the maximum risk is higher in Task 1, which is 3.0 and with a high return value. A greedy investor would choose this approach because, at a lower risk, it's possible to attain a higher degree of excepted return. Also, many levels of max returns contribute to a return of 8, 7 with a lesser risk. 

Conclusion: The Markowitz algorithm proposes that an investor assert the right decision for a perfect outcome with a specific risk level. The gurobi is perfect tool for any investor to navigate the complex trade-off between risk and returns. 




 
