
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

For a [[pointed topological space]] $(X, x)$, its *reduced suspension* $\Sigma (X,x) $ is obtained from the plain [[suspension]] 

$$
  \mathrm{S}X
  \;\coloneqq\;
  \frac{
    X \,\times\, [-1,\, +1]
  }{
    \left(
    \begin{array}{c}  
      X \times \{-1\}\mathrlap{,\,}
      \\
      X \times \{+1\}
    \end{array}
    \right)
  }
$$ 

of the [[underlying]] [[topological space]] $X$ by [[quotient space|collapsing]] the [[meridian]] through the [[basepoint]] $x$ itself to a point --- this making $\Sigma(X,x)$ itself a [[pointed topological space]] with basepoint the [[equivalence class]] of that meridian $mer(x)$:

$$
  \Sigma (X,x) 
    \;\coloneqq\; 
  \frac{
    \mathrm{S}X
  }{ \{x\} \times [-1,1] }
  \;\;\;
  \in
  \;\;
  Top^{\ast/}
  \,.
$$

(Notice that this identifies in particular also the two [[antipode|antipodal]] "poles" of the plain suspension.)

If $X$ admits the structure of a [[CW-complex]] then, under passage to the [[classical homotopy category]] of [[pointed topological spaces]] (cf.  [here](classical+model+structure+on+topological+spaces#ModelstructureOnPointedTopologicalSpaces)) this construction models the [[homotopy pushout]] of the [[terminal object|terminal]] map $(X,x) \to (\ast,pt)$ along itself, which explains its prevalence in [[homotopy theory]] (especially in [[stable homotopy theory]], see also at *[[suspension spectrum]]*).

Moreover, in this case of [[CW-complexes]] the [[underlying]] space of $\Sigma (X,x)$ (i.e. forgetting its [[basepoint]]) is [[weak homotopy equivalence|weakly homotopy equivalent]] to the plain [[suspension]] $\mathrm{S} X$ of the [[underlying]] space $X$ of $(X,x)$. In this sense, reduced suspension in the context of [[homotopy theory]] may be understood as just being plain suspension but with basepoints taken into account.


## Definition
 {#Definition}

For $(X,x)$ a [[pointed topological space]], then its *reduced suspension* $\Sigma X$ is equivalently the following:

* obtained from the standard [[cylinder]] $I\times X$ ([[product topological space]] with the [[closed interval]] $I = [0,1]$) by identifying the [[subspace]] $(\{0,1\}\times X) \cup (I\times \{x\})$ to a point, i.e. the [[quotient space]] ([this example](quotient+space#QuotientBySubspace))

  $$
     (X \times [0,1])/ ( ( X \times \{0,1\} ) \cup ([0,1] \times \{x\}) )
  $$  

  (Think of crushing the two ends of the cylinder and the line through the base point to a point.) 

* obtained from the plain [[suspension]] 

  $$
    S X = (X \times [0,1])/( X \times \{0\}, X \times \{1\})
  $$ 

  of $X$ by passing to the [[quotient space]] which collapses $\{x\} \times I$ to a point ([this example](quotient+space#QuotientBySubspace))

  $$
    \Sigma X \simeq S X / (  \{x\} \times I )
  $$

  For the purposes of [[generalized (Eilenberg-Steenrod) cohomology]] theory typically it does not matter whether one evaluates on the standard suspension or the reduced suspension. For example for [[topological K-theory]] since $\{x\} \times I$ is a [[contractible topological space|contractible]] [[closed subspace]], then [this prop.](topological+vector+bundle#VectorBundlesOverQuotientByContractibleSubspaceAreEquivalentToVectorBundlesOnTotalSpace) says that [[topological vector bundles]] do not see a difference as long as $X$ is a [[compact Hausdorff space]].



* obtained from the [[reduced cylinder]] by collapsing the two ends, i.e. the [[cofiber]]

  $$
    \Sigma X \simeq cofib(X \vee X \to X \wedge (I_+))
  $$

* the [[mapping cone]] in [[pointed topological spaces]] formed with respect to the [[reduced cylinder]] $X \wedge (I_+)$ of the map $X \to \ast$;

* the [[smash product]] $S^1\wedge X$, of $X$ with the [[circle]] (based at some point) with $X$.

  $$
    \Sigma X \simeq S^1 \wedge X
    \,.
  $$


## Properties

### Relation to suspension

For [[CW-complexes]] $X$ that are also [[pointed topological space|pointed]], with the point identified with a 0-cell, then their reduced suspension is [[weak homotopy equivalence|weakly homotopy equivalent]] to the ordinary suspension: $\Sigma X \simeq S X$.

### Cogroup structure

[[suspensions are H-cogroup objects]]

## Examples

\begin{example} **(spheres)** \linebreak
Up to [[homeomorphism]], the reduced suspension of the $n$-[[sphere]] is the $(n+1)$-sphere
$$
  \Sigma S^n \simeq S^{n+1}
  \,.
$$
For more see at _[one-point compactification -- Examples -- Spheres](one-point+compactification#ExamplesSpheres)_.
\end{example}

\begin{example} **(stable splitting of product spaces)** 
\label{StableSplittingOfProductSpaces}
\linebreak
  For $X$ and $Y$ a [[pair]] of [[pointed topological space|pointed]] [[CW-complexes]], the reduced suspension of their [[product space]] is [[homotopy equivalence|homotopy equivalent]] to the [[wedge sum]] of their individual reduced suspensions with that of their [[smash product]] $X \wedge Y$:
$$
  \Sigma(X \times Y)
  \,\underset{hmtp}{\simeq}\,
  \Sigma X 
    \,\vee\, 
  \Sigma Y
    \,\vee\,
  \Sigma(X \wedge Y)
  \mathrlap{\,.}
$$
\end{example}
(cf. [Hatcher 2002 Prop. 4I.1](#Hatcher02))

## Related concepts

* [[loop space object]], [[free loop space object]],

  * [[delooping]]

  * [[loop space]], [[free loop space]], [[derived loop space]]

* [[pointed (∞,1)-category]], [[pointed model category]]

* [[suspension object]]

  * [[suspension type]], [[reduced suspension type]]

  * [[suspension]], **reduced suspension**

    * [[Freudenthal suspension theorem]]

    * [[Spanier-Whitehead category]]

    * [[suspension isomorphism]]

    * [[suspension of a chain complex]]

    * [[Sullivan model of a suspension]]

## References
 {#References}

Discussion of (reduced) [[suspension]] may be found in most introductions to [[homotopy theory]] (for discussion of unreduced suspension see also [there](suspension#References)).

For instance:

* {#Hatcher02} [[Allen Hatcher]], Ex. 0.10 in: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* [[Marcelo Aguilar]], [[Samuel Gitler]], [[Carlos Prieto]], §2.10 in: *Algebraic topology from a homotopical viewpoint*, Springer (2008) &lbrack;[doi:10.1007/b97586](https://link.springer.com/book/10.1007/b97586)&rbrack;

* [[Jeffrey Strom]], §3.8 and §17 in: *Modern classical homotopy theory*, Graduate Studies in Mathematics **127**, American Mathematical Society (2011) &lbrack;[doi:10.1090/gsm/127](http://www.ams.org/books/gsm/127/)&rbrack;

* [[Martin Arkowitz]], *Loop spaces and suspensions*, §2.3 in: *Introduction to Homotopy Theory*, Springer (2011) &lbrack;[doi:10.1007/978-1-4419-7329-0](https://doi.org/10.1007/978-1-4419-7329-0)&rbrack;

Review in the context of [[stable homotopy theory]]:

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 2 of: _Spectra and stable homotopy theory_ (2012) &lbrack;[pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]]&rbrack;


[[!redirects reduced suspensions]]

[[!redirects reduced suspension object]]
[[!redirects reduced suspension objects]]



