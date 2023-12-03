---
bibliography: c:/users/user/onedrive - university of pretoria/tuks/honours/mek 781/macro-modelling economics/project/export.bib
output:
  pdf_document:
    number_sections: true
    latex_engine: pdflatex
    pandoc_args:
      - "--variable=geometry:margin=1in"
      - "--variable=fontsize:11pt"
      - "--variable=mainfont:Times New Roman"
      - "--variable=classoption:justified"
      - "--variable=setspace:stretch=2"
      - "--variable=line-height:1.5"
link-citations: yes
urlcolor: black
---

`\begin{center}   \Huge{\textbf{Decentralized Dynamic General Equilibrium Modeling\\}}   \vspace*{0.5cm}   \Large{\textbf{Tshidiso Mofokeng\\}}   \par   \vspace*{2cm} \end{center}`

`\begin{center} \textbf{Abstract} \end{center}`

<div style="text-align: center; width: 80%;">

This paper investigates contemporary macroeconomics by developing a decentralized dynamic general equilibrium model in MATLAB using Dynare. It focuses on micro-founded technique for modeling real-world business cycles and addresses constraints to understanding and predict economic phenomena. The paper further builds a benchmark DGE model, incorporating a utility function with two state variables, and presents Impulse Response Functions in linearised and log-linearised forms. This offers insights into economic implications of a shock to technology on various macroeconomic variables. The findings were that output, consumption, investment, labour, the rental rate of capital and wages increased in response to a 1% shock in technology. Whereas, the marginal utility of consumption and leisure subsided in response to a 1% shock in technology.

</div>

# Introduction

Contemporary macroeconomics has placed more focus on making use of micro-founded methodology to model relevant real-world situations business cycles. The key ingredient in macro modelling is solving a problem under constraints to address a particular problem at hand. In so doing, a macro model helps us to understand a particular problem in the past or present and to make predictions about the future and also to carry counter factual experiments.

The benchmark model that is built reflects the way current macroeconomic analysis is done at the frontier of macroeconomic research and at central banks and government. This paper sets out to build a decentralised dynamic general equilibrium model (DGE). The primary software used to model outcomes in this study is Dynare, of which runs on MATLAB. Moreover, it is well accepted in the literature as the main program for dynamic stochastic general equilibrium modeling.

The paper firstly sets up the consumers maximum lifetime utility function subject to a budget constraint. Moreover, we include not one but two state variables, that is, capital stock as well as bonds. The underlying assumption of building our model is that along the balanced growth path, the economy does not grow or rather the economy grows at zero. Thereafter, we solve for the steady states of all variables in our model. Subsequently, the model is calibrated which entails finding unique set of model parameters that provide a good description of the system behaviour. Lastly, we provide the Impulse Response Functions in levels, logs as well as the log-linearised form and offer a discussion on the economic meaning.

# Question A

Setting up the consumer’s infinite utility maximization problem in recursive form using bond as an additional state variable. We obtain:

\[
V(k\_{t}, b\_{t}) = *{t=s}^{} *{{c_t, k\_{t+1}, b\_{t+1}}} \[u(c_t) + (k\_{t+1}, b\_{t+1})\]
\]

Since we are given the budget constraint, we insert in into our consumer’s infinite maximization problem to find,

\[
V(k_t, b_t) = *{{l_t, k*{t+1}, b\_{t+1}}} *{t=s}^{} u \[w_tl_t + r_t^k k_t - k\_{t+1} + (1+*k)k_t - b*{t+1} + (1+r_t)b_t + \_t, 1-l_t\] + V(k*{t+1}, b\_{t+1})
\]

Now given the current period utility be of log form as (u(c_t, x_t) = ln(c_t) + ln(x_t)). The two margins w.r.t (c_t) and (x_t) can be written as,

`\begin{align} \frac{\partial u(c_t, x_t)}{\partial c_t} = \frac{1}{c_t} = \lambda_t, \tag{marginal utility of consumption} \label{eq:mu_cons} \end{align}`

and

\[
=
\]

# Question B

We decentralize and solve for two problems. Firstly for the consumer problem, then using the results from the consumer problem, we subsequently solve for the firm problem. Decentralising the consumer and firm problem will allow prices to be made implicit. Taking the first order condition w.r.t (l_t) we get,

