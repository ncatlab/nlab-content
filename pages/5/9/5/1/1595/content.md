+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_lemma #SigmaOmegaAdjunctionUnitOnNConnectedSpaceIsHigherConnected}
###### Lemma

Let $X$ be an [[n-connected topological space]]. Then the [[adjunction unit]] of the ([[suspension]] $\dashv$ [[loop space]])-[[adjunction]]

$$
  X \longrightarrow \Omega \Sigma X
$$

is [[n-connected continuous function|(2n+1)-connected]].

=--

(e.g. [Kochmann 96, prop. 3.2.2](#Kochmann96))

+-- {: .proof}
###### Proof

The [[Serre long exact sequence]] ([prop.](Serre+long+exact+sequence#SerreLongExactSequenceForHighlyConnectedBaseAndFiber)) applied to the based [[path space]] [[Serre fibration]] of any [[n-connected topological space]]

$$
  \Omega X \longrightarrow Path_\ast(X) \longrightarrow X
$$

is of the form

$$
  H_{2n}(\Omega X)
    \overset{i_\ast}{\longrightarrow}
  H_{2n}(Path_\ast(X))
    \overset{p_\ast}{\longrightarrow}
  H_{2n}(X)
    \overset{\tau}{\longrightarrow}
  H_{2n-1}(\Omega X)
    \overset{i_\ast}{\longrightarrow}
  \cdots
    \overset{i_\ast}{\longrightarrow}
  H_1(X)        
$$

and hence yields (using that $Path_\ast(X)$ is [[contractible topological space|contractible]]) isomorphisms

$$
  \tau \colon H_k(X) \simeq H_{k-1}(\Omega X)
$$

for $k \leq 2n$. Applied to $\Sigma X$, which is $(n+1)$-connected this hence yields isomorphisms

$$
 \tau \colon H_{k}(\Sigma X) \simeq H_{k-1}(\Omega \Sigma X)
$$

for $k \leq 2n+2$.

To get a comparison map, observe that there is a [[commuting diagram]] of the form

$$
  \array{
     X 
       &\longrightarrow&  
     Cone(X)
       &\overset{q}{\longrightarrow}& 
     \Sigma X
     \\
     {}^{\mathllap{j}}\downarrow && \downarrow && \downarrow
     \\
     \Omega \Sigma X
       &\longrightarrow&
     Path_\ast(\Sigma X)
       &\underset{p}{\longrightarrow}&
     \Sigma X
  }
$$

which induces a diagram of [[relative homology]] groups of the form

$$
  \array{
    \tilde H_k(X) 
      &\underoverset{\simeq}{\partial}{\longleftarrow}& 
    H_{k+1}(Cone(X),X)
      &\underoverset{\simeq}{}{\longrightarrow}&
    \tilde H_{k+1}(\Sigma X)
    \\
    {}^{\mathllap{j_\ast}}\downarrow && \downarrow && \downarrow^{\mathrlap{id}}
    \\
    \tilde H_k(\Omega \Sigma X)
      &\underoverset{\simeq}{\partial}{\longleftarrow}&
    H_{k+1}(Path_\ast(\Sigma X),\Omega \Sigma X)
      &\underoverset{}{p_\ast}{\longrightarrow}&
    \tilde H_{k+1}(\Sigma X)
  }
$$

=--

The **Freudenthal suspension theorem** ([Freudenthal 37](#Freudenthal37)) is the following theorem about [[homotopy groups]] of [[n-spheres]]:


+-- {: .num_prop}
###### Proposition

The [[suspension]] [[homomorphism]] on [[homotopy groups of spheres]] 

$$
  \pi_{n+k}(S^n) \longrightarrow \pi_{n+k+1}(S^{n+1})
$$ 

is an [[isomorphism]] for $n\gt k+1$. 

More generally, for $X$ an [[n-connected]] [[CW-complex]], then the suspension homomorphism on [[homotopy groups]]

$$
  \pi_k(X) \longrightarrow \pi_{k+1}(\Sigma X)
$$

is an [[isomorphism]] for $k \leq 2n$.

=--

The suspension isomorphism is equivalently given by the map in lemma \ref{SigmaOmegaAdjunctionUnitOnNConnectedSpaceIsHigherConnected}.

An alternative proof proceeds from the [[Blakers-Massey theorem]] (e.g. [Kochmann 96, p. 70](#Kochmann96)). 

The following more general statement is also often referred to as the Freudenthal suspension theorem:

+-- {: .num_prop}
###### Proposition

For $X$ an [[n-connected]] [[CW-complex]] and $Y$ a [[CW-complex]] of [[dimension]] $\leq 2n$, then the maps of [[homotopy classes]] of [[continuous functions]]

$$
  [Y,X]\stackrel{}{\longrightarrow} [\Sigma Y, \Sigma X] \stackrel{}{\longrightarrow}[\Sigma^2 Y, \Sigma^2 X]
$$

are [[isomorphisms]]. In particular $[Y,X]$ canonically has the structure of an [[abelian group]].

=--



## Properties

### As motivation for stable homotopy theory

The Freudenthal suspension theorem motivated introducing the [[stable homotopy groups of spheres]] $\pi_k(S):=\pi_{n+k}(S^n)$, more generally the [[stable homotopy groups]] $\pi_k^S(Y) = \pi_{n+k}(\Sigma^n Y)$, both independent of $n$ where $n\gt k+1$, and still more generally the [[Spanier-Whitehead category]], then the [[stable homotopy category]] and eventually the [[stable (infinity,1)-category of spectra]].


## Related concepts

* [[suspension isomorphism]]

## References

Due to 

* {#Freudenthal37} [[Hans Freudenthal]],  _&#220;ber die Klassen der Sph&#228;renabbildungen_, Compositio Math., 5:299-314, 1937.

Textbook accounts include

* {#Switzer75} [[Robert Switzer]], theorem 6.26 in _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#Kochmann96} [[Stanley Kochmann]], section 3.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Alan Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, chapter 4 ([pdf](http://www.math.cornell.edu/~hatcher/AT/ATch4.pdf))

A nice expanded version of the latter is in

* Tengren Zhang, _Freudenthal suspension theorem_  ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/ZhangTengren.pdf))


A formalization in [[homotopy type theory]] in [[Agda]] is in 

* [[Peter Lumsdaine]], [[Dan Licata]], _[Freudenthal.agda](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Freudenthal.agda)_

Discussion in [[equivariant homotopy theory]] includes

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], p. 7,8 of _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))




