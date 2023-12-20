---
date: "2023-12-03T00:00:00Z"
external_link: ""
image:
  caption: 
  focal_point: Smart
summary: Building a benchmark DGE model, incorporating a utility function with two state variables, and presenting the Impulse Response Functions in linearised and log-linearised forms.
tags:
- Deep Learning
title:  Decentralized Dynamic General Equilibrium Modeling
---


<div style="text-align: center; width: 80%;">

This paper investigates contemporary macroeconomics by developing a decentralized dynamic general equilibrium model in MATLAB using Dynare. It focuses on micro-founded technique for modeling real-world business cycles and addresses constraints to understanding and predict economic phenomena. The paper further builds a benchmark DGE model, incorporating a utility function with two state variables, and presents Impulse Response Functions in linearised and log-linearised forms. This offers insights into economic implications of a shock to technology on various macroeconomic variables. The findings were that output, consumption, investment, labour, the rental rate of capital and wages increased in response to a 1% shock in technology. Whereas, the marginal utility of consumption and leisure subsided in response to a 1% shock in technology.

</div>

# Introduction

Contemporary macroeconomics has placed more focus on making use of micro-founded methodology to model relevant real-world situations business cycles. The key ingredient in macro modelling is solving a problem under constraints to address a particular problem at hand. In so doing, a macro model helps us to understand a particular problem in the past or present and to make predictions about the future and also to carry counter factual experiments.

The benchmark model that is built reflects the way current macroeconomic analysis is done at the frontier of macroeconomic research and at central banks and government. This paper sets out to build a decentralised dynamic general equilibrium model (DGE). The primary software used to model outcomes in this study is Dynare, of which runs on MATLAB. Moreover, it is well accepted in the literature as the main program for dynamic stochastic general equilibrium modeling.

The paper firstly sets up the consumers maximum lifetime utility function subject to a budget constraint. Moreover, we include not one but two state variables, that is, capital stock as well as bonds. The underlying assumption of building our model is that along the balanced growth path, the economy does not grow or rather the economy grows at zero. Thereafter, we solve for the steady states of all variables in our model. Subsequently, the model is calibrated which entails finding unique set of model parameters that provide a good description of the system behaviour. Lastly, we provide the Impulse Response Functions in levels, logs as well as the log-linearised form and offer a discussion on the economic meaning.

# Section 2

Setting up the consumer’s infinite utility maximization problem in recursive form using bond as an additional state variable. We obtain:

```latex
{{</* math */>}}
$$f(k;p_{0}^{*}) = \begin{cases}p_{0}^{*} & \text{if }k=1, \\
1-p_{0}^{*} & \text{if }k=0.\end{cases}$$
{{</* /math */>}}
```


{{</* math */>}}
$V(k\_{t}, b\_{t}) = *{t=s}^{} *{{c_t, k\_{t+1}, b\_{t+1}}} \[u(c_t) + (k\_{t+1}, b\_{t+1})$
{{</* /math */>}}


Since we are given the budget constraint, we insert in into our consumer’s infinite maximization problem to find,

{{</* math */>}}
$$V(k_t, b_t) = *{{l_t, k*{t+1}, b\_{t+1}}} *{t=s}^{} u \[w_tl_t + r_t^k k_t - k\_{t+1} + (1+*k)k_t - b*{t+1} + (1+r_t)b_t + \_t, 1-l_t$$ + V(k*{t+1}, b\_{t+1})
{{</* /math */>}}

Now given the current period utility be of log form as (u(c_t, x_t) = ln(c_t) + ln(x_t)). The two margins w.r.t (c_t) and (x_t) can be written as,