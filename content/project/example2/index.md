---
title: "Vector Error Correction Model"
author: "Tshidiso Mofokeng"
date: "2023-12-03T21:13:14-05:00"
links:
- icon: linkedin
  icon_pack: fab
  name: Follow
  url: "https://www.linkedin.com/in/tshidiso-mofokeng-0562861b4/"
- icon: instagram
  icon_pack: fab
  name: Follow
  url: https://www.instagram.com/tshidis_o/
summary: Application of flexible price monetary model to model the long-run steady-state
tags:
- Deep Learning
link-citations: yes
urlcolor: black
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
---

# VECM applied to the South African Rand-US dollar exchange rate

We use the flexible price monetary model specified as:

e<sub>t</sub> = B<sub>1</sub>(m<sub>t</sub> - m<sub>t</sub>\* ) + B<sub>2</sub>(y<sub>t</sub> - y<sub>t</sub>\*),  B<sub>1</sub> \> 0  and  B<sub>2</sub> \< 0

to model the long-run steady-state or equilibrium relationship, where e<sub>t</sub> is the log of the spot nominal bilateral rand-US dollar exchange rate, m<sub>t</sub> - m<sub>t</sub>\* represents the nominal M3 money differential and y<sub>t</sub> - y<sub>t</sub>\* represents the real income differential.

The above theoretical specification relies on three assumptions:

- Stable money demand equations for home (domestic) and foreign countries;

- Long-run Purchasing power parity (PPP);

- Uncovered interest rate parity (UIP) and

- Similar production structures in the home and foreign country.

We departure by inspecting selected macroeconomic variables visually in figure 1.

<figure>
<img src="/VECM/q1.png" alt="Figure 1: Time series for various selected macroeconomic variables, 1979–2022 " />
<figcaption aria-hidden="true">Figure 1: Time series for various selected macroeconomic variables, 1979–2022 </figcaption>
</figure>

