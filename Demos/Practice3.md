### Problem #11
**a)** Based on the sensitivity report, the solution is degenerate \
**b)** It can increase by $4 based on the sensitivity report \
**c)** Given that $9 is lower then the maxium allowable decrease, no change takes effect \
**d)** There is already extra hours not being used, therefore it would make no sense, and no money would be saved \
**e)** Given there is availability in that specific area, they can reach a maximum of $633.33 in the available cost for saving \
**f)** The spider diagram is created via right clicking on the data and generating the plot, I don't have that plugin available on Linux. That said, given you are following percentage points, the end points should meet at 100%. The first harnessing model is likely the line furthest, then the second and third harnessing model. The wiring models for 2 and 3 would intersect each other. The sensitivty drops in each increment, and I believe the first harnessing model has the most savings potential.
    
### Problem #24
``C$6:E$9`` \
``C$15:E$18`` \
``F$15`` \
``F$16`` \
``F$17:F$18`` \
``C$24:E$27`` \
``C$19`` \
``D19:E19`` \
``F$6:F$19`` \
``G$6`` \
``G$7:G$9`` \
``G$10`` \
Formulas are ``SUM`` and ``PRODUCT`` or ``*`` \
``F15=SUM(C15:D15)`` \
``C19=SUMPRODUCT(C24:C27,C15:C18)`` \
``G6=F6*F15`` \
``G10=SUM(G6:G9)`` \
``Total cost = SUM(G10,SUMPRODUCT(C15:E18,C6:E9)`` \
**a)** You end up getting a non-zero constraint, so it isn't degenerate \
**b)** The optimal value is $44.06774K, and it is non-unique \
**c)** The shadow price is zero at that point, so the recycler wouldn't be willing to pay more \
**d)** The total cost actually increases from $43.9106K to $44.06774K, so obviously not \
**e)** Given the sensitivity report: newsprint is $28.99, packaging is $36.43 and print is $37.70 (rounded) \
**f)** The cost would have to drop by $1.87 to be economical \
**g)** I believe the increase woule be a dollar or 15.38% \ 
**h)** Again w/ the spider diagrams :). The margin implications is that newsprint is cheapest, and the stock print is most expensive. Packaging is near the cost of the stock print.  \
**i)** Same thing w/ f in regards to spider plots, but I believe a carboard increase is most reasonable given it is still already the lowest percentage yield. If you are going by cost over recycling yield, which I guess you are, it is actually the white office paper for newsprint.  
      
### Problem #27
The formulas used were ``SUM``, ``SUMPRODUCT`` and the data model generator w/ solver. I had to input for the cost of each day. \
**a)** Again some people use linux, but for the ``$H$16`` cell for the spider plot for the data, likely the increase would plateau at $1.31K. This will happen around day 7. \
**b)** The total profit is $1,309.90. Part a) is rounded. The capacity is 360Kcf \
**c)** I believe for a 350Kcf unit, the company should pay around $4.214K \
**d)** The company needs to demand to pay at least $1.0598K 
