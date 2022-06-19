> under construction

#Contents#
* table of contents
{:toc}

## Introduction ##

In [Shulman18](#Shulman18), the authors write 

> One might argue that it would be better to include a separate kind
of type representing objects in the base category, and type constructors represent-ing the functors $p_*$, $p^*$, etc. rather than the monads and comonads they induce. This would be in line with the “judgmental deconstruction” of Reed (2009) that decomposes $\Box$ and $\bigcirc$ into pairs of adjoint functors. It could be that this is indeed better; in fact, the current rules for $\flat$ and $\sharp$ were deduced from a generalization of Reed (2009) developed by Licata and Shulman (2016).

This is an attempt at developing such a [[cohesive homotopy type theory]]. 

## Overview ##

This presentation of [[cohesive homotopy type]] theory is a [[dependent type theory]] consisting of two different kinds of [[types]], __[[spaces]]__ and __[[homotopy types]]__. There exist [[judgments]] 

* for __spaces__
$$\frac{\Gamma}{\Gamma \vdash S\ space}$$

* for __homotopy types__
$$\frac{\Gamma}{\Gamma \vdash T\ homotopy\ type}$$

* for __points__
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash s:S}$$

* for __terms__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash t:T}$$

* for __fibrations__
$$\frac{\Gamma \vdash S\ space}{\Gamma, s:S \vdash A(s)\ space}$$

* for __dependent types__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma, t:T \vdash B(t)\ homotopy\ type}$$

* for __sections__
$$\frac{\Gamma \vdash S\ space}{\Gamma, s:S \vdash a(s):A(s)}$$

* for __dependent terms__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma, t:T \vdash b(t):B(t)}$$

Cohesive homotopy type theory has the following additional judgments, 2 for turning spaces into homotopy types and the other two for turning homotopy types into spaces:

* Every space has an __underlying homotopy type__
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash p_*(S)\ homotopy\ type}$$

* Every space has a __fundamental homotopy type__
$$\frac{\Gamma \vdash S\ space}{\Gamma \vdash p_!(S)\ homotopy\ type}$$

* Every homotopy type has a __discrete space__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash p^*(T)\ space}$$

* Every homotopy type has an __indiscrete space__
$$\frac{\Gamma \vdash T\ homotopy\ type}{\Gamma \vdash p^!(T)\ space}$$

The underlying homotopy type and fundamental homotopy type are sometimes represented by the greek letters $\Gamma$ and $\Pi$ respectively, but both are already used in dependent type theory to represent the [[context]] and the [[dependent product type]]. 

## Modalities ##

From these judgements one could construct the [[sharp modality]] as 
$$\sharp(S) \coloneqq p^!(p_*(S))$$
the [[flat modality]] as 
$$\flat(S) \coloneqq p^*(p_*(S))$$
and the [[shape modality]] as 
$$\esh(S) \coloneqq p^*(p_!(S))$$
for a space $S$. 

## Other types ##

### Path spaces ###
$$\frac{\Gamma, a:S, b:S}{\Gamma \vdash a =_S b\ space}$$

### Identity types ###
$$\frac{\Gamma, a:T, b:T}{\Gamma \vdash a =_T b\ homotopy\ type}$$

### Mapping spaces ###
$$\frac{\Gamma, A\ space, B\ space}{\Gamma \vdash A \to B\ space}$$

### Function types ###
$$\frac{\Gamma, A\ homotopy\ type, B\ homotopy\ type}{\Gamma \vdash A \to B\ homotopy\ type}$$

### Section spaces ###
$$\frac{\Gamma, s:S \vdash A(s)\ space}{\Gamma \vdash \prod_{s:S} A(s)\ space}$$

### Dependent function types ###
$$\frac{\Gamma, t:T \vdash A(t)\ homotopy\ type}{\Gamma \vdash \prod_{t:T} A(t)\ homotopy\ type}$$

### Product spaces ###
$$\frac{\Gamma, A\ space, B\ space}{\Gamma \vdash A \times B\ space}$$

### Pair types ###
$$\frac{\Gamma, A\ homotopy\ type, B\ homotopy\ type}{\Gamma \vdash A \times B\ homotopy\ type}$$

### Total spaces ###
$$\frac{\Gamma, s:S \vdash A(s)\ space}{\Gamma \vdash \sum_{s:S} A(s)\ space}$$

### Dependent pair types ###
$$\frac{\Gamma, t:T \vdash A(t)\ homotopy\ type}{\Gamma \vdash \sum_{t:T} A(t)\ homotopy\ type}$$

### Unit space ###
$$\frac{\Gamma}{\Gamma \vdash \mathbb{1}\ space}$$

### Unit type ###
$$\frac{\Gamma}{\Gamma \vdash \mathbb{1}\ homotopy\ type}$$

## Other properties ##
The fundamental homotopy type of the unit space is equivalent to the unit type. 
$$p_!(\mathbb{1}) \cong \mathbb{1}$$

The product of the fundamental homotopy types of spaces $A$ and $B$ is equivalent to the fundamental homotopy type of the product of spaces $A$ and $B$: 
$$p_!(A \times B) \cong p_!(A) \times p_!(B)$$

## Sources ##

* {#Shulman18} [[Mike Shulman]], Brouwer’s fixed-point theorem in real-cohesive homotopy type theory, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))