\[
w_t + (-1) = 0
\]

Now substituting the two margins from section 2 back into the first order conditions of the consumer’s infinite maximization problem w.r.t (l_t) we obtain,

\[
w_t + = 0
\]

\[
w_t =
\]

\[
\]

\[
\]

This is the marginal product of labour otherwise known as the real wage or the shadow price. Now taking the first order condition of the consumer’s infinite maximization problem w.r.t (k\_{t+1}) we get,

`\begin{align} \frac{\partial u(c_t, x_t)}{\partial c_t} (-1) + \beta \frac{\partial V(k_{t+1}, b_{t+1})}{\partial k_{t+1}} = 0, \tag{1} \label{eq:one} \end{align}`

But,

`\begin{align} \frac{\partial V(k_{t}, b_{t})}{\partial k_{t}} = \frac{\partial u(c_t, x_t)}{\partial c_t} [1 + r_t^k - \delta_k], \tag{by envelope condition} \end{align}`

`\begin{align} \implies \frac{\partial V(k_{t}, b_{t})}{\partial k_{t}} = \frac{1}{c_t} [1 + r_t^k - \delta_k], \tag{using the marginal utility (MU) of consumption} \end{align}`

Hence advancing t to t+1 gives,

\[
= \[1 + r\_{t+1}^k - \_k\]
\]

Substituting Euler equation also known as the intertemporal margin back into equation yields,

\[
(-1) + \[1 + r\_{t+1}^k - \_k\] = 0
\]

Simplifying we obtain,

`\begin{align} \beta \frac{1}{c_{t+1}} [1 + r_{t+1}^k - \delta_k] = \frac{1}{c_t}, \tag{Euler equation} \end{align}`

\[
= =
\]

This is the MRS between consumption today and consumption tomorrow. Hereafter, we take the first order condition of the consumer’s infinite maximization problem w.r.t (b\_{t+1}), of which we obtain,

`\begin{align} \frac{\partial u(c_t, x_t)}{\partial c_t} . (-1) + \beta \frac{\partial V(k_{t+1}, b_{t+1})}{\partial b_{t+1}} = 0, \tag{2} \label{eq:two} \end{align}`

But again,

`\begin{align} \frac{\partial V(k_{t}, b_{t})}{\partial b_{t}} = \frac{\partial u(c_t, x_t)}{\partial c_t} [1 + r_t^k] \tag{by envelope condition} \end{align}`

`\begin{align} \implies \frac{\partial V(k_{t}, b_{t})}{\partial b_{t}} = \frac{1}{ c_t} [1 + r_t^k] \tag{using MU of consumption} \end{align}`

Hence advancing t to t+1 gives,

`\begin{align} \frac{\partial V(k_{t+1}, b_{t+1})}{\partial b_{t+1}} =  \frac{1}{c_{t+1}} [1 + r_{t+1}^k], \tag{3} \label{eq:three} \end{align}`

Substituting equation into equation then yields,

\[
(-1) + \[1 + r\_{t+1}^k\] = 0
\]

Simplifying we obtain,

\[
=   
\]

\[
\]

This is also the MRS between consumption today and consumption tomorrow. Hence from above, we note three consumer equilibrium conditions,

\[
w_t =
\]

\[
= \]

\[
\]

where the discount factor (= ).

\[
=\]

\[
\]

Now consider the firm problem. We are given the production function in terms of the Cobb-Douglas form as (y_t = A_g l_t<sup>k_t</sup>{1-}). We want to maximize profit in the firms problem subject to production. Hence our firm problem becomes,

\[
V(k_t, b_t) = *{{l_t, k*{t}}} \_t A_g l_t<sup>k_t</sup>{1-} - w_t l_t - r_t^k k_t  
\]

Our first order conditions w.r.t (l_t) yield,

\[
= A_g l_t^{- 1} k_t^{1-} - w_t = 0
\]

\[
w_t = A_g l_t^{- 1} k_t^{1-}
\]

Simplifying this yields,

\[
= {l_t^{1-}}
\]

