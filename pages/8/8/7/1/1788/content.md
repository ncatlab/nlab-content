For $G \,\equiv\, A$ an *[[abelian group|abelian]] [[topological group|group]]*, one readily sees that there is a [[fiber]]-wise $A$-[[tensor product]] of principal $A$-bundles

\begin{tikzcd}[sep=0pt]
    \mathrm{Prnc}A\mathrm{Bndl}(X)_{/\sim}
    \,\times\,
    \mathrm{Prnc}A\mathrm{Bndl}(X)_{/\sim}
    \ar[
      rr
    ]
    &&
    \mathrm{Prnc}A\mathrm{Bndl}(X)_{/\sim}    
    \\
    \big(
      \,
      [P],
      \,
      [P']
      \,
    \big)
    &\longmapsto&
    \big[
      P \times_A P'
    \big]
\end{tikzcd}

given by

> (NB: This tensor product of fibrations exists also for non-abelian $G$, but the commutativity of $A$ is needed for principality, namely for the resulting transition functions to again by given by group multiplication.)

$$
  (P \times_A P')_x
  \;\coloneqq\;
  \Big\{
    (p, p')
    \,\in \,
    P_x \times P'{}_{\!\!\!x}
  \Big\}\Big/\Big(
    (a \cdot p,\, p')
    \sim
    (p,\, a^{-1} \cdot p')
  \Big)
  \,,
$$
which makes the isomorphism classes naturally form an abelian group. 

Under the classification of principal $A$-bundles by $A$-cohomology, this means that
the classifying space $B A$ (may be chosen such that it) carries topological group structure itself!, so that the construction iterates:

$$
  A \;\in\; 
  \mathrm{AbGrp}(\mathrm{TopSpc})
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  \left\{
  \begin{array}{l}
  B^2 A
  \;\coloneqq\;
  B(B A)
  \\
  B^3 A
  \;:=\;
  B\big(B(B A)\big)
  \\
  \;\;\;\vdots
  \\
  B^{1+n} \;:=\; B\big(B^n A\big)
  \mathrlap{\,.}
  \end{array}
  \right.
$$

For a *[[discrete group|discrete]]* abelian group $A$ (such as [[integers|$A = \mathbb{Z}$]]) these higher-order classifying spaces are also denoted "$K(A,n)$" and called "[[Eilenberg-MacLane spaces]]":

$$
  A \,\in\,
  \mathrm{AbGrp}(\mathrm{Set})
  \;\;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;\;
  K(A,n)
  \;\;
  :=
  \;\;
  B^n A
  \,.
$$

But this means that for abelian group coefficients $A$ there is *higher-degree $A$-cohomology* appearing as a special case of non-abelian cohomology, as follows:

$$
  H^{1+n}\big(
    X
    ;\,
    A
  \big)
  \;\;
  :=
  \;\;
  H^1\big(
    X
    ;\,
    B^nA
  \big)
  \;\;
  :=
  \;\;
  \pi_0
  \, \mathrm{Maps}\big(
    X
    ,\,
    B^{1+n} A
  \big)
  \,.
$$

Of course, when $A$ is discrete then there is also *[[Čech cohomology]]* and *[[singular cohomology]]* with coefficients in $A$. A classical theorem says that (on our smooth manifold domain $X$) all these notions of [[ordinary cohomology]] agree, hence that

$$
   \text{Ordinary}\;A\text{-cohomology has classifying spaces}\; B^n A \,=\, K(A,n).
$$
