# Contents
* toc
{: toc}

## Idea
 
We wish to more generally discuss the criterion in the [[Landweber exact functor theorem]]. Rather than looking at formal groups classified by maps from $Spec(R) \to M_{fg}$ that are **etale**, we look at p-divisible groups classified by maps from $Spec(R) \to M_{p-div}$ which are **unramified**. 

Lurie defines the condition for a [[p-divisible group]] $G$ over $R$ to be nonstationary. Heuristically, we think of $G$ as a family of p-divisible groups parameterized by $Spec(R)$. The concept of $G$ being nonstationary is that this family is _nonconstant along every tangent vector_ in $Spec(R)$. 
This is equivalent to the map classifying $G$ from $Spec(R) \to M_{p-div}$ being unramified.


## Definition

Let $R$ be a commutative ring and let $G$ be a p-divisible group over $R$. Let $\kappa(x)$ be the residue field of $R$ at $x \in |Spec(R)|$.

Let $G$ be a p-divisible group defined over a commutative ring $R$. Suppose that we are given a point $x \in |Spec(R)|$ and a derivation $d: R \to \kappa(x)$, then the canonical map $\beta_0: R \to \kappa(x)$ lifts to a ring homomorphism $\beta: R \to \kappa(x)[\epsilon]/(\epsilon^2)$, given by the formula $\beta(t) = \beta_0(t) + \epsilon dt$. 

Let $G_d$ denote the p-divisible group over $\kappa(x)[\epsilon]/(\epsilon^2)$ obtained from $G$ by extending scalars along $\beta$.

We say $G$ is **nonstationary** if: 

* For every point $x \in |Spec(R)|$ and every nonzero derivation $d: R \to \kappa(x)$. the p-divisible group $G_d$ is a nontrivial first order deformation $G_{\kappa(x)}$. 

(If the map $d = 0$, then $G_d$ is a trivial first order deformation of $G_{\kappa(x)}$). 
