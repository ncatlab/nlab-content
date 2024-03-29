
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General

Given a [[fiber sequence]] $F \to A \stackrel{\mathbf{c}}{\to} B$ of [[classifying spaces]]/[[moduli stacks]], hence $[\mathbf{c}]$ a [[universal characteristic class]],  and given an "$A$-structure" in the form of a morphism ([[cocycle]]) $f : X \to A$, then a lift $\hat f$ through $F \to A$ to an "$F$-structure" exists precisely if the induced $B$-structure $\mathbf{c}(f) : X \to B$ is trivializable in $B$-[[cohomology]]. One says that $[\mathbf{c}(f)]$ it is the **obstruction** to lifting the $A$-structure to an $F$-structure.

$$
  \array{
    && F &\to& * 
    \\
    & {}^{\mathllap{\hat f}}\nearrow & \downarrow^{\mathrlap{i}} && \downarrow^{\mathrlap{pt_B}}
    \\
    X &\stackrel{f}{\to}& A &\stackrel{\mathbf{c}}{\to}& B
  }
$$

### Twisted cohomology

Conversely, by the [[universal property]] of [[fiber sequences]], $A$-cocycles are equivalent to $B$-cocycles whose obstruction class under $f$ is trivial. 

Therefore it makes sense to ask for the [[infinity-groupoid]] of $B$-cocycles whose class under $f$ has some other fixed value $\chi$. This gives $\chi$-_[[twisted cohomology]]_ with coefficients in $A$.

### In terms of homotopy type theory

Formulated in [[homotopy type theory]], obstruction theory reduces to a rather simple statement about factorization, or not, of [[functions]] through [[kernels]] of other functions. We spell out some details.

Let $\mathbf{c} : A \to B$ be a [[term]] of [[function type]] and let $pt_B : * \to B$ be a global point of $B$. The [[homotopy fiber|fiber]] of $\mathbf{c}$ over $pt_B$

$$
  F \coloneqq \sum_{a : A} (\mathbf{c}(a) = pt_B)
$$

comes with a canonical "inclusion" function

$$
  i : F \to A
$$

given by

$$
  i : (a, \mathbf{c}(a) \stackrel{\simeq}{\to} pt_B) \mapsto a
  \,.
$$

Now let 

$$
  f : X \to A
$$

be any other function. We are asking for the _obstruction_ to lift it to a function $\hat f : X \to F$ such that 

$$
  i \circ \hat f \simeq f
  \,.
$$

This exists precisely if there is an equivalence

$$
  \phi : \mathbf{c}\circ f \stackrel{\simeq}{\to} pt_B
$$

hence if the obstruction class

$$
  f^* \mathbf{c} \coloneqq \mathbf{c} \circ f
$$

is trivial.

## Examples

### Lift through Postnikov stages

If $F \to A$ in the above is a stage $\tau_{\leq n+1} B \to \tau_{\leq n}B$ in the [[Postnikov tower]] of an object $B$, then the lifting problem is that of lifting through the Postnikov tower of $A$ and the universal obstruction class is that which classified $\tau_{\leq n+1} B \to \tau_{\leq n}B$ as a $\pi_{n+1} B$-[[principal infinity-bundle]].

### Obstruction to extension

The formal dual of the lift obstruction problem discussed above is the following extension problem:

we start with a [[universal characteristic class|universal characteristic map]]

$$
  \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^n A
$$

representing a class $[\mathbf{c}] \in H^n(\mathbf{B}G, A)$ in the $A$-cohomology of $\mathbf{B}G$. Then given a morphism  $\phi : \mathbf{B}G \to \mathbf{B}H$ we may ask for the obstruction to extending $\mathbf{c}$ along it.

Now the statement is: if  $\phi$ is a [[homotopy cofiber|homotopy cofiber]], then there is a good obstruction theory to answer this question. Namely in that situation we are looking at a [[diagram]] of the form

$$
  \array{
    \mathbf{B}Q &\stackrel{f}{\to}& \mathbf{B}G &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^n A
    \\
    \downarrow && \downarrow^{\mathrlap{\phi}} & \nearrow_{\mathrlap{\hat \mathbf{c}}}
    \\
    * &\to& \mathbf{B}H
  }
$$

where the left square is an [[homotopy pushout]]. By its universal property, the extension $\hat {\mathbf{c}}$ of $\mathbf{c}$ exists as indicated precisely if the class

$$
  [f^* \mathbf{c}] \in H^n(\mathbf{B}Q, A)
$$

is trivial.

One class of examples for this sort of situation is where one considers refined [[Lie group cohomology]] on simply connected [[Lie groups]] and is asking for ways to push it down to discrete [[quotients]], hence to non-simply connected Lie groups integrating the same [[Lie algebra]]. This is often phrased in terms of "multiplicative bundle gerbes" over these Lie groups, but that is just another way of talking about the corresponding cohomology of the [[smooth infinity-groupoid|smooth]] [[moduli stack]] $\mathbf{B}G$.

### Obstruction to quantization: Quantum anomaly
 {#QuantumAnomaly}

There are various formalizations of the notion of [[quantization]] in [[physics]], or at least various aspects of that formalization. This involves various steps, some of which may have obstructions to being carried out. In [[physics]] such an obstruction in the process of quantization is often called a [[quantum anomaly]].

For instance for many [[theory (physics)|theories in physics]] the [[action functional]] is a priori not a [[function]] on the [[field (physics)|fields]] but a [[section]] of a circle-[[principal bundle]]. For this to qualify as an action functional therefore one needs a trivialization of that bundle and so the [[Chern class]] of the bundle is the obstruction and hence an _[[quantum anomaly|anomaly]]_ of the system. See there for more.

(...)

[[!redirects obstructions]]
[[!redirects obstruction theory]]