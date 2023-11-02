


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _vectorial bundle_ ([Gomi 08](#Gomi08)) is a $\mathbb{Z}_2$-[[graded vector space|graded]] [[vector bundle]] $E$ of [[finite number|finite]] [[rank of a vector bundle|rank]], equipped with an odd [[endomorphism]] $h \;\colon\; E \to E$. The [[homomorphisms]] of vectorial bundles are such that the [[endomorphism]] $h$ acts like canceling parts of the even and odd degree of $E$ against each other.

This way vectorial bundles lend themselves to the description of [[topological K-theory]]. In particular, they allow a geometric model for [[twisted K-theory]].

## Definition 


For $X$ a [[topological space]], the [[category]] $VectrBund(X)$ of **vectorial bundles** on $X$ has

* as [[objects]] $(E \stackrel{h}{\to} E)$ [[finite number|finite]] [[rank of a vector bundle|rank]] Hermitean $\mathbb{Z}_2$-graded [[vector bundle | vector bundles]] $E\to X$ equipped with a self-adjoint [[endomorphism]] $h$ of odd degree. In [[matrix calculus]]

  $$
    E = \left( 
      \array{
        E_{0}
        \\
        E_{1}
      }
    \right)
  $$
  
  $$
     h = 
     \left(
       \array{
        0 & h_{10}
        \\
        h_{01} & 0
      }
     \right)
  $$

* as [[morphisms]] $\phi : (E,h) \to (E',h)$ [[equivalence classes]] of morphisms $\phi \colon E \to E'$ of vector bundles such that

  $$
    \array{
      E &\stackrel{\phi}{\longrightarrow}& E
      \\
      {}^{\mathllap{h}}\big\downarrow && \big\downarrow^{\mathrlap{h'}}
      \\
      E &\stackrel{\phi}{\longrightarrow}& E
    }
    \,,
  $$

  where two such maps are regarded as equivalent, $\phi \sim \phi'$,  already if they coincide on  the kernel of $h^2_x$ for each point $x$.

In particular, we have the following two important special cases:

* the case that $h = 0$ -- in this case all eigenvalues of all $h_x^2$ are zero. and hence maps $\phi, \phi' : (E,0) \to (E',0)$ represent the same morphism precisely if they are actually equal as morphisms $\phi, \phi' : E \to E'$ of vector bundles. 

  (Notice that there is only the 0-morphism $(E,0) \to (E',h')$ for $h' \neq 0$.)

  This yields a canonical inclusion

  $$
    VectBund(X) \hookrightarrow VectrBund(X)
  $$

  by sending $E \mapsto (E \stackrel{0}{\to} E)$.

* the case that $E = \left( \array{V \\ V}\right)$ 
  and $h = \left(
       \array{
         0 & Id \\ 
         Id & 0
       }
    \right)
  $
 
  Here $E_x|_{\lt \mu \lt 1} = 0$ and hence two morphisms
  $\phi, \phi' : (E,h) \to (E',h')$ are identified already if they agree on the 0-vector. In other words, _all_ morphisms out of such $(E,h)$ are identified. In particular they are all equal to the 0-morphism to $(0,0)$. Therefore the bundles of this form represent the 0-element.

**Definition**

Say two vectorial bundles $(E,h)$, $(E',h')$ on $X$ are **[[concordance|concordant]]** if there is a vectorial bundle on $X \times [0,1]$ which restricts to them at either end, respectively. 

Let 
$
  (E,h)^{\vee}
  =
$  be the degree-reversed bundle to $(E,h)$. 

**Lemma**

There is a concordance

$$
  E \oplus E^\vee \to 0 .
$$

## References 

The definition of vectorial bundles is due to Furuta. It is recalled and applied to the study of [[K-theory]] and [[twisted K-theory]] in

* {#Gomi08} [[Kiyonori Gomi]], _Twisted K-theory and finite-dimensional approximation_ ([arXiv:0803.2327](http://arxiv.org/abs/0803.2327))

[[!redirects vectorial bundles]]