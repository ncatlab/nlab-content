
#Contents#
* table of contents
{:toc}

## Idea 

Nakayama's lemma is a simple but fundamental result of commutative algebra frequently used to lift information from the [[fiber]] of a [[sheaf]] over a point (as for example a [[coherent sheaf]] over a [[scheme]]) to give information on the [[stalk]] at that point. 

## Statement and consequences 

Nakayama's lemma is frequently stated in a general but slightly unilluminating form. We begin with an easier and more intuitive form. In this article, all rings are assumed to be commutative. 

+-- {: .num_prop}
###### Proposition 
Let $R$ be a [[local ring]], with maximal [[ideal]] $\mathfrak{m}$ and residue [[field]] $k = R/\mathfrak{m}$. Let $M$ be a finitely generated $R$-[[module]]. Then $M \cong 0$ if and only if $k \otimes_R M \cong 0$. 
=-- 

Here is a sample application. Suppose $f \colon N \to M$ is an $R$-module map, giving rise to an exact sequence 

$$N \stackrel{f}{\to} M \stackrel{p}{\to} M/N \to 0.$$ 

Tensoring with $k$ is a right exact functor, so we have an exact sequence 

$$k \otimes_R N \stackrel{k \otimes_R f}{\to} k \otimes_R M \to k \otimes_R M/N \to 0.$$ 

Nakayama's lemma says that if $k \otimes_R M/N \cong 0$, then $M/N \cong 0$. Equivalently, that if $k \otimes_R f$ is epic, then $f$ is epic. In particular, to check whether a finite set of elements $v_1, \ldots, v_n$ generates $M$, it suffices to check whether the residue classes $v_i \mod \mathfrak{m}M$ generate the vector space $M/\mathfrak{m}M$, which is a linear algebra calculation. 

+-- {: .num_remark} 
###### Example 
Suppose $O$ is a [[Noetherian ring|Noetherian]] local ring. A typical example is the stalk at a point $p$ of a Noetherian scheme as locally ringed space, and we will write as if we were in that situation. Being Noetherian, its maximal ideal $\mathfrak{m}$ is finitely generated. Suppose $k \otimes_O \mathfrak{m} \cong \mathfrak{m}/\mathfrak{m}^2$ -- the cotangent space -- is a vector space of dimension $n$. We would like to know whether a collection of functions $f_1, \ldots, f_n$ that vanish at $p$ form a local coordinate system. 

For this, it suffices to check whether the differentials $d f_1, \ldots, d f_n$ at $p$, belonging to the cotangent space $\mathfrak{m}/\mathfrak{m}^2$, are linearly independent. (For then they span the cotangent space, and one concludes from Nakayama that the $f_i$ generate $\mathfrak{m}$ as an $O$-module, thereby forming a local coordinate system at $p$.) In this way, Nakayama's lemma operates as a kind of "inverse function theorem". 
=-- 

To cement this further, the following statement is offered in [Harris](#Harris) as a corollary of Nakayama's lemma (corollary 14.10, page 179): 

+-- {: .num_prop}
###### Proposition 
**(Inverse Function Theorem)** 
A map between complex projective varieties of dimension $n$ which is a bijection and has injective derivative at every point is an isomorphism. 
=-- 

We turn now to a general statement of Nakayama's lemma. 

(To be continued)

[[!redirects Nakayama lemma]]
