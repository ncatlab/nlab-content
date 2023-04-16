
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{T}$ a [[sheaf topos]], $G \in Grp(\mathcal{T})$ a [[group object]] and $V \in \mathcal{T}$ any object, and for $\rho \colon V \times G \to V$ an [[action]] of $G$ on $V$  , the **quotient stack** $V// G$ is the [[quotient]] of this action but formed not in $\mathcal{T}$ but under the inclusion

$$
  \mathcal{T} \hookrightarrow \mathbf{H}
$$

into the [[(2,1)-topos]] over the given [[site]] of definition: it is the quotient after regarding the action as an [[infinity-action]] in $\mathbf{H}$.

This is the geometric version of the notion of _[[action groupoid]]_. A wider notion of the quotient stack may be defined using more general internal groupoids. Indeed,
the [[small fibration]] obtained by the [[externalization]] of an internal groupoid in a site with pullbacks will be a [[fibered category]] which is a candidate for a quotient stack in this context. For many interesting sites, sometimes under additional conditions on the internal groupoid, the resulting small fibration is indeed a stack.

If the [[stabilizer subgroups]] of the [[action]] are [[finite groups]], then the quotient stack is an [[orbifold]]/[[Deligne-Mumford stack]] --the "quotient orbifold".

## Motivation for definition of quotient stack. 

Let $G$ be a Lie group action on a manifold $X$ (left action). 

We define the quotient stack $[X/G]$ as 
$$
[X/G](Y):=\{P\xrightarrow{p} Y, P\xrightarrow{f}X | P\rightarrow Y \,\text{is a G-bundle,}\, f \,\text{is}\, G\text{-equivariant}\}.
$$ 

Morphisms of objects are $G$-equivariant isomorphisms. This definition is taken from Heinloth's [Some notes on Differentiable stacks](https://www.uni-due.de/~hm0002/stacks.pdf).

Given a Lie group action of $G$ on $X$, if we want to associate a stack, we  start with simpler cases which allows us to guess how to define $[X/G]$ in general.

1. Suppose $X$ is trivial and $G$ acts trivially on $X=\{*\}$ then $[X/G]$ should only depend on $G$. We know what stack to associate for a Lie group $G$ i.e., $BG$. Thus, $[X/G]$ should just be $BG$.

2. Suppose $G$ is trivial and $G$ acts on $X$, $[X/G]$ should only depend on $X$. We know what stack to associate for a manifold $X$ i.e., $\underline{X}$. Thus, $[X/G]$ should just be $\underline{X}$.

3. Suppose $G$ is non trivial and $X$ is non trivial and that the action of $G$ on $X$ is free (and proper) so that $X/G$ is a manifold. We know what stack to associate for a manifold $X/G$ i.e., $\underline{X/G}$. Thus, $[X/G]$ should just be $\underline{X/G}$. 

 
For general case of $G$ acting on $X$, we get a Lie groupoid, called the Translation groupoid (or action groupoid) usually denoted by $G\ltimes X$. 

* Given a manifold $M$, we have a stack associated to it, namely $\underline{M}$. Given a Lie group $G$, we have a stack associated to it, namely $BG$. Given a Lie groupoid $\mathcal{G}$, we have a stack associated to it, namely $B\mathcal{G}$ i.e., the stack of principal groupoid $\mathcal{G}$ bundles.

