> This entry is about the notion of "content" in [[measure theory]]. For the notion in ring theory, see [[content (ring theory)]] and for the notion in [[combinatorics]]/[[representation theory]] set at *[[hook-content formula]]*. For the contents sidebar of this wiki, see *[[contents]]*.  For more disambiguation see *[[content]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


\tableofcontents


## Definition 
 {#Definition}

In [[measure theory]], a __content__ on a [[distributive lattice]] $(L, \leq, \bot, \vee, \top, \wedge)$ is a [[function]] 

$$
  \mu 
    \,\colon\, 
  L \longrightarrow [0, \infty]
$$ 

to the non-[[negative real number|negative]] [[one-sided real number|lower reals]] satisfying:

1. *strictness*, the [[bottom]] element is sent to zero:

   $\mu(\bot) = 0$

2. *additivity*:

   $
   \forall_{a,b\in L}
    \;\;:\;\;
   (a \wedge b = \bot) 
     \implies 
   \big(
     \mu(a \vee b) = \mu(a) + \mu(b)
   \big)
   \mathrlap{\,.}
  $


A content that moreover satisfies the conditions

3. *modularity*: 

   $\mu(a) + \mu(b) = \mu(a \vee b) + \mu(a \wedge b)$

4. *monotonicity*: 

   $(a \leq b) \Rightarrow \big(\mu(a) \leq \mu(b)\big)$

is called a *[[valuation (measure theory)|valuation]]*.


## See also ##

* [[valuation (measure theory)]]

* [[sigma-continuous valuation]]

* [[probability content]]

* [[measure]]

* [[Jordan content]]

## References ##

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Content_(measure_theory)">*Content (measure theory)*</a>