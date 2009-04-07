

{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
###### Lexicon
##Lexicon##
This continues from [[graded vector space]] a lexicon of terminology relating to differential graded objects, especially as relate to [[rational homotopy theory]].
=--
**Definition**

**Differential (pre-)graded vector spaces.**
(We continue from [[graded vector space|graded vector spaces]] with the terminology of pre-gvs for the general case and gvs for the positively or negatively graded ones.)

A **differential (pre-)graded vector space**, (dgvs), is a pair $(V,\partial)$, where $V$ is a (pre-)graded vector space and $\partial \in Hom_{-1}(V,V)$ satisfies $\partial\circ\partial = 0$. 

This endomorphism, $\partial$, of degree -1 is called the [[differential]] or sometimes the _boundary operator_ of the dgvs.

To link it with [[differential object]], note that using the suspension (as in [[graded vector space]]) as the translation (see [[category with translation]]) and then the differential is $\partial : V\to s(V)$. A dgvs is essentially the same as a [[chain complex]] of vector spaces. (Some questions of terminology are addressed further down this entry.)

As usual, $Ker \partial / Im \partial$ is called the [[homology]] of $(V,\partial)$, denoted $H(V,\partial)$.




Let $(V,\partial)$, $(V',\partial')$ be two pre-dgvs

$$Hom(V,V') = \bigoplus_{p\in \mathbb{Z}}Hom_p(V,V')$$

is a pre-dgvs with differential

$$Df = \partial'\circ f - (-1)^{|f|}f\circ\partial$$

for $f$ homogeneous.

A degree $r$ linear morphism $f$ is _compatible with the differentials_ if it is a cycle for this differential $D$, i.e., $Df = 0$ or $\partial' f = (-1)^{r}f\partial.$

A **morphism between pre-dgvs** is a linear morphism of degree 0 that is compatible with the differentials:

$$f: (V,\partial)\to (V',\partial').$$ 

This induces $H(f): H(V,\partial)\to H(V',\partial').$

We get a category $pre -  DGVS$ and $H$ is a functor $H : pre\! -\! DGVS\to pre\!-\! GVS$.


**Weak equivalences or [[quasi-isomorphism|quasi-isomorphisms]]**

If $f: (V,\partial)\to (V',\partial')$ in {\sf pre-DGVS}, then $f$ is a **weak equivalence** or [[quasi-isomorphism]] if $H(f)$ is an isomorphism.  In this case we write $f: (V,\partial)\stackrel{\simeq}{\to} (V',\partial')$



**Homotopies**

Let  $f,f' : (V,\partial)\to (V',\partial')$ be two morphisms in $pre-DGVS$. We say $f$ and $f'$ are **homotopic** denoted $f\sim f'$ if $f-f'$ is a boundary in $(Hom(V,V'),D)$, i.e., there is some $h : V \to V'$ of degree +1 such that $f-f' = Dh = \partial' h + h\partial$.

**Contractable and Acyclic DGVSs**

 A dgvs $(V,\partial)$ is _contractible_ if the identity map on $V$ is homotopic to the zero morphism and is _acyclic_ if $H(V,\partial) = 0$.


**Remarks**

(i) A _contracting homotopy_ $h : Id_V \sim O_V$ is a degree 1 map such that $\partial h(x) + h(\partial x) = x$ for  all $x$ in $V_p$.

(ii) If $(V,\partial)$ is contractible, then it is acyclic and conversely.  The converse depends strongly on our working with vector spaces.  If we worked with modules over a commutative ring, $k$, then the correct result would be ''If $(V,\partial)$ is acyclic and projective in each dimension, then it is contractible.'' This is important when looking at, for instance, diagrams of dgvs since even if each individual object in the diagram may be contractible, it might be impossible to pick the contracting homotopies to give a map of diagrams, i.e., to be compatible with the structural maps.


**Suspension for (pre-) dgvs**

If $(V,\partial)$ is a pre-dgvs, then its $r$-suspension $(s^rV,\partial)$, is the $r$-suspension, $s^rV$, of $V$ together with the differential

$$\partial s^rv = (-1)^rs^r(\partial v).$$

**Tensor product of (pre-) dgvs**

If $(V,\partial)$, and $(V',\partial')$ are pre-dgvs, then we give the tensor product, $V\otimes V'$, the differential given on generators by

$$ \partial(v\otimes v') = (\partial v) \otimes v' + (-1)^{|v|}v \otimes (\partial' v' ),$$

and we denote the result by $(V,\partial)\otimes (V', \partial')$. We have ([[Kunneth Theorem]])
$$H((V,\partial)\otimes (V', \partial')) \cong H(V,\partial)\otimes H(V', \partial').$$


**Duals of (pre-)dgvs**

The dual $\#(V,\partial) = (\# V,\#\partial)$ of a pre-dgvs $(V,\partial)$ is given by $\# V$ with differential $(\# \partial ) = - ^t \partial$.  This satisfies 

$$\langle(\# \partial)f; v\rangle + (-1)^{|f|}\langle f; \partial v\rangle = 0.$$

**Chains and cochains: terminology**

If $(V,\partial)$ is a pre-dgvs with 'lower grading' that is the summands are written $V_p$, then $(V,\partial)$ may be called a [[chain complex]] and terms such as _cycle_, _boundary_, [[homology]] are used with the usual meanings. 


If $(V,\partial)$ is presented with the 'upper grading', so $V^p$, then the corresponding words will have a 'co' as prefix, cochain complex, cocycle, etc.  

There is no real distinction between the two cases in the abstract, but in applications there is often a fixed 'dimensional' interpretation and then the 'natural' and 'geometric' aspects determine which is more appropriate or useful. 
{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
###### Lexicon links onwards:

[[Tim Porter|Tim]]:  The lexicon will continue on a new entry on [[differential graded algebra|differential graded algebras]].  (Yes I know there is [[dg-algebra]] already but as I said before, these lexicon pages are for editing and I am not 100% happy about the terminological conventions on that existing page, nor am I suggesting that this lexicon gets things 'right'!
=--