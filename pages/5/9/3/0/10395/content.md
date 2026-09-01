
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


\tableofcontents


## Idea

For $G$ a [[topological group]] (or [[Lie group]]) and $P \to X$ a $G$-[[principal bundle]], we have that forming [[mapping spaces]] out of the [[circle]] yields a free [[loop group]]-[[principal bundle]] over the [[free loop space]] of $X$:

$$
  \array{
    \mathcal{L}G &\to& \mathcal{L} P
    \\
    && \downarrow
    \\
    && \mathcal{L} X
  }
  \,.
$$

In the special case that $X = Y \times S^1$ is a [[Cartesian product]] with the [[circle]], then one can consider the [[subspace]] of the [[free loop space]] of $X$ on those loops whose [[projection]] on the $S^1$-factor is the [[identity]]. This subspace is of course [[equivalence|equivalent]] to $Y$, giving a canonical inclusion

$$
  i \;\colon\; Y \hookrightarrow \mathcal{L} (Y \times S^1)
  \,.
$$

(Abstractly, this is the [[adjunct]] of the [[identity]] under the [[internal hom]]-[[adjunction]].)

Along this inclusion one can [[pullback|pull back]] the $\mathcal{L}G$-principal bundle over $\mathcal{L}X$. The **caloron correspondence** is the statement that if 

$$
  \Omega_{Y} P \hookrightarrow \mathcal{L} P
$$ 

in turn is the subspace on those loops in $P$ which map $0 \in S^1$ to a chosen [[section]] of $P$ over $Y \times \{0\}$, then forming the pullback $i^\ast \Omega_Y P$ in

$$
  \array{
    i^\ast \Omega_Y P &\to& \Omega_Y P
    \\
    \downarrow && \downarrow
    \\
    Y &\stackrel{i}{\longrightarrow}& \mathcal{L}(Y \times S^1)
  }
$$

constitutes an [[equivalence of groupoids]] between 

1. $G$-[[principal bundles]] over $Y \times S^1$ with a trivialization over $Y \times \{0\}$ 

2. [[loop group]]-principal bundles over $Y$.

## Properties

### Relation to $Ext/Cyc$ adjunction
 {#RelationToExtCycAdjunction}

On the level of [[homotopy theory]] and [[isomorphism classes]] of principal bundles, the above Caloron correspondence is a special case of the [[Ext/Cyc-adjunction]] ([BMSS19 §2.2](#BMSS19)):


The latter applies to all [[circle principal bundles]] $X \longrightarrow Y$, classified by a possibly nontrivial [[first Chern class]] $c_1$, and gives that:

\[
  \label{ExtCycCorrespondence}
  \big( X \longrightarrow B G \big)
  \;\;
  \leftrightarrow
  \;\;
  \left(
  \begin{array}{ccc}
    Y &&\longrightarrow&& (L B G)\sslash S^1
    \\
    & \mathllap{_{c_1}}\searrow & & \swarrow\mathrlap{_{(L B G \to \ast) \sslash S^1 }}
    \\
    && B S^1 
  \end{array}
   \right)
   \mathrlap{\,,}
\]

as the special case of the general statement for the [[classifying space]] $B G$ replaced by *any* space $\mathcal{A}$.

In the case of [[connected topological space|connected]] $G$ we have

$$
  L B G \,\simeq\, B L G
$$

and hence 

$$
  (B L G) \sslash S^1 \,\simeq\, B( S^1 \ltimes L G )
  \mathrlap{\,.}
$$

In this generality the caloron correspondence appears (not under this name, though) in [Bergman & Varadarajan 2005](#BergmanVaradarajan05).


Specialized to trivial circle bundles $c_1 = 0$, the above correspondence (eq:ExtCycCorrespondence) becomes the [[internal hom]]-[adjointness](adjoint functor#InTermsOfHomIsomorphism):

\[
  \big( Y \times S^1 \longrightarrow B G \big)
  \;\;
  \leftrightarrow
  \;\;
  \big( Y \longrightarrow L B G \big)
\]

that the above discussion started with. At the level of [[principal infinity-bundles|principal $\infty$-bundles]] (ignoring geometric strcture) we may conclude from this the Caloron correspondence more abstractly: 

Observe that the condition for $Y \times S^1 \to B G$ to trivialize on $Y \simeq Y \times \{0\}$ means equivalently that $Y \longrightarrow L B G$ factors through the [[homotopy fiber]]

\[
  \Omega B G 
   \xrightarrow
     { hofib_{ev_0} }
  L B G
  \overset
    { ev_0 }
    {\longrightarrow}
  B G
\]

of the basepoint [[evaluation map]], being the [[based loop space]] of the [[classifying space]].

But that is

\[
  \Omega B G
    \underset{hmpt}{\simeq}
  G 
    \underset{hmpt}{\simeq}
  B \Omega G
\]

(cf. at *[[May recognition theorem]]*).


## Related concepts

* [[caloron]]

* [[Nahm transform]]

* [[double dimensional reduction]]


## References

The term "caloron correspondence" originates in:

* H. Garland, [[Michael Murray]]: _Kac-Moody monopoles and periodic instantons_. Comm. Math. Phys. **120** 2 (1988) 335--351 &lbrack;[doi:10.1007/BF01217968](https://doi.org/10.1007/BF01217968)&rbrack;

Application (not under this term, though) to [[duality between M-theory and type IIA string theory]]:

* [[Varghese Mathai]], [[Hisham Sati]]: *Some Relations between Twisted K-theory and $E_8$ Gauge Theory*, JHEP 0403:016 (2004) &lbrack;[doi:10.1088/1126-6708/2004/03/016](https://doi.org/10.1088/1126-6708/2004/03/016), [arXiv:hep-th/0312033](https://arxiv.org/abs/hep-th/0312033)&rbrack;

The general case (not assuming trivial circle bundles), but with focus on $G = $ [[E8]]:

* {#BergmanVaradarajan05} Aaron Bergman, Uday Varadarajan: *Loop Groups, Kaluza-Klein Reduction and M-Theory*, JHEP0506 043 (2005) &lbrack;[arXiv:hep-th/0406218](https://arxiv.org/abs/hep-th/0406218), [doi:10.1088/1126-6708/2005/06/043](https://doi.org/10.1088/1126-6708/2005/06/043)&rbrack;

recalled in

* [[Hisham Sati]]: *$E_8$ Gauge Theory and Gerbes in String Theory*, Adv. Theor. Math. Phys. **14** (2010) 1--39 &lbrack;[arXiv:hep-th/0608190](https://arxiv.org/abs/hep-th/0608190), [doi:10.4310/ATMP.2010.v14.n2.a2](http://doi.org/10.4310/ATMP.2010.v14.n2.a2)&rbrack;

* [[Hisham Sati]]: *The Loop Group of $E_8$ and Targets for Spacetime*, Mod. Phys. Lett. A **24** (2009) 25--40 &lbrack;[arXiv:hep-th/0701231](https://arxiv.org/abs/hep-th/0701231), [doi:10.1142/S0217732309028746](https://doi.org/10.1142/S0217732309028746)&rbrack;


Review and further developments:

* [[Michael Murray]], [[Raymond Vozzo]]: _The caloron correspondence and higher string classes for loop groups_, J. Geom. Phys. **60** 9  (2010) 1235--1250 &lbrack;[arXiv:0911.3464 math.DG](http://arxiv.org/abs/0911.3464), [doi:10.1016/j.geomphys.2010.05.003](https://doi.org/10.1016/j.geomphys.2010.05.003)&rbrack;

See also:

* Pedram Hekmati, [[Michael Murray]], [[Raymond Vozzo]], _The general caloron correspondence_, J. Geom. Phys. **62** 2 (2012) 224--241 &lbrack;[arXiv:1105.0805](http://arxiv.org/abs/1105.0805), [doi:10.1016/j.geomphys.2011.10.015](http://doi.org/10.1016/j.geomphys.2011.10.015)&rbrack;

The [[Ext/Cyc-adjunction]]:

* {#BMSS19} [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]]; §2.2 of: _[[schreiber:Gauge enhancement of Super M-Branes|Gauge enhancement of Super M-Branes via rational parameterized stable homotopy theory]]_, Communications in Mathematical Physics **371** 197 (2019) &lbrack;[doi:10.1007/s00220-019-03441-4](https://doi.org/10.1007/s00220-019-03441-4), [arXiv:1806.01115](https://arxiv.org/abs/1806.01115)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]]; §2.2 of: *[[schreiber:Cyclification of Orbifolds]]*, Comm. Math. Phys. **405** 67 (2024) &lbrack;[doi:10.1007/s00220-023-04929-w](https://doi.org/10.1007/s00220-023-04929-w), [arXiv:2212.13836 math.AT](https://arxiv.org/abs/2212.13836), [[schreiber:cyclic loop spaces 2022|talk]]&rbrack;


[[!redirects caloron correspondences]]
