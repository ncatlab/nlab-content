#Idea#

As described at [[cohomology]], a notion of [[cohomology]] exists for every [[(infinity,1)-topos]] $\mathbf{H}$: for $X$ and $A$ two objects of $\mathbf{H}$, 

* an $A$-valued cocycle on $X$ is an object in the [[infinity-groupoid]] $\mathbf{H}(X,A)$;

* a coboundary between two such cocycles is a morphism in $\mathbf{H}(X,A)$

* the cohomology classes are the equivalence classes of $\mathbf{H}(X,A)$, so that the cohomology set of $A$-valued cohomology on $X$ is
  $$
    H(X,A) = := \pi_0 \mathbf{H}(X,A) = Ho_{\mathbf{H}}(X,A)
    \,,
  $$
  where $\mathbf{H}$ is the [[homotopy category of an (infinity,1)-category|homotopy category]] of the [[(infinity,1)-category]] $\mathbf{H}$.

Now ordinary **groupoid [[nonabelian cohomology]]** is the cohomology obtained for $\mathbf{H} = $ [[Infinity-Grpd]] $\simeq$ [[Top]]: cohomology on [[infinity-groupoid]]s (or [[topological space]]s) with coefficients in $\infty$-groupoids.

The various notions of **group cohomology** are special cases of this:

* **Group cohomology with coefficients in a trivial module** is the cohomology in $\mathbf{H} = $ [[Infinity-Grpd]] for the case that

  * the domain $X = \mathbf{B} G$ is a one-object [[groupoid]] coming from a [[group]] $G$;

  * the coefficient object is $A = \mathbf{B}^n K$, the [[strict infinity-groupoid]] coming from the [[crossed complex]] that is concentrated in degree $n$, where it is the abelian group $K$ (see [[Eilenberg-MacLane space|Eilenberg-MacLane object]] for more details).

  For $n \in \mathbB{N}$ One writes
  $$
    H_{Grp}^n(G,K) := H(\mathbf{B}G, \mathbf{B}^n K)
    = Ho_{\infty Grpd}(\mathbf{B}G , \mathbf{B}^n K)
  $$
  for the **degree $n$-group cohomology of $G$ with values in $K$.

* **Nonabelian group cohomology** is obtained from this by allowing the coefficient object to be of the form 

  * $A =\mathbf{B} K_{(n)}$, for $K_{(n)}$ an arbitrary [[n-group]] 

  For instance for $K = AUT(H)$ the [[2-group|automorphism 2-group]] of a possibly nonabelian group $H$, nonabelian group cohomology classified $H$-extensions of $G$ (see also [[gerbe (general idea)]]).

* **Group cohomology with coefficients in a nontrivial module** is in turn the following special case and variation of nonabelian group cohomology:

  * let $A := \mathbf{B}^n_\rho K$ be a [[strict infinity-groupoid]] coming from a [[crossed complex]] of the form 
    $$
      [\mathbf{B}^n_\rho K] := (  \cdots \to {*} \to {*} \to K \to \cdots \to {*} \to {}* \to G \stackrel{\to}{\to}{*})
    $$
    with the abelian group $K$ in degree $n$ and for 
    $$
      \rho : G \to Aut(K)
    $$ 
    the action of $G$ on $K$ required by the structure of a [[crossed complex]]

  then the consider the $\infty$-groupoid $\mathbf{H}^{\rho}(\mathbf{B}G, \mathbf{B}^n_G )$ induced by the [[fibration sequence|homotopy fiber]] of the canonical projection morphism $\mathbf{B}^n_\rho K \to \mathbf{B} G$
  $$
    \array{
      \mathbf{H}^\rho(\mathbf{B}G, \matbf{B}^n K) &\to& {*}
      \\
      \downarrow && \downarrow^{const_{Id_{\mathbf{B}G}}}
      \\
      \mathbf{H}(\mathbf{B}G, \mathbf{B}^n K)
      &\to&
      \mathbf{H}(\mathbf{B}G, \mathbf{B}G)
    }
    \,.
  $$

  The $n$th group cohomology of $G$ with coefficients in the module $(K, \rho)$ is the cohomology classes of that $\infty$-groupoid:

  $$
    H_{Grp}^n(G,(K,\rho)) =
    \pi_o \mathbf{H}^\rho(\mathbf{B}G, \matbf{B}^n K)
    \,.
  $$

  This is an example of general [[twisted cohomology]].

# References #

Aspects of this general point of view on group cohomology is described for instance in chaper 12 of

* R. Brown, P. Higgins, R. Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/%7Emas010/pdffiles/rbrsbookb-e040609.pdf), [web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html))

Much of what is called "nonabelian cohomology" in the existing literature concerns the case of nonabelian group cohomology with coefficients in the [[2-group|automorphism 2group]] $AUT(H)$ of some possibly nonabelian group $H$.

This is the topic of [[Schreier theory]].

A random example for this use of terminology would be

* Roggenkamp, Scott, _Automorphisms and nonabelian cohomology_ ([pdf](http://www.math.virginia.edu/~lls2l/automorphisms_and_nonabelian.pdf))

For a conceptual discussion of nonabelian group cohomology see

* [[John Baez]], [[Mike Shulman]], _Lectures on $n$-Categories and Cohomology_ ([arXiv](http://arxiv.org/abs/math/0608420))



