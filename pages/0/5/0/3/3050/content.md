
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

1-categorical [[descent]] can be formulated in several ways, most traditional is due [[Alexander Grothendieck|Grothendieck]] via [[Grothendieck fibration|fibered categories]] $E \to B$ or equivalently [[pseudofunctor]]s. 

**Monadic descent** focuses on a situation in which a morphism $f : b_1 \to b_2$ in the base $B$ induces an [[adjunction]] $F\dashv U$ where 

$$
  F \;:\; E_{b_1} =: A\leftrightarrow B := E_{b_2} \;:\; U
$$ 

and we ask weather $U$ is a [[monadic functor]]. 

## Details

In more detail, the adjunction $F\dashv U$ with unit $\eta:1_B \to UF$ and counit $\epsilon: F U\to 1_A$ induces the [[monad]] $\mathbf{T}= (T,\mu,\eta)$ in $B$ via $T:=U F$, $\mu:=U\epsilon F:U F U F\to UF$ with unit $\eta$. Monad $\mathbf{T}$ generates the [[Eilenberg-Moore category]] $B^{\mathbf{T}}$ of modules (= algebras) over $\mathbf{T}$ that is the pairs $(M,\nu)$ where $M\in Ob(B)$ and $\nu:TM\to M$ satisfies the action axioms $T(\nu)\circ \nu= \nu_T \circ\nu$ and $\nu\circ\eta_M=id_M$. There is a **comparison functor** 

$$ K : A\to B^{\mathbf{T}}, \,\,\,\, K(N) := (U(N),U(\epsilon_N)). $$

We say that the functor $U$ is monadic or more informally that $A$ is monadic over $B$ if the comparison functor is an [[equivalence]] of categories. Sometimes one is interested in a weaker statement weather the comparison functor is fully faithful. 

## Main theorems

The main theorem is Beck's [[monadicity theorem]].

Given a Grothendieck bifibration $p:F\to B$ and a morphism $f:b\to b'$ in the base category $B$, one can choose a direct image $f_!$ and a inverse image functor $f^*$ which form an adjunction $f_!\dashv f^*$. Under some conditions (see [[Benabou-Roubaud theorem]]), the morphism $f$ is an effective descent morphism (with respect to $p$ as a [[fibered category]]) iff the comparison functor for the monad induced by the adjunction $f_!\dashv f^*$ is monadic. 

We should now see that some instances of categories of descent data are canonically equivalent to and can be reexpressed via Eilenberg-Moore categories of monads, or dually comonads. 

## Examples

Descent for a [[Sweedler coring]] is co-monadic descent. See there for more details and geometric interpretations. 

[[!redirects comonadic descent]]