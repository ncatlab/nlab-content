
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Grothendieck spectral sequence_ is a [[spectral sequence]] that computes the [[cochain cohomology]] of the [[composition|composite]] of two [[derived functor in homological algebra|derived functors]] on [[categories of chain complexes]].



## Statement
 {#Statement}

Let $\mathcal{A},\mathcal{B},\mathcal{C}$ be [[abelian category|abelian categories]] and let $F \colon \mathcal{A}\to \mathcal{B}$ and $G \colon \mathcal{B}\to \mathcal{C}$  be [[exact functor|left exact]] [[additive functor|additive]] [[functors]]. Assume that $\mathcal{A}, \mathcal{B}$ have [[injective object|enough injectives]].


+-- {: .num_theorem}
###### Theorem ([[Tohoku]])


Write $R_F\subset \mathrm{Ob} A$ and $R_G\subset\mathrm{Ob} B$ for the [[class of adapted objects|classes of objects adapted to]] $F$ and $G$ respectively, and let furthermore $F(R_A)\subset R_B$. Then the derived functors $R F:D^+(A)\to D^+(B)$, $R G:D^+(B)\to D^+(C)$ and $R(G\circ  F):D^+(A)\to D^+(C)$ are defined and the natural morphism $R(G\circ F)\to R G\circ R F$ is an isomorphism. 

=--

+-- {: .num_theorem}
###### Theorem ([[Tohoku]])

In the above situation, assume that for every [[injective object]] $I \in \mathcal{A}$ the object $F(I) \in \mathcal{B}$ is a $G$-[[acyclic object]]. 

Then for every object $A \in \mathcal{A}$ there is a [[spectral sequence]] $\{E^r_{p,q}(A)\}_{r,p,q}$ called the **Grothendieck spectral sequence** whose $E_2$-page is the composite

$$
  E^{p,q}_2(A) = R^p G \circ R^q F (A)
$$ 

of the [[derived functor in homological algebra|right derived functors]] of $F$ and $G$ in degrees $q$ and $p$, respectively
and which is converging to to the derived functors $R^n(G\circ F)$ of the composite of $F$ and $G$:

$$
  E^{p,q}_\infty(A) \simeq R^{p+q}(G \circ F)(A)
  \,.
$$

Moreover, this is [[natural isomorphism|natural]] in $A \in \mathcal{A}$.

=--

+-- {: .proof}
###### Proof

By assumption of enough injectives, we may find an _[[injective resolution]]_

$$  
  A \stackrel{\simeq_{qi}}{\to} C^\bullet 
$$

of $A$. Next, by the discussion at _[injective resolution -- Existence and construction](projective+resolution#ExistenceAndConstructionOfResolutionsOfComplexes)_ we may find a _fully injective_ resolution of the chain complex $F(C^\bullet)$:

$$
  0 \to F(C^\bullet) \to I^{\bullet, \bullet}
  \,,
$$

where hence $I^{\bullet, \bullet}$ is a [[double complex]] of [[injective objects]] such that for each $n \in \mathbb{N}$ the component $0 \to F(C^n) \to I^{n,\bullet}$ is an ordinary injective resolution of $F(C^n) \in \mathcal{B}$. 

Thus we have the corresponding double complex $G(I^{\bullet,\bullet})$ in $\mathcal{C}$. The claim is that the Grothendieck spectral sequence is the [[spectral sequence of a double complex]] for $G(I^{\bullet, \bullet})$ equipped with the vertical-degree [[filtered chain complex|filtration]] $\{{}^{vert}E^r_{p,q}(A)\}$:

$$
  {}^{vert} E^2_{p,q}(A) \simeq R^p G (R^q F(A))
  \,.
$$

To see this, notice that by the assumption that $I^{\bullet,\bullet}$ is a _fully_ injective projective resolution, the short exact sequences

$$
  0 \to B^{q,p}(I) \to Z^{q,p}(I) \to H^{q,p}(I) \to 0
$$

are [[split exact sequence|split]] (by the discussion there) and hence so is their image under any functor and hence in particular under $G$. Accordingly we have

$$
  \begin{aligned}
    {}^{vert}E^{p,q}_1 
    & \simeq
    H^q(G(I^{\bullet,p}))
    \\
    & \simeq (G(Z^{q,p})) / (G(B^{q,p}))
    \\
    & \simeq G H^{q,p}
  \end{aligned}
$$

(the first two equivalences by general properties of the filtration spectral sequence, the last by the above splitness). Hence it follows that

$$
  \begin{aligned}
    {}^{vert}E^{p,q}_2 
    & \simeq 
    H^p(G(H^{q,\bullet}))
    \\
    & \simeq
    R^p G (R^q F (A))   
  \end{aligned}
  \,,
$$

where in the last step we used that $H^{q,\bullet}$ is be construction an injective resolution of $H^q(F(C^\bullet)) \simeq R^q F(A)$ (using the $G$-acyclicity of $F(C^\bullet)$).

This establishes the spectral sequence and its second page as claimed. It remains to determine its convergence.

To that end, consider dually, the spectral sequence $\{{}^{hor}E^{p,q}_r\}$ coming from the horizontal filtration on the double complex $G(I^{\bullet, \bullet})$. By the general properties of [[spectral sequence of a double complex]] this converges to the same value as the previous one. But for this latter spectral sequence we find

$$
  \begin{aligned}
    {}^{hor}E^{p,q}_1 & \simeq H^q(G I^{p,\bullet})
    \\
    & \simeq R^q G(F(C^p))
  \end{aligned}
  \,,
$$

the first equivalence by the general properties of filtration spectral sequences, the second then by the definition of [[derived functor in homological algebra|right derived functors]]. But by assumption $F(C^p)$ is $G$-[[acyclic object|acyclic]] and hence all these derived functors vanish in positive degree, so that

$$
  {}^{hor}E^{p,q}_1 \simeq
  \left\{
    \array{
       G(F(C^p)) & if\; q = 0
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

Next, the $E_2$-page then contains just horizontal homology of $G(F(C^\bullet))$ and this is by definition now the derived functor of the composite of $F$ with $G$:

$$
  {}^{hor}E^{p,q}_2 \simeq
  \left\{
    \array{
      R^p(G \circ F) & if \; q  = 0
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

Since this is concentrated in the $(q = 0)$-row the spectral sequence of the horizontal filtration collapses here and hence

$$
  \begin{aligned}
    H^n(Tot(G(I^{\bullet,\bullet})))
    &\simeq
    G^n H^{n+0}(Tot(G(I^{\bullet,\bullet})))
    \\
    & \simeq
    E^{n,0}_\infty
 \end{aligned}
$$


So in conclusion we have

$$
  \begin{aligned}
    R^p G(R^q F(A))
    & \simeq
    {}^{vert}E^{p,q}_2
    \\
    & \Rightarrow
    {}^{vert} E^{p,q}_\infty
    \\
    & \simeq
    G^p_{vert} H^{p+q}(Tot(G(I^{\bullet, \bullet})))
    \\
    & \simeq 
    H^{p+q}(Tot(G(I^{\bullet, \bullet})))    
    \\
    & \simeq 
    G^{p+q}_{hor} H^{p+q}(Tot(G(I^{\bullet, \bullet})))    
    \\
    & \simeq
    {}^{hor} E^{p+q,0}_\infty(A)
    \\
    & \simeq
    R^{p+q}(G \circ F)(A)
  \end{aligned}
$$


=--

## Examples

Many other classes of spectral sequences are special cases of the Grothendieck spectral sequence, for instance the

* [[Hochschild-Serre spectral sequence]]

* [[Leray spectral sequence]]

* [[base change spectral sequence]] 


## References

Leture notes include

* [[James Milne]], section 10 of _[[Lectures on Étale Cohomology]]_

* Jinhyun Park, _Personal notes on Grothendieck spectral sequence_ ([pdf](http://mathsci.kaist.ac.kr/~jinhyun/note/g_s_sequence/sequence.pdf))