`\begin{align} = \gamma A_g [\frac{k_t}{l_t}]^{1-\gamma}, \tag{real wage} \label{eq:real_wage} \end{align}`

Subsequently, the first order condition w.r.t (k_t) yields,

\[
= A_g l_t^{} k_t^{-} - r_t^k = 0
\]

\[
r_t^k = (1-) A_g l_t^{} k_t^{-}
\]

Simplifying gives us,

\[
= (1-) {l_t^{- }}
\]

`\begin{align} = (1-\gamma) A_g [\frac{k_t}{l_t}]^{- \gamma}\tag{real interest rate} \label{eq:real_interest} \end{align}`

These are our firm equilibrium conditions, that is the real wage and the real interest rate. Overall, taking the first order conditions and solving for the respective variables. We find that the consumer has three equilibrium conditions, on the other hand, the firm has two equilibrium conditions. As a result, we note that decentralising the consumer and firm problem makes prices explicitly known.

# Question C

In this section aims to solve the steady state of all the variables in the model. Assuming net supply/demand of bond (debt) is zero and that productivity ((A = 1)). The firms profit is zero after paying out wages and rents. We are given that consumption and investment are expected to exhaust output, that is (y_t = c_t + i_t). Since savings equals investment in equilibrium we can then rewrite the law of motion of capital w.r.t interest as (i_t = k\_{t+1} - (1-\_k)k_t).

Furthermore, in the case of zero growth, all variables are stationary in the equilibrium. Assuming zero growth would in one case mean that consumption is not growing and so ( = 1). Hence,

\[
1 =
\]

\[
1+= 1 + r\_{t}^k - \_k
\]

\[
r\_{t}^k = + \_k
\]

Returning to the firm equilibrium condition, we found the marginal product of capital to be,

\[
+ *k = r*{t}^k = (1-) A_g \[\]^{- }
\]

Simplifying we obtain,

\[
= \[\]^{ - }
\]

`\begin{align} \frac{k_t}{l_t} = [\frac{\rho + \delta_k}{(1-\gamma) A_g}]^{-\frac{1}{\gamma}},  \tag{capital to labour ratio} \label{eq:kl} \end{align}`

Returning to the budget constraint, recall it was given as,

\[
c_t = w_tl_t + r_t^k k_t - k\_{t+1} + (1+*k)k_t - b*{t+1} + (1+r_t)b_t + \_t
\]

Assuming zero growth implies no change in the capital stock so that ( = 1 k_t = k\_{t+1} ) and ( = 1 b_t = b\_{t+1} ) and the firm makes no profit. Moreover, in steady state for bonds we have (b = 0). We note that capital is constant in equilibrium and so from the law of motion,

\[
i_t = \_k k_t
\]

Furthermore, the consumption demanded now becomes,

\[
c_t = w_tl_t + r_t^k k_t - k\_{t} + (1+*k)k_t - b*{t}
\]

This simplify’s to,

\[
= w_tl_t + r_t^k k_t - \_kk_t
\]

Note from the consumer equilibrium condition, our (MRS\_{c_t, x_t}) in terms of leisure was obtained as,

\[
w_t =
\]

Re-writing this finally yields,

`\begin{align} x_t = \frac{\alpha c_t}{w_t} \tag{4} \label{eq:four} \end{align}`

Since we given that (y_t = c_t + i_t), re-writing this in terms of consumption yields (c_t = y_t - i_t). Since we know our production function and our law of motion in equilibrium, we can represent consumption as (c_t) = (A_g l_t^{} k_t^{1-} - \_k k). Furthermore, taking the equation from the first order condition of the firm is and solving for leisure in equation yields,

\[
x_t =
\]

The time constraint in terms of leisure can be written as (x_t = 1- l_t),

\[
1 - l_t =
\]

\[
l_t = 1 -   
\]

Let
\[
k_t =
\]

where (= ). Recall the equation. Subsequently, simplifying w.r.t (l_t) gives us,

\[
l_t =
\]

Let

\[
= \[\]^{-}
\]

Then we can write (l_t) as

\[
l_t = k_t
\]
Returning to the time constraint in terms of leisure, we can now write this as,

\[
1 - k_t = k_t
\]

