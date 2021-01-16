
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[spin group]] in [[dimension]] 6.

## Properties

### Exceptional isomorphism
 {#ExceptionalIsomorphism}

+-- {: .num_prop #IsomorphismBetweenSpin6AndSU4}
###### Proposition

There is an [[exceptional isomorphism]] 

\begin{tikzpicture}

  \node (Spin6) at (0,1.4)  {$\mathrm{Spin}(6)$};
  \node (SU4) at (3.4,1.4)  {$\mathrm{SU}(4)$};

  \node at (1.7,1.4) {$\simeq$};

  \node (center) at (0,0) {};
  \node (topright) at (30:1) {};
  \node (left) at (180-30:1) {};
  \node (botright) at (0,-1) {};
  
  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[draw=lightgray, fill=lightgray] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);


  \draw (center) to (topright);
  \draw[lightgray] (center) to (botright);
  \draw (center) to (left);
    
  \begin{scope}[shift={(3.4,0)}]
  \node (center) at (0,0) {};
  \node (left) at (-1,0) {};
  \node (right) at (+1,0) {};

  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (left) circle (.1);
  \draw[fill=black] (right) circle (.1);

  \draw (center) to (left);
  \draw (center) to (right);
  \end{scope}
\end{tikzpicture}

between [[Spin(6)]] and [[SU(4)]], reflecting, under the [[classification of simple Lie groups]], the coincidence of [[Dynkin diagram]] of "[[D3]]" with [[A3]].


=--

(e.g. [Figueroa-O'Farrill 10, Lemma 8.1](#FigueroaFarrill10))

One way to see the isomorphism $\mathrm{Spin}(6) \cong \mathrm{SU}(4)$ is as follows.  Let $V$ be a 4-dimensional complex vector space with an inner product and a compatible complex volume form, meaning an element of $\Lambda^4 V$ whose norm is 1 in the norm coming from the inner product on $V$.   The inner product defines a conjugate-linear isomorphism $V \cong V^\ast$ that together with the complex volume form can be used to define a conjugate-linear Hodge star operator on $\Lambda^2 V$.  This Hodge star operator squares to the identity, and its $+1$ and $-1$ eigenspaces, say $\Lambda_{\pm}^2 V$, each become 6-dimensional *real* inner product spaces in a natural way.  Thus, the group $\mathrm{SU}(V)$, consisting of all linear transformations of $V$ that preserve the inner product and complex volume form, acts functorially as linear transformation of the real vector space $\Lambda_+^2 V$ that preserve the inner product, giving a homomorphism $\rho: \mathrm{SU}(V) \to \mathrm{O}(\Lambda_+^2 V)$.  Since $\mathrm{SU}(V)$ is connected we in fact have $\rho: \mathrm{SU}(V) \to \mathrm{SO}(\Lambda_+^2 V)$.  

Specializing to the case $V = \mathbb{C}^4$ we get a Lie group homomorphism $\rho: \mathrm{SU}(4) \to \mathrm{SO}(6)$.  Since $d\rho$ is nonzero and $\mathrm{SU}(4)$ is simple, $d\rho$ must be injective.   Since 

$$ \mathrm{dim}(\mathrm{SU}(4)) = 15 = \mathrm{dim}(\mathrm{SO}(6)), $$

$d\rho$ must also be surjective.   Since $\mathrm{SO}(6)$ is connected and $d\rho$ is a bijection, $\rho$ must be a covering map.  Since $\rho(\pm 1) = 1$, $\rho$ exhibits $\mathrm{SU}(4)$ as a connected cover of $\mathrm{SO}(6)$ that is *at least* a double cover.  But the universal cover of $\mathrm{SO}(6)$, namely $\mathrm{Spin}(6)$, is only a double cover.  Thus $\mathrm{SU}(4)$ is a double cover of $\mathrm{SO}(6)$, and $\mathrm{SU}(4) \cong \mathrm{Spin}(6)$.   



### Coset spaces

[[!include coset space structure on n-spheres -- table]]


### $G$-Structure and exceptional geometry


[[!include Spin(8)-subgroups and reductions -- table]]


\linebreak

## Related concepts

[[!include low dimensional rotation groups -- table]]

* [[U(1)]], [[SU(2)]], [[SU(3)]], [[SU(5)]]

\linebreak

## References

* {#FigueroaFarrill10} [[José Figueroa-O'Farrill]], _[PG course on Spin Geometry](https://empg.maths.ed.ac.uk/Activities/Spin/)_ lecture 8: _Parallel and Killing spinors_, 2010 ([pdf](https://empg.maths.ed.ac.uk/Activities/Spin/Lecture8.pdf))

[[!redirects SU(4)]]
