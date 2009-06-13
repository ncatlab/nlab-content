# Definition #

Let $X$ be an $n$-dimensional manifold. 
Its tangent [[bundle]] is canonically associated to a $O(n)$-principal bundle, which is in turn classified by a map

$$
  X \to B O(n)
$$

from $X$ to the [[classifying space]] of the group $O(n)$.

* A **String structure** on $X$ is the choice of a lift of this map a few steps through the [[Whitehead tower]] of $O(n)$.

* The manifold "is string" if such a lift exists.

This means the following:

* there is a canonical map $w_1 : B O(n) \to B\mathbb{Z}_2$ from the [[classifying space]] of $O(n)$ to that of $\mathbb{Z}_2 = \mathbb{Z}/2\mathbb{Z}$ that represents the general of the cohomology $H^1(B O(n), \mathbb{Z}_2)$. The classifying space of the group $SO(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B SO(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B O(n) &\stackrel{w_1}{\to}& \mathbb{B}\mathbb{Z}_2
   }
  $$
  Namely using the [[homotopy hypothesis]] (which is a theorem, recall), we may identify $B O(n)$ with the one object [[groupoid]] whose space of morhisms is $O(n)$ and similarly for $ B \mathbb{Z}_2$. Then the map in question is the one induced from the group homomorphism that sends orientation preserving elements in $O(n)$ to the identity and orientation reversing elements to the nontrivial element in $\mathbb{Z}_2$.

  * an **orientation** on $X$ is a choice of lift of the structure group through $B SO(n) \to B O(n)$
  $$
   \array{
    && B SO(n)
    \\
    & {}^{orientation}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B O(n)
   }
   \,.
  $$

* there is a canonical map $w_2 : B SO(n) \to B^2 \mathbb{Z}_2$ representing the generator of $H^2(B SO(n), \mathbb{Z}_2)$. The classifying space of the group $Spin(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Spin(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B SO(n) &\stackrel{w_2}{\to}& \mathbb{B}^2\mathbb{Z}_2
   }
  $$

  * a **spin structure** on an oriented manifold $X$ is a choice of lift of the structure group through $B Spin(n) \to B SO(n)$
  $$
   \array{
    && B Spin(n)
    \\
    & {}^{spin structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B SO(n)
   }
   \,.
  $$

* there is a canonical map $B Spin(n) \to B^3 U(1)$ The classifying space of the group $String(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Spin(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B SO(n) &\stackrel{\frac{1}{2}p_1}{\to}& \mathbb{B}^3 U(1)
   }
  $$

  * a **string structure** on an oriented manifold $X$ is a choice of lift of the structure group through $B String(n) \to B Spin(n)$
  $$
   \array{
    && B String(n)
    \\
    & {}^{string structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B Spin(n)
   }
   \,.
  $$

* there is a canonical map $B String(n) \to B^7 U(1)$ The classifying space of the group $Fivebrane(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Fivebrane(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B String(n) &\stackrel{\frac{1}{6}p_2}{\to}& \mathbb{B}^7 U(1)
   }
  $$

  * a **fivebrane structure** on an string manifold $X$ is a choice of lift of the structure group through $B Fivebrane(n) \to B String(n)$
  $$
   \array{
    && B Fivebrane(n)
    \\
    & {}^{fivebrane structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B String(n)
   }
   \,.
  $$