Solving for k yields,

\[
1 = k_t + k_t
\]

\[
k_t =
\]

\[
\]

\[
\]

Thus in steady state, after having solved for all the variables in the model, we find 10 variables with 10 equations as:

`\begin{align} \frac{k_t}{l_t} = [\frac{\rho + \delta_k}{(1-\gamma) A_g}]^{-\frac{1}{\gamma}}  \tag{Capital to labour ratio} \end{align}`

`\begin{align} w_t  = \gamma A_g [\frac{k_t}{l_t}]^{1-\gamma} \tag{Real wage}  \end{align}`

`\begin{align} r_t = (1-\gamma) A_g [\frac{k_t}{l_t}]^{- \gamma} \tag{Real interest rate} \end{align}`

`\begin{align} l_t = \frac{k_t}{[\frac{\rho + \delta_k}{(1-\gamma) A_g}]^{-\frac{1}{\gamma}}} \tag{Labour} \end{align}`

`\begin{align} k_t = \frac{\gamma A_g (\frac{k_t}{l_t})^{1-\gamma}}{\gamma A_g (\frac{k_t}{l_t})^{1-\gamma} [\frac{\rho + \delta_k}{(1-\gamma) A_g}]^{-\frac{1}{\gamma}} + \alpha [A_g (\frac{l_t}{k_t})^{\gamma} - \delta_k]} \tag{Captial} \end{align}`

`\begin{align} i_t = \delta_k k_t \tag{Investment}  \end{align}`

`\begin{align} y_t = A_g [\frac{k_t}{l_t}]^{1-\gamma} k_t \tag{Output} \end{align}`

`\begin{align} c_t = A_g [\frac{k_t}{l_t}]^{1-\gamma} k_t - \delta_k k_t \tag{Consumption} \end{align}`

`\begin{align} \lambda = c^{-1} \tag{Marginal utility of consumption}  \end{align}`

`\begin{align} x_t = \frac{\alpha [A_g [\frac{l_t}{k_t}]^{\gamma} k_t - \delta_k k_t]}{ \gamma A_g [\frac{k_t}{l_t}]^{1- \gamma}} \tag{Leisure} \end{align}`

# Question D

In this section we calibrate the parameters pertaining to the technology process, namely the persistence in the process ( *{}) and the volatility of the shock or its standard deviation ( *). We assume that the technology process follows a zero mean autoregressive order one ( AR(1)) process in the form:

\[ log(A_t) = \_{}log(A_t) + \_t\]