Between 1985 and 1994, during the period of economic sanctions, the average economic growth rate was low, with negative growth rates in 1985 and again from 1990 to 1993. As a result, South Africa experienced weaker currency. In the the years 2001/2002 we note currency depreciation of the back of the South African Reserve Bank announcing an intention to close of the net open foreign position, of which contributed to currency depreciation ([South African Reserve Bank 2001](#ref-ReserveBankSA2001)). In the years 2008/2009, there was another depreciation in the currency, which was a factor of global events (specifically from the USA) spilling over into a number of foreign countries including South Africa. In the turn of the 2018 year, the Rand had appreciated strongly to a three-year high with significant signs of recovery in business confidence, following the election of currency president Mr Ramaphosa. Lastly, we note depreciation during the Covid pandemic period given strong uncertainty domestically as well as globally.

Now we will proceed with applying the Phillips-Perron unit root test, to assess the order of integration of the income differential (lrgdp). The results are shown in figure 2.

<figure>
<img src="/VECM/q3.png" alt="Figure 2: Phillips-Perron unit root test " />
<figcaption aria-hidden="true">Figure 2: Phillips-Perron unit root test </figcaption>
</figure>

Now we will proceed with applying the Elliott-Rothenberg-Stock Point-Optimal unit root test, to assess the order of integration of the inflation differential (infl). The results are shown in figure 3.

<figure>
<img src="/VECM/q2.png" alt="Figure 3: Elliott-Rothenberg-Stock Point-Optimal unit root test " />
<figcaption aria-hidden="true">Figure 3: Elliott-Rothenberg-Stock Point-Optimal unit root test </figcaption>
</figure>

Based on the unit root test for the income differential as well as the inflation differential. The summary for the univariate characteristics of selected variables are found in figure 4.

<figure>
<img src="/VECM/q55.png" alt="Figure 4: Summary of univariate characteristics " />
<figcaption aria-hidden="true">Figure 4: Summary of univariate characteristics </figcaption>
</figure>

In this section we desire to test for cointegration. For this, we start by estimating a reduced form vector autoregressive (VAR) model. The existence of cointegration implies that we may proceed to estimate a vector error correction model (VECM).

Here we estimate a reduced form VAR. Furthermore, we allow for four lags and perform a lag selection test. The results from the lag selection test are shown in figure 5.

<figure>
<img src="/VECM/q6.png" alt="Figure 5: Lag selection test " />
<figcaption aria-hidden="true">Figure 5: Lag selection test </figcaption>
</figure>

From figure 5, we will select the lag length of two, which is in agreement with the majority of the selection criteria that is the LogL, LR as well as the HQ. Moreover, we favour the longer lag selection in order to avoid serial correlation which could be present when selecting lag length of one suggested by the SIC, and on the other hand, we avoid issues of multicollinearity with selecting lag length of three proposed by the AIC.

The multivariate cointegration test was an offspring from shortcomings of the Engle-Granger approach. The extension of the multivariate case is, due to the fact that, it is possible for there to be more than two cointegrating vectors. In other words, for n the number of the variables exceeding two in the model, there might form several equilibrium relationships which govern the joint evolution of all the variables. Johansen framework helps overcome the shortcoming. An advantage of this approach is, if there is only one cointegrating relationship rather than two, with the multiple equation approach we can all three differing speeds of adjustment α<sub>11</sub> α<sub>21</sub> α<sub>31</sub>. In that case, α<sub>21</sub> α<sub>31</sub> without loss of generality. Moreover, the Johansen procedure estimates the rank of the cointegration matrix and provides eigenvectors and eigenvalues, from which cointegration relationships can be derived. Overall, there are different tests within the Johansen procedure, such as the Trace test and the Maximum Eigenvalue test, which help determine the number of cointegrating relationships.

According to Asteriou and Hall ([2015](#ref-asteriou2015applied)), we may summarize the five deterministic trend cases as follows:

- Model 1: No intercept or trend in cointegration or VAR (no deterministic components in data or in
  cointegrating vectors – series have zero means)

- Model 2: Intercept (no trend) in cointegration, no intercept or trend in VAR (no deterministic
  trends in the data, first differenced series have zero means; intercept restricted to long run model)

- Model 3: Intercept in cointegration and VAR, no trends in cointegration and VAR (linear trends in levels of
  data, but both specifications allowed to drift around the intercept)

- Model 4: Intercept in cointegration and VAR, linear trend in cointegration, no trend in VAR (trend included
  in cointegration, e.g. technical progress; intercepts in both cointegration and VAR, but no trend in short-run
  relationship)

- Model 5: Intercept and quadratic trend in cointegration; intercept and linear trend in VAR (linear
  trends in short-run model, quadratic trends in cointegration)

We will preferably apply model 2, since it assumes that the data has stochastic trends which includes a constant in long run but no constant in short run. Figure 6 provides confirmation on our model 2 selection. Furthermore, figure 6 indicates that both the trace and maximum eigenvalue test suggest that there is one cointegrating vector present in the data.

<figure>
<img src="/VECM/q7.png" alt="Figure 6: Number of cointegrating relations by model " />
<figcaption aria-hidden="true">Figure 6: Number of cointegrating relations by model </figcaption>
</figure>

In this section we perform a unrestricted cointegration rank test.

  
H<sub>o</sub>: Number of cointegrating vectors is at most equal to 0  

  
H<sub>a</sub>: The number of cointegrating vectors is greater than 0  

According to figure 7, with respect to the trace test, we note that the p-value = 0.0005 &leq 0.05 for this reason we fail to reject the null of zero cointegrating vectors. In addition, for the maximum eigenvalue test, we also note that the p-value = 0.0023 &leq 0.05 and for this reason as well we reject the null of zero cointegrating vectors.

  
H<sub>o</sub>: Number of cointegrating vectors is at most equal to 1  

  
H<sub>a</sub>: The number of cointegrating vectors is greater than 1  

However, for the trace test defining our null hypothesis for at most 1 cointegrating vector. We find that, the p-value = 0.0550 &geq 0.05 meaning we fail to reject the null hypothesis 1 cointegrating vectors in favour of 2 cointegrating vectors. Similarly for the maximum eigenvalue test, we fail to reject the null hypothesis 1 cointegrating vectors in favour of 2 cointegrating vectors. Thus, there exists one unique cointegrating vector between natural log of spot nominal bilateral rand-US dollar exchange rate, broad money (M3) differential and the income differential.

<figure>
<img src="/VECM/q8.png" alt="Figure 7: Unrestricted Cointegration Rank Test " />
<figcaption aria-hidden="true">Figure 7: Unrestricted Cointegration Rank Test </figcaption>
</figure>

In this section we build the vector error correction model (VECM). The results may be seen in figure 8.

<figure>
<img src="/VECM/q9.png" alt="Figure 8: Vector Error Correction Estimates " />
<figcaption aria-hidden="true">Figure 8: Vector Error Correction Estimates </figcaption>
</figure>

The long run equilibrium relationship for a VAR(2) model is given in equation 2 as:

log(RD) = 3.735 + 0.492log(M3) - 2.309log(RGDP)

The interpretation of our results are, 1% rise in the broad money (M3) differential differential will correspond to a 0.492% rise in the spot nominal bilateral rand-US dollar exchange rate, holding all other factors constant. Furthermore, a 1% in the income differential, will translate in a 2.309% fall in the spot nominal bilateral rand-US dollar exchange rate, holding all other factors constant.

The error correction mechanism (speed of adjustment parameter) is α = -0.435 with t-value = -6.666. Since, \|t-value\| = \|-6.666\| \> 1.96, it is statistically and significantly different from zero. In other words, an exogenous shock would return the system back to equilibrium, with the speed of adjustment being moderate.

A few nations which have been labelled to have commodity currency’s are: Australia, New Zealand, Canada as well as South Africa. In the case of South Africa, the multiplier effect of an increase in commodity prices otherwise seen during commodity cycle boom phases, tend to filter into higher export revenue, strength in the currency as well as economic growth. In phases of commodity cycle booms or peaks, there competitive advantage that commodity currency nations receive allows them to benefit from higher export revenue, owing to favourable the favourable commodity prices ([Clements and Fry 2008](#ref-clements2008commodity)). This translates into balancing of trade deficits and in some cases a resulting trade surplus for the respective nation. Intentional investors are likely to be more supportive of a nation that produces trade surpluses as in some cases this may reduce the respective nation’s need to finance pre-existing or even new debt through foreign borrowing at an unfavourable rate. Given the increased export revenues, a favourable perception of foreign investors in combination with a trade surpluses, the currency is likely to appreciate during that period as well. Moreover, the different mechanisms acting in favour of the respective nation would boost government income bigger than expected tax windfalls which translates to overall higher than expected economic growth. However, in the commodity cycle what usually follows after a *peak* is a *trough* and hence this may notably have a negative and reverse effect on the outcomes mentioned above.

We mow proceed with post VECM estimation diagnostic testing for violations of the CRLM assumptions to test for the presence of serial correlation.

<figure>
<img src="/VECM/q13_1.png" alt="Figure 9: LM test for serial correlation " />
<figcaption aria-hidden="true">Figure 9: LM test for serial correlation </figcaption>
</figure>

In figure 9,the Edgeworth expansion corrected likelihood ratio statistic results indicate that the LR test statistic for 1 and 2 lags are 4.125 and 15.388 respectively. Furthermore, the p-values are 0.9030 and 0.6352 which exceed any conventional levels of significance[^1]. Hence, based on this evidence, we fail to reject the null hypothesis that there is no serial correlation at lags 1 to 2. In other words, we conclude that there is no serial correlation at lags 1 to 2.

Next we provide an alternative test on the residuals for serial correlation. Namely, the white test for heteroscedasticity with no cross terms.

<figure>
<img src="/VECM/q14_1.png" alt="Figure 10: White test for heteroscedasticity (with cross terms) " />
<figcaption aria-hidden="true">Figure 10: White test for heteroscedasticity (with cross terms) </figcaption>
</figure>

In figure 10, the reported χ<sub>138</sub> <sup>2</sup> = 135.826 with p-value of 0.5364 which also which exceeds any conventional levels of significance respectively. Hence, we fail to reject the null hypothesis that the residuals is homoskedastic (constant) across all independent variables. Thus, we report that that there is no strong indication of heteroskedasticity detected in the data

In this section we show a graphical comparison between the actual exchange rate value **RD** which is the line in blue and the fitted/estimated (baseline) value which is the line in orange for the period 1979 to 2022, see figure 11.

<figure>
<img src="/VECM/q15.png" alt="Figure 11: Model fit for the spot nominal bilateral rand-US dollar exchange rate " />
<figcaption aria-hidden="true">Figure 11: Model fit for the spot nominal bilateral rand-US dollar exchange rate </figcaption>
</figure>

We now apply a scenario to our VECM model to see how much of a role the commodity price variable played. We exclude in our VECM and illustrate this in figure 12.

<figure>
<img src="/VECM/q16.png" alt="Figure 12: Model fit for scenario to the spot nominal bilateral rand-US dollar exchange rate " />
<figcaption aria-hidden="true">Figure 12: Model fit for scenario to the spot nominal bilateral rand-US dollar exchange rate </figcaption>
</figure>

We find in figure 12 that nearing the end of our sample period, the model over-predicts then under-predicts over time spans. The first instance of this is in 2004 where the VECM is over-predicting then during the Global Financial Crises there is an under-prediction. From the year 2011, the model does well in matching the actual data. However, post 2015 there is spirals of under-predicting then over-predicting once more. This highlights how commodity prices does indeed play a significant role in improving the fit of our model.

# References

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-asteriou2015applied" class="csl-entry">

Asteriou, D, and SG Hall. 2015. “Applied Econometrics Third Edition.” Palgrave Macmillan, London.

</div>

<div id="ref-clements2008commodity" class="csl-entry">

Clements, Kenneth W, and Renée Fry. 2008. “Commodity Currencies and Currency Commodities.” *Resources Policy* 33 (2): 55–73.

</div>

<div id="ref-ReserveBankSA2001" class="csl-entry">

South African Reserve Bank. 2001. “<span class="nocase">Statement of the Monetary Policy Committee : evaluated the monetary policy stance</span>.” 2001. <https://www.resbank.co.za/en/home/publications/publication-detail-pages/statements/monetary-policy-statements/2001/4325>.

</div>

</div>

[^1]: At a 1%, 5% and 10% level of significance.