For action groupoid $\mathcal{G}=G\ltimes X$, let $B\mathcal{G}$ be the corresponding stack of principal $\mathcal{G}$ bundles. It turns out that $B\mathcal{G}$ is same $[X/G]$ defined above. More details to be found in [this page](https://mathoverflow.net/questions/319038/motivation-for-definition-of-quotient-stack).


 * If action of the Lie group $G$ on the manifold $X$ is free and proper, what we get is   **a manifold** $X/G$. Stack associated to this manifold is $\underline{X/G}$ which we call to be the quotient stack, denote by $[X/G]$.


 * If the action of the Lie group $G$ on the manifold $X$ is not necessarily free and proper, what we get is   **a Lie groupoid** denoted (among other symbols) by $X//G$. Stack associated to this Lie groupoid $X//G$ is $B(X//G)$ which we call to be the quotient stack, denote by $[X/G]$.

## Universal property (??) for Quotient stack
 {#AsFibrationsOverBG}

> (references for what the following paragraphs are getting at are listed [below](#ReferencesAsFibrationsOverBG))

Let $G$ be a Lie group and $X$ be a manifold with a $G$-action. 

Supposing that $G$ acts freely and properly on $X$, the quotient stack $[X/G]$ will be the stack $\underline{X/G}$. 
This action yields a [[principal bundles|principal $G$-bundle]] of manifolds $X\rightarrow X/G$, which gives a morphism of stacks $\underline{X}\rightarrow \underline{X/G}$. We refer to this stack morphism $\underline{X}\rightarrow \underline{X/G}$ as a principal $G$-bundle of stacks. 

More precisely, a stack morphism $\underline{M}\rightarrow \mathcal{D}$ is said to be **representable** if given a manifold $N$ and a stack morphism $\underline{N}\rightarrow \mathcal{D}$, the fiber product $\underline{M}\times_{\mathcal{D}}\underline{N}$ is a manifold. 
A representable morphism of stacks is said to be a **principal $G$ bundle of stacks** if the map $\underline{M}\times_{\mathcal{D}}\underline{N}\rightarrow N$ is a principal $G$-bundle of manifolds. 
The stack morphism $\underline{X}\rightarrow \underline{X/G}$ is a principal $G$-bundle of stacks, since the map
$X\rightarrow X/G$ is a principal $G$-bundle of manifolds. 

The property "$\underline{X}\rightarrow \underline{X/G}$ is a principal $G$-bundle" is the main ingredient in the definition of the quotient stack $[X/G]$.  Irrespective of whether or not $G$ acts freely and properly on $X$, we still want to define a *quotient stack* as a stack $\mathcal{D}$ such that $\underline{X}\rightarrow \mathcal{D}$ is a principal $G$-bundle of stacks in a "minimal" way. 

The **quotient stack of the action of $G$ on $X$** is a stack $\mathcal{D}$ equipped with a principal $G$-bundle of stacks $\underline{X}\rightarrow \mathcal{D}$ such that any other principal $G$-bundle of stacks $\underline{X}\rightarrow \mathcal{C}$ factors through $\underline{X}\rightarrow \mathcal{D}$. 

If $G$ acts freely and properly, then an obvious choice for $\mathcal{D}$ is the stack $\underline{X/G}$. By the universal property, $\mathcal{D}$ must be precisely the stack appearing in the definition of quotient stacks, i.e. 
$$
\mathcal{D}(Y):=\{P\xrightarrow{p} Y, P\xrightarrow{f}X | P\rightarrow Y \,\text{is a}\, G\text{-bundle,}\, f  \,\text{is}\, G\text{-equivariant}\}.
$$ 

Morphisms of quotient stacks are isomorphisms of principal $G$-bundles that commute with $G$-equivariant morphisms. Fixing notation, we write $[X/G]$ for $\mathcal{D}$ and refer to this as **the quotient stack**. 



## Properties

### Relation to principal and associated bundles

For $V = *$ the [[terminal object]], one writes $\mathbf{B}G \coloneqq *// G$.  This is the [[moduli stack]] for $G$-[[principal bundles]]. It is also the trivial _$G$-[[gerbe]]_.

There is a canonical projection $\overline{\rho} \;\colon\; V// G \to \mathbf{B}G$. This is the [[universal associated infinity-bundle|universal rho-associated bundle]].


## Related concepts

* [[quotient]], [[quotient space]], [[quotient type]]

* [[action groupoid]], [[global quotient orbifold]]

* [[local quotient stack]]

* [[Borel construction]]

* [[(infinity,1)-colimit]], [[infinity-action]]

* [[mapping stack]]

* [[orbifold]], [[Deligne-Mumford stack]]

* [[geometric invariant theory]]

## References
 {#References}

### As stackification of action groupoids

The definition of quotient stacks as [[stackifications]] of ([[(2,1)-presheaves|presheaves of]]) [[action groupoids]] is considered for instance in:

* {#LaumontMoret-Bailly} [[Gérard Laumon]], [[Laurent Moret-Bailly]], Prop. 4.3.1 in: _Champs alg&#233;briques_, Ergebn. der Mathematik und ihrer Grenzgebiete **39**, Springer (2000) &lbrack;[doi:10.1007/978-3-540-24899-6](https://doi.org/10.1007/978-3-540-24899-6)&rbrack;

* [[Stacks Project]], Definition 77.20.1 in: *Quotient Stacks* &lbrack;[tag:044Q](https://stacks.math.columbia.edu/tag/044Q)&rbrack;

### As presheaves of equivariant maps out of principal bundles 

The construction of quotient stacks $X\sslash G$ as [[prestacks]] of $G$-[[principal bundles]] equipped with $G$-[[equivariant maps]] to $X$ is considered for instance in:

* [[Jochen Heinloth]], Exp. 1.5 in: *Notes on differentiable stacks* (2004) &lbrack;[pdf](https://math.nyu.edu/~tschinke/WS04/pdf/heinloth.pdf), [[Heinloth-DifferentiableStacks.pdf:file]]&rbrack;

* [[Frank Neumann]], p. 28 in: *Algebraic Stacks and Moduli of Vector Bundles*, impa (2011) &lbrack;[pdf](https://impa.br/wp-content/uploads/2017/04/PM_36.pdf), [pdf](https://www.cimat.mx/~luis/seminarios/Pilas-algebraicas/neumann-Stacks.pdf)&rbrack;

* [[Michael Groechenig]], Def. 5.23 in: *Algebraic Stacks*, Lecture notes (2014) &lbrack;[web](http://individual.utoronto.ca/groechenig/stacks.html), [pdf](http://individual.utoronto.ca/groechenig/stacks.pdf), [[Groechenig-AlgebraicStacks.pdf:file]]&rbrack;

* {#Halpern-Leistner20} [[Daniel Halpern-Leistner]], Section 7.1 of: *Moduli theory*, Lecture notes (2020) &lbrack;[pdf](http://pi.math.cornell.edu/~danielhl/moduli_theory_notes.pdf), [[Halpern-Leistner_ModuliTheory.pdf:file]]&rbrack;

Discussion of sufficient conditions for this construction to really yield a [[stack]] (instead of just a [[prestack]]):

* [[Elena Caviglia]], *Generalized principal bundles and quotient stacks* &lbrack;[arXiv:2302.07852](https://arxiv.org/abs/2302.07852)&rbrack;

### As fibrations over $\mathbf{B}G$
 {#ReferencesAsFibrationsOverBG}

The characterization of quotient stacks $X \sslash G$ as fibrations over [[looping and delooping|delooping stacks]] $\ast \sslash G \simeq \mathbf{B}G$ with [[homotopy fiber]] $X$ (cf. also the discussion at *[[infinity-action|$\infty$-action]]*):

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Exp. 4.4 in: _[[schreiber:Principal ∞-bundles -- models and general theory|Principal $\infty$-bundles -- General theory]]_, J. Hom. Rel. Struc. **10** 4 (2015) 749-801 &lbrack;[arXiv:1207.0248](https://arxiv.org/abs/1207.0248), [doi:10.1007/s40062-014-0083-6](http://link.springer.com/article/10.1007/s40062-014-0083-6)&rbrack;

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], Prop. 2.79 in: _[[schreiber:Proper Orbifold Cohomology]]_ &lbrack;[arXiv:2008.01101](https://arxiv.org/abs/2008.01101)&rbrack;

* {#SatiSchreiber21} [[Hisham Sati]], [[Urs Schreiber]], Prop. 0.2.1 (ii) & Prop. 3.2.76 in: *[[schreiber:Equivariant principal infinity-bundles|Equivariant principal $\infty$-bundles]]* &lbrack;[arXiv:2112.13654](https://arxiv.org/abs/2112.13654)&rbrack;

* [Halpern-Leistner (2020), Exc. 7.2](#Halpern-Leistner20)  

### More

See also:

* [[Jack Morava]], _Theories of anything_ ([arXiv:1202.0684](http://arxiv.org/abs/1202.0684))


[[!redirects quotient stacks]]

[[!redirects orbifold quotient]]
[[!redirects orbifold quotients]]

[[!redirects quotient orbifold]]
[[!redirects quotient orbifolds]]

[[!redirects stacky quotient]]