Harris ([2015](#ref-harris2015)) proposed an approach to finding ( *{}) and ( *), in the case when the technological process is not observable or there is not any data on it. Since we have data on the real gross domestic product, the labour as well as the capital which is (GDP_t, l_t) and (k_t) respectively.

Let the production function be of Cobb-Douglas form:
\[
yt = A_t l_t<sup>k_t</sup>{1-}
\]

where (A, l_t ) and ( k_t) are the productivity process, labour and capital respectively. We begin by adding a new variable to the original dataset called ( A_t) which is a vector of 288 zeros. Then we add another new variable (= ) which is the labour elasticity that is given or already known. Thereafter, we log our (GDP_t, l_t) and (k_t). We are now in position to build a time series for the technological process that directly estimates the process using the Solow residual ([Harris 2015](#ref-harris2015)). Solow ([1957](#ref-solow1957technical)) recommended, measuring the portion of growth that can be attributable to technological development as output growth that remains unexplained after accounting for input growth. From the production function, solving for ( A_t) returns,

\[
A_t =
\]

Taking the natural log and subsequently applying the laws of logarithms yields,

\[
log(A_t) = log(yt) - log(l_t) - (1-) logk_t
\]

Hence, the previously created variable in our dataset called ( A_t) becomes a function of the above equation. Furthermore, we lag ( A_t) and now define this new variable as,

\[
log(A\_{t-1}) = log(yt) - log(l_t) - (1-) logk_t
\]

Thus, running a regression of (log(A\_{t})) on (log(A\_{t-1})), that is, the estimation of the (AR(1)) process yields the ( *{} = 0.990) and ( *= 0.008), as seen in table .

# Question E

In this section we provide the list of equations that will go into Dynare software. That is, the equations in *levels* of which we will let Dynare do a linearisation around the level of the variables. Using Dynare we will simulate a model with the calibration of parameters given as:

\[
= 0.97,  \_k = 0.03,  = 0.5,  = ,  and  A = 1.
\]

From section 6 we simulated an autoregressive process of order one and found the persistence and standard deviation of the shock parameters to be ( *{} = 0.990) and ( *= 0.008) respectively. Hence, the set of equations for the model are:

`\begin{align} \lambda_t = \lambda_{t+1} \beta[r_{t+1} + 1 - \delta] \tag{Euler equation} \label{eq:intertemporal_margin} \end{align}`

`\begin{align} 1 = x_t + l_t \tag{Time constraint} \label{eq:time_constraint} \end{align}`

`\begin{align} \alpha c_t = x_t w_t \tag{Labour supply} \label{eq:labour_supply} \end{align}`

`\begin{align} k_t = i_t + (1 - \delta)k_{t-1} \tag{Capital accumulation} \label{eq:cap_accum} \end{align}`

`\begin{align} y_t = c_t + i_t \tag{Market clearing} \label{eq:market_clearing} \end{align}`

`\begin{align} y_t = a_t l_t^{\gamma} k_{t-1}^{1 - \gamma}  \tag{Production function} \label{eq:production_function} \end{align}`

`\begin{align} w_t = \gamma a_t l_t^{\gamma} k_{t-1}^{1 - \gamma} \tag{Wage} \label{eq:wage} \end{align}`

`\begin{align} r_t = (1 - \gamma) a_t l^{\gamma} k_{t-1}^{- \gamma} \tag{Capital return} \label{eq:capital_return} \end{align}`

From here, we proceed by reporting the resulting impulse response function subsequent to a one standard deviation shock, in other words a positive one percent technology shock from it’s steady state level, as shown in figure .

`\begin{figure}     \includegraphics{qD.png}     \caption{IRFs to a 1\% technology shock in levels}     \label{fig11} \end{figure}`

From figure , we note that a rise in technology translates to an instant increase in output over the period of 40 periods. We know that output’s two inputs are consumption and investment. Inadvertently, consumption on the one hand has also risen in line with expectation. Owing to higher perceived income from economic agents which evidently rises at a sustained pace, with no indication of return to steady state level at least of the 40 period time horizon. Employment or rather labour is inversely related to leisure. With that said, a positive shock in technology will reduce labour demanded by firms, as a resulted of, more efficient way of producing cars via usage of advanced machinery for instance. Revisiting the inverse relationship, we then expect leisure to rise and labour to fall back toward their steady states after instantly decreasing and increasing respectively.

There is a substitution effect that prevails from the slow to take off but eventually rising rental rate of capital as this translates to lowered discounted price of future consumption. This leads to economic agents postponing their consumption today to the future. Also, we note that rising marginal product of capital paired with the rising consumption will lead to higher investment ([Sims 2017](#ref-sims2017)). On that note, investment instantly rises above its steady state level once the technological shock takes effect, before then embarking on a falling trend over the 40 period horizon. Lastly, there is a instant rise in productivity above steady state, of which starts to taper off at a slow pace, back toward its steady state which displays how strong the persistence in the technology shock is.

# Question F

This section is an extension of the previous section in that here we just apply the logs of the set of equations to our model. Our persistence and standard deviation of the shock parameters still remain the same as estimated from table . Hence, the set of equations for the model are:

`\begin{equation} e^{\lambda} = e^{\lambda_{t+1}} \beta e^{[r_{t+1} + 1 - \delta]} \label{eq:intertemporal_margin1} \end{equation}`

`\begin{equation} 1 = e^{x} + e^{l} \label{eq:time_constraint1} \end{equation}`

`\begin{equation} \alpha e^{c} = e^{x + w} \label{eq:labour_supply1} \end{equation}`

`\begin{align} e^{k_t} = e{i_t + (1 - \delta)k_{t-1}} \label{eq:cap_accum1} \end{align}`

`\begin{equation} e^{y} = e^{c} + e^{i} \label{eq:market clearing1} \end{equation}`

`\begin{equation} e^{y} = e^{a l^{\gamma} k_{t-1}^{1 - \gamma}}   \label{eq:production_function1} \end{equation}`

`\begin{equation} e^{w} = \gamma e^{a l^{\gamma} k_{t-1}^{1 - \gamma}} \label{eq:wage1} \end{equation}`

`\begin{equation} e^{r} = (1 - \gamma)   e^{a l^{\gamma} k_{t-1}^{- \gamma}} \label{eq:capital_return1} \end{equation}`

`\begin{figure}     \includegraphics{qE.png}     \caption{The IRFs to a 1\% technology shock in logs}     \label{fig22} \end{figure}`

From figure , we note that output instantly rises, at just under 0.01%, above steady state and over the time horizon at an increasing rate. Then we capture a instant and above steady state rise as well for consumption. However, the marginal utility of consumption falls instantly and then continues to embark on the falling trend over the 40 period time horizon. Hereafter, we note how leisure upon the shock of technology, begins well below its steady state then for the rest of the time horizon it edges closer toward its steady state. Conversely, labour begins well above its steady state and thereafter tapers down toward its steady state. Investment begins slightly above 0.02% over its steady state, owing to a positive shock in technology, then it slowly reduces over the time horizon in the direction of its steady state. Furthermore, we have the rental rate of capital, which rises over the time horizon above its steady state. Subsequently, we note that productivity begins 0.008% above its steady state, then it reduces at a slow pace toward its steady state as the technological shock fades away. Lastly, wages rise over the time horizon, as seen in figure .

# Question G

Given the main steady states derived in section 5, we now proceed expressing the model in terms of log deviations from its deterministic steady state. This is done by log-linearising the model. The goal with log-linearisation is to solve the model as an approximation around its steady state. Hence, we assume that the steady state is a relevant concept, and look at the dynamics of the model when the economy faces small departures from steady state.

Furthermore, we log-linearise the full model using the following formula as a guide:

`\begin{equation} E_{t} [f(X)] \approx E_{t} [f(\bar X) + \frac{\partial f(X)}{\partial X}  X |_{x = \bar x} \hat x] \label{eq:formula} \end{equation}`

where (X) denotes the variable and (X) its steady state and (log(X) = x) and (x) denotes the log deviation from steady state, i.e (x = log(X) - log(X) = x - x  - 1).

We begin by log-linearising the production function which yields,

\[
y e^{y_t} = a e^{a_t} (l e<sup>{l_t})</sup>{} (k e<sup>{k\_{t-1}})</sup>{1 - }
\]

Note in steady state that ( y = a l^{} k^{1 - } ), which simplifies the above equation to

\[
e^{y_t} = e^{a_t} (e<sup>{l_t})</sup>{} (e<sup>{k\_{t-1}})</sup>{1 - }
\]

Taking the logs of this, we find the log-linearised production function equation to yield,

\[
y_t = a_t + l_t^{} + k\_{t-1}^{1 - }
\]

Next we follow a similar procedure for the equation of real wage,

\[
w e^{w_t} = a e^{a_t} \[\]^{1 - }
\]

Again in steady state, we note that ( w = a \[\]^{1- }), simplifies the equation to,

\[
e^{w_t} = e^{a_t} \[\]^{1 - }
\]

Taking the natural log,

\[
log(e^{w_t}) = log(e^{a_t}) + log(e<sup>{l_t})</sup>{1- } - log(e<sup>{k\_{t-1}})</sup>{1- }
\]

Simplifying this we find ,

\[
w_t = a_t + (1- )k\_{t-1} - (1- )l_t
\]

The log-linearised real wage equation is,

\[
w_t = a_t + (1- )\[k\_{t-1} - l_t\]
\]

Next, we find the log-linearised equation for the capital return otherwise known as the rental rate equation,

\[
r e^{w_t} = (1-) a e^{a_t} \[\]^{}
\]

Once more in steady state, we note that ( r = a \[\]^{ }) which simplifies the equation to,

\[
e^{r_t} = e^{a_t} \[\]^{}
\]

Taking the natural log, we find the log-linearised capital return to be,

\[
r_t = a_t + \]

Proceeding onward, we solve for the log-linearised capital accumulation equation as follows,

\[
k\_{t+1} = (1-) k_t + i_t
\]

Applying yields,

\[
k k\_{t+1} = (1-) k k_t + i i_t
\]

\[
k\_{t+1} = (1-) k_t + i_t
\]

Note in steady state we have (k = (1-) k + i) and also note that ( = ) hence the log-linearised capital accumulation becomes,

\[
k\_{t+1} = (1-) k_t + i_t
\]

Recall the marginal utility of consumption equation is:

\[
\_t = c_t^{-1}
\]

Applying equation on the marginal utility of consumption yields,

\[
= - c c
\]

\[
= - c
\]

Note that in steady state (= (c)^{-1}) and hence we have,

\[
(c)^{-1} = - c
\]

As a result, multiplying throughout by (c) finally yields,

\[
= - c
\]

Next we apply equation on the intertemporal margin which yields,

\[
*t = *{t+1} \]

Next we solve for the log-linearised time constraint equation as follows,

\[
1 = x_t + l_t
\]

Subsequently applying equation we obtain,

\[
0 = x x_t + l l_t
\]

Lastly, we solve for the log-linearised labour supply equation as follows,

\[
c_t = x_t w_t
\]

Applying equation yields,

\[
c c_t = x x_t + w w_t
\]

We note in steady state that the labour supply is (c = x w ). Hence our log-linearised labour supply is,

\[
c_t = x_t + w_t
\]

For our log-linearised market clearing equation we have,

\[
y y_t = c c_t + w w_t
\]

Which can also be written as

\[
y_t = c_t + w_t
\]

Thus the full set of log-linearised equations are given as:

`\begin{align} \hat \lambda_t = \hat \lambda_{t+1} + \hat r_{t+1} [1- \beta (1 - \delta)] \tag{Euler equation} \label{eq:intertemporal_margin2} \end{align}`

`\begin{align} 0 = (\frac{\bar x}{\bar x + \bar l} ) \hat x_t + (\frac{\bar l}{\bar x + \bar l} ) \hat l_t \tag{Time constraint} \label{eq:time_constraint2} \end{align}`

`\begin{align} \hat c_t =  \hat x_t + \hat w_t \tag{Labour supply} \label{eq:labour_supply2} \end{align}`

`\begin{align} \hat k_{t} = (1-\delta) \hat k_{t+1} + \delta \hat i_t \tag{Capital accumulation} \label{eq:cap_accum2} \end{align}`

`\begin{align} \hat y_t = \frac{\bar c}{\bar y} \hat c_t + \frac{\bar w}{\bar y} \hat w_t \tag{Market clearing} \label{eq:market_clearing2} \end{align}`

`\begin{align} \hat y_t = \hat a_t + \hat l_t^{\gamma}  + \hat k_{t-1}^{1 - \gamma}  \tag{Production function} \label{eq:production_function2} \end{align}`

`\begin{align} \hat w_t = \hat a_t + (1- \gamma)[\hat k_{t-1} - \hat l_t] \tag{Wage} \label{eq:wage2} \end{align}`

`\begin{align} \hat r_t = \hat a_t + \gamma[\hat k_{t-1} - \hat l_t] \tag{Capital return} \label{eq:capital_return2} \end{align}`

# Question H

In this last section of the paper, we provide the graphical illustration of the log-linearised IRF in response to the 1% technology shock. Thereafter, briefly discuss if this result should match the one from sections 6 and 7 respectively.

`\begin{figure}     \includegraphics{qH.png}     \caption{IRFs to a 1\% technology shock in log-linearisation}     \label{fig3} \end{figure}`

The 1% impulse in technology on all the other macroeconomic variables generally seems to have the desired effect. In , output continues to rise over the 40 period horizon with the rise of just under 0.01% being similar to that from . Investment declines rises just above 0.02% in response to a 1% shock in technology of which it then declines over the 40 period time horizon toward its steady state. The rise in investment leads to a subsequent rise in consumption, of which it continues to rise with no sign of reverting back to their steady state levels over the 40 period time horizon. Since we expect economic agents to smooth their consumption over time, owing to the positive wealth effect and perceived higher income, we note as the reason why consumption is persistently high. However, as the technological shock dies out they will return back to their steady state.

Owing to the inverse relationship between labour and leisure. A 1% shock in technology results in a increase in labour supply and conversely a reduction in leisure over the 40 period horizon with both returning to their steady state levels overtime. At the initial technology shock, the rental rate of capital marginally rises at just above 0% before embarking on a rising trend, with no indication of of returning to its steady state level, over the time horizon. On the other hand, wages maintains a increase within the bounds of 0.005% and 0.015% over the time horizon, with no indication of returning back to its steady state level as well. Lastly, the technology shock seems fairly persistent, falling at a slow pace over the time horizon, as seen on the productivity IRF in figure .

From figure , the shape of the IRFs of the levels, logs as well as the log-linearised models take on the same shape. However, we note that the results for the log model IRFs and the log-linearised model IRFs match, both of which are different from the level model IRF. In addition, the results are as expected since we did not account for higher order terms in the Taylor expansion. Hence, we obtained a system of linear stochastic difference equations that we could solve for ([Harris 2015](#ref-harris2015)). Moreover, for most of the equations post the log-linearisation procedure, we found the equations to be similar to their original equations or non log-linearised forms.

# Conclusion

In this study, we built a benchmark model by making use of micro-founded methodology to model how various macroeconomic outcomes would be effected post a 1% shock in the technology stock of an economy. We decentralised the representative agent problem for both the consumer and the firm, of which prices (wages and interest) became explicitly defined. A further level of nuance in the model was including not only the capital stock state variable but an additional state variable for bonds.

Moreover, our evidence on a 1% shock was modeled in two folds. Firstly, it was modeled in levels, then in logs and we also made use of a log-linearisation technique. Overall, the shape of the responses of the various macroeconomic variables were all of the same resemblance. However, the interpretation was slightly different across all three categories with respect to the magnitude of the deviation away from the steady state. Since we higher order terms was neglected when log-linearising the model, we found the model in logs and the model log-linearisation were similar by shape and magnitude. However, the log and log-linearised were different in magnitude to when the shock in the model equation, that is the autoregressive order one process was just defined in levels.

Given the high level of persistence we found in table , we note the model display that persistence with the shock in technology taking longer to die out, since the technological shock is only transitory. In other words, the macroeconomic variables in figures , and take prolonged time to return return to steady state. This DGE model was built using Dynare, which is an extension MATLAB. Nonetheless, the economic meaning across all variables in all three models was consistent and in line with expectation. The findings were that output, consumption, investment, labour, the rental rate of capital and wages increased after a 1% shock in technology. Whereas, the marginal utility of consumption and leisure subsided after a 1% shock in technology. Overall, this paper explored on the way current macroeconomic analysis is done at the frontier of macroeconomic research and at central banks and government.

# Appendix

In this section, we present the code to build the time series for the Total Factor Productivity shock as well as the Dynare code for the IRFs.

    ## The following objects are masked from data1:
    ## 
    ##     Capital, Date, gamma, Labour, lCapital, lGDP, lLabour, Price index,
    ##     Real_GDP

`\begin{figure}     \includegraphics{level.png}     \caption{Model in levels}     \label{fig4} \end{figure}`

`\begin{figure}     \includegraphics{log.png}     \caption{Model in logs}     \label{fig5} \end{figure}`

`\begin{figure}     \includegraphics{linearisation.png}     \caption{Model in log-linearisation}     \label{fig6} \end{figure}`

# References

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-harris2015" class="csl-entry">

Harris, D. 2015. “The Real Business Cycle Model.” <http://harrisdellas.net/teaching/semmacro15/rbc.pdf>.

</div>

<div id="ref-sims2017" class="csl-entry">

Sims, Eric. 2017. “Graduate Macro Theory II: The Real Business Cycle Model.” University of Notre Dame; Class Lecture Notes.

</div>

<div id="ref-solow1957technical" class="csl-entry">

Solow, Robert M. 1957. “Technical Change and the Aggregate Production Function.” *The Review of Economics and Statistics* 39 (3): 312–20.

</div>

</div>
