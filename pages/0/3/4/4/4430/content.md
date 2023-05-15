
#Contents#
* table of contents
{:toc}

## Idea

The __center of an [[additive category]]__ $A$ is the [[endomorphism ring]] of the [[identity functor]] $Id_A$ (cf. with [[center]]). 

In general, the center is not functorial, but it is functorial in some important special circumstances, like some reconstruction theorems in the commutative setup.  (It is also functorial on [[equivalence of categories|equivalences]].)

## Examples

\begin{proposition}\label{CenterOfRModIsR}
Let [[Mod|$R Mod$]] denote the [[category]] of [[modules]] over a [[commutative ring]] $R$.  Then the center of $R Mod$ is $R$.  
\end{proposition}
\begin{proof}
First note that for any $r \in R$, [[multiplication]] by $r$ acts as an [[endomorphism]] of each $R$-module (because $R$ is commutative), and this endomorphism is [[natural transformation|natural]]. This gives a [[ring homomorphism]] from $R$ to the center of $R Mod$ which is [[injective]] because distinct elements of $r$ act differently as multiplication on the $R$-module given by $R$ itself. To see that it is also [[surjective]] and [hence](balanced+category#SetIsBalanced) [[bijective]], suppose $\alpha$ is a [[natural transformation]] of the [[identity functor]] on $R \Mod$.  Then $\alpha_R \colon R \to R$ must be [[multiplication]] by some $r \in R$, since every endomorphism of the $R$-module $R$ is given by multiplication by some $r \in R$.  More generally, for any module $M$ and any $m \in M$ there is a module [[homomorphism]] $f \colon R \to M$ with $f(1) = m$, which by [[natural transformation|naturality]] implies
$$
  \alpha_M (m) 
   \,=\, 
  \alpha_M\big(f(1)\big)
   \,=\, 
  f\big(\alpha_R(1)\big) 
    \,=\, 
  f(r) 
    \,=\, 
  r m
  \,,
$$
which shows that $\alpha_M$ is multiplication by $r$. \end{proof}

## Related concepts

* [[center]]

* [[Drinfeld center]]

## References

An early occurence of the definition of the center of an additive category is in section 5.d of 

* [[Pierre Gabriel]], [[Des catégories abéliennes]], Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __90__ (1962), 323-448 ([numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0))

[[!redirects center of an abelian category]]
