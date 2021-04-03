
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Real numbers object
* table of contents
{: toc}

## Idea

Recall that it is possible to define an [[internalization]] of the set of [[natural numbers]], called a [[natural numbers object]] (NNO), in any [[cartesian monoidal category]] (a category with finite [[product|products]]). In particular, the notion makes sense in a [[topos]]. But a topos supports [[intuitionistic logic|intuitionistic]] [[higher-order logic]], so once we have an NNO, it is also possible to repeat the usual construction of the [[integer|integers]], the [[rational number|rationals]], and then finally the [[real number|real numbers]]; we thus obtain an internalization of $\mathbb{R}$ in any topos with an NNO.

More generally, we can define a real numbers object (RNO) in any category with sufficient structure (somewhere between a cartesian monoidal category and a topos).  Then we can prove that an RNO exists in any topos with an NNO (and in some other situations).


## Definition

Let $\mathcal{E}$ be a [[Heyting category]].  (This means, in particular, that we can interpret full [[first-order logic|first-order]] [[intuitionistic logic]] using the [[stack semantics]].)

+-- {: .num_defn}
###### Definition

A (located Dedekind) __real numbers object__ in $\mathcal{E}$ is a [[ring object]] in $\mathcal{E}$ that satisfies (in the [[internal logic]]) the axioms of a [[Dedekind-complete]] [[linearly ordered]] [[Heyting field]].
=--

In detail:

A _commutative ring object_ in $\mathcal{E}$ is an object $R$ equipped with morphisms $0\colon \mathbf{1} \to R$, ${-}\colon R \to R$, ${+}\colon R \times R \to R$, $1\colon \mathbf{1} \to R$, and ${\cdot}\colon R \times R \to R$ (where $\mathbf{1}$ is the [[terminal object]] of $\mathcal{E}$ and $\times$ is the [[product]] operation in $\mathcal{E}$) that make certain diagrams commute.  (These diagrams may be found at [[ring object]], in principle, although right now they\'re not there.)

Given a commutative ring object $R$ in $\mathcal{E}$, we define a [[binary relation]] $\#$ on $R$ (that is a [[subobject]] of $R \times R$) as
$$ \{ (x,y)\colon R \times R \;|\; \exists z\colon R.\, x \cdot z = y \cdot z + 1 \} ,$$
written in the [[internal language]] of $\mathcal{E}$.  Then $R$ is a (Heyting) _field object_ if $\#$ is a tight [[apartness relation]]; that is if the following axioms (in the internal language) hold:

*  [[irreflexive relation|irreflexivity]]: $\forall x\colon R.\, \neg(x \# x)$,
*  [[symmetric relation|symmetry]]: $\forall x\colon R.\, \forall y\colon R.\, (x \# y \implies y \# x)$ (which can actually be proved using $-$),
*  [[comparison relation|comparison]]: $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, (x \# z \implies (x \# y \vee y \# z))$,
*  [[tight relation|tightness]]: $\forall x\colon R.\, \forall y\colon R.\, (\neg(x \# y) \implies x = y)$.

A (linearly) _ordered field object_ in $\mathcal{E}$ is a field object $R$ equipped with a binary relation $\lt$ such that the following axioms hold:

*  strong [[irreflexive relation|irreflexivity]]: $\forall x\colon R.\, \forall y\colon R.\, (x \lt y \implies x \# y)$,
*  strong [[connected relation|connectedness]]: $\forall x\colon R.\, \forall y\colon R.\, (x \# y \implies (x \lt y \vee y \lt x))$,
*  [[transitive relation|transitivity]]: $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, ((x \lt y \wedge y \lt z) \implies x \lt z)$,
*  respecting addition: $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, (x \lt y \implies x + z \lt y + z)$,
*  respecting multiplication: $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, ((x \lt y \wedge 0 \lt z) \implies x \cdot z \lt y \cdot z)$.

Given an ordered field object $R$ in $\mathcal{E}$, any object $\Gamma$ in $\mathcal{E}$, and subobjects $L$ and $U$ of $\Gamma \times R$, we say that $(L,U)$ is a _Dedekind cut_ in $R$ (parametrised by $\Gamma$) if the following axioms hold:

*  lower bound: $\forall a\colon \Gamma.\, \exists x\colon R.\, (a,x) \in L$,
*  upper bound: $\forall a\colon \Gamma.\, \exists x\colon R.\, (a,x) \in U$,
*  downward roundedness: $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, ((x \lt y \wedge (a,y) \in L) \implies (a,x) \in L)$,
*  upward roundedness: $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, (((a,x) \in U \wedge x \lt y) \implies (a,y) \in U)$,
*  upward openness: $\forall a\colon \Gamma.\, \forall x\colon R.\, ((a,x) \in L \implies \exists b\colon \Gamma.\, \exists y\colon R.\, ((b,y) \in L \wedge x \lt y))$,
*  downward openness: $\forall a\colon \Gamma.\, \forall x\colon R.\, ((a,x) \in U \implies \exists b\colon \Gamma.\, \exists y\colon R.\, ((b,y) \in U \wedge y \lt x))$,
*  locatedness: $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, (x \lt y \implies ((a,x) \in L \vee (a,y) \in U))$,
*  separation: $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, (((a,x) \in L \wedge (a,y) \in U) \implies x \lt y)$.

An ordered field object $R$ in $\mathcal{E}$ is _Dedekind complete_ if, given any object $\Gamma$ of $\mathcal{E}$ and any Dedekind cut $(L,U)$ in $R$ parametrised by $\Gamma$, there exists a morphism $x\colon \Gamma \to R$ such that
$$ L = \{ (a,b)\colon \Gamma \times R \;|\; b \lt x(a) \} ,$$
$$ U = \{ (a,b)\colon \Gamma \times R \;|\; x(a) \lt b \} .$$

Finally, a _real numbers object_ in $\mathcal{E}$ is a Dedekind-complete ordered field object.


## Properties

In the last requirement, of Dedekind completeness, we postulate (under certain conditions) the existence of a morphism $x\colon \Gamma \to R$ satisfying certain properties.
+-- {: .num_thm}
###### Theorem
This morphism is in fact unique.
=--
Here is an explicit 'external' proof:
+-- {: .proof}
###### Proof
Suppose that $x, x'\colon \Gamma \to R$ both satisfy the required properties, and consider $x \# x'$, which is a subobject of $\Gamma$.  By the strong connectedness of $\lt$, $x \# x'$ is contained in (factors through) $x \lt x' \vee x' \lt x$, which is the [[union]] of $x \lt x'$ and $x' \lt x$.

Now consider $x \lt x'$, and let $a$ be a [[generalised element]] of $\Gamma$.  If $a$ belongs to (factors through) $x \lt x'$, or equivalently $(x(a), x'(a))$ belongs to $\lt$, it follows that $(a,x(a))$ belongs to $L$.  Thus, $(x(a), x(a))$ also belongs to $\lt$, or equivalently $a$ belongs to $x \lt x$.  By the strong irreflexivity of $\lt$, this is contained in $x \# x$; by the irreflexivity of $\#$, this is contained in $\bot$ (as a subobject of $\Gamma$).  Since every $a$ that belongs to $x \lt x'$ belongs to $\bot$, $x \lt x'$ is contained in (and so equals as a subobject) $\bot$.

Similarly (either by swapping $x$ with $x'$ or by using $U$ instead of $L$), $x' \lt x$ is also $\bot$.  Therefore, $x \# x'$ is $\bot$.  By the tightness of $\#$, $x = x'$.
=--
Here is an 'internal' proof, to be interpreted in the [[stack semantics]] of $\mathcal{E}$:
+-- {: .proof}
###### Proof
Suppose that $x, x'\colon R$ both satisfy the required properties, and suppose that $x \# x'$.  By the strong connectedness of $\lt$, $x \lt x'$ or $x' \lt x$.

Now suppose that $x \lt x'$.  It follows that $x$ belongs to $L$, so $x \lt x$.  By the strong irreflexivity of $\lt$, $x \# x$; by the irreflexivity of $\#$, we have a contradiction.

Similarly (either by swapping $x$ with $x'$ or by using $U$ instead of $L$), $x' \lt x$ is also false.  Therefore, $x \# x'$ is false.  By the tightness of $\#$, $x = x'$.
=--

In the definition of a Heyting field object, all of the axioms except the last are [[coherent logic|coherent]] and therefore make sense in any [[coherent category]].
+-- {: .num_thm}
###### Theorem
An object satisfying all but the last axiom of a field object is precisely a [[local ring]] object (so in particular an RNO is a local ring object).
=--
+-- {: .proof}
###### Proof
...
=--

It would be nice to say that a Heyting category with an RNO must have an NNO; after all, $\mathbb{N}$ is contained in $\mathbb{R}$.  However, my only argument is impredicative; although I don't know a specific example, there could be a [[Π-pretopos]] with an RNO but no NNO.  However, the argument works for a [[infinitary coherent category|geometric]] Heyting category or a [[topos]].  (In light of the constructions below, the existence of an RNO is therefore equivalent to the existence of an NNO in a topos.)
+-- {: .num_thm}
###### Theorem
If $R$ is an RNO in an infinitary Heyting category or topos, then there is unique subobject $N$ of $R$ that is both a sub-[[rig]] object of $R$ and an NNO under the operations $0\colon \mathbf{1} \to N$ and $({-}) + 1\colon N \to N$.
=--
+-- {: .proof}
###### Proof
...
=--

We usually speak of *[[the]]* RNO, if one exists.  This is because any two RNOs in a Heyting category with an NNO are [[isomorphic]], in an essentially unique way.  (I can't prove this without an NNO, although the previous theorem shows that we often have one.)
+-- {: .num_thm}
###### Theorem
If $R$ and $R'$ are both RNOs in a Heyting category $\mathcal{E}$ with an NNO, then there is a unique isomorphism from $R$ to $R'$ that preserves the structures on them ($0$, $-$, $+$, $1$, $\cdot$, $\lt$).
=--
+-- {: .proof}
###### Proof
...
=--


## Constructions

We can construct a real numbers object in the following cases (presumably among others):

1. in a topos with an NNO;
2. in a $\Pi$-[[Pi-pretopos|pretopos]] with an NNO and [[weak countable choice]];
3. in a $\Pi$-pretopos with an NNO and [[subset collection]].

(Actually, (1) is a special case of (3), but the usual construction in (1) is not available in (3).  Thus, we still have three different constructions to consider.)


### In a topos with an NNO

Let $\mathcal{E}$ be an [[elementary topos]] with a natural numbers object $\mathbb{N}$. The **Dedekind real numbers object** of $\mathcal{E}$ is the object of all [[Dedekind cut|Dedekind cuts]]. To be more precise, we will need to make some auxiliary definitions.

We first construct an integers object as follows. Let $a, b\colon E \to \mathbb{N} \times \mathbb{N}$ be the [[kernel pair]] of the addition map ${+}\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}$, and let $\pi_1, \pi_2\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ be the [[product]] projections. We define $\mathbb{Z}$ to be the [[coequalizer]] of $(\pi_1 \circ a, \pi_2 \circ b), (\pi_2 \circ a, \pi_1 \circ b)\colon E \to \mathbb{N}$. A similar construction yields a rational numbers object $\mathbb{Q}$. 

We denote by $\mathcal{P}(A)$ the [[power object]] of $A$ in $\mathcal{E}$. A **Dedekind cut** is a [[generalized element]] $(L, U)$ of $\mathcal{P}(\mathbb{Q}) \times \mathcal{P}(\mathbb{Q})$, satisfying the following conditions, expressed in the [[Mitchell-Bénabou language]] of $\mathcal{E}$ and interpreted under [[Kripke-Joyal semantics]]:

1. Non-degenerate:
   $$ \exists q\colon \mathbb{Q}.\, q \in L ;$$
   $$ \exists r\colon \mathbb{Q}.\, r \in U .$$

2. Inward-closed:
   $$ \forall q\colon \mathbb{Q}.\, \forall r\colon \mathbb{Q}.\, ((q \lt r \wedge r \in L) \implies q \in L) ;$$
   $$ \forall q\colon \mathbb{Q}.\, \forall r\colon \mathbb{Q}.\, ((r \lt q \wedge r \in U) \implies q \in U) .$$

3. Outward-open:
   $$ \forall q\colon \mathbb{Q}.\, (q \in L \implies \exists r\colon \mathbb{Q}.\, (r \in L \wedge q \lt r)) $$
   $$ \forall q\colon \mathbb{Q}.\, (q \in U \implies \exists r\colon \mathbb{Q}.\, (r \in L \wedge r \lt q)) .$$

4. Located:
   $$ \forall q\colon \mathbb{Q}.\, \forall r\colon \mathbb{Q}.\, (q \lt r \implies (q \in L \vee r \in U)) .$$

5. Mutually exclusive:
   $$ \forall q\colon \mathbb{Q}.\, \neg(q \in L \wedge q \in U) .$$

The relation $\lt$ on $\mathbb{Q}$ is the order relation constructed in the usual way. We define $\mathbb{R}$ to be the subobject of $\mathcal{P}(\mathbb{Q}) \times \mathcal{P}(\mathbb{Q})$ consisting of all Dedekind cuts as defined above.


### In a $\Pi$-pretopos with $WCC$

Summary: construct a [[Cauchy real numbers]] object and use $WCC$ ([[weak countable choice]]) to prove that it is an RNO.

Note that any [[Boolean topos]] with an NNO satisfies $WCC$, so in all we have three different constructions available in that case.


### In a $\Pi$-pretopos with an NNO and subset collection

Summary: modify the construction of a [[Cauchy real numbers]] object to use [[multi-valued function|multi-valued]] [[Cauchy sequences]].


## Examples

### In $Set$

The real numbers object in [[Set]] is the [[real line]], the usual set of (located Dedekind) [[real numbers]].  Note that this is a theorem of [[constructive mathematics]], as long as we assume that $Set$ is an elementary topos with an NNO (or more generally a [[Π-pretopos]] with [[natural numbers object|NNO]] and either WCC or subset collection).


### In sheaves on a topological space

Let $X$ be a [[topological space]], and $\mathrm{Sh}(X)$ its [[category of sheaves]]. It is well-known that $\mathrm{Sh}(X)$ is a [[Grothendieck topos]] (and so, _a fortiori_, an elementary topos), and the [[constant sheaf]] [[functor]] $\Delta\colon \mathbf{Set} \to \mathrm{Sh}(X)$ preserves [[finite limits]] and has the [[global section]] functor $\Gamma\colon \mathrm{Sh}(X) \to \mathbf{Set}$ as a [[right adjoint]]. (Hence, $\Delta$ and $\Gamma$ are the components of a [[geometric morphism]] $\mathrm{Sh}(X) \to \mathbf{Set}$.) The following claims are essentially immediate:

1. If $\mathbf{N}$ is the set of natural numbers, then $\Delta (\mathbf{N})$ must be an NNO in $\mathrm{Sh}(X)$, since $\Delta$ has a right adjoint. 

2. If $\mathbf{Z}$ is the set of integers, then $\Delta (\mathbf{Z})$ is an integers object in $\mathrm{Sh}(X)$ (as defined above), since $\Delta$ preserves finite limits and colimits.

3. Similarly, if $\mathbf{Q}$ is the set of rational numbers, then $\Delta (\mathbf{Q})$ is a rational numbers object in $\mathrm{Sh}(X)$.

Thus, for every topological space $X$, the topos $\mathrm{Sh}(X)$ has a Dedekind real numbers object $\mathbb{R}$. Na&#239;vely one might expect $\mathbb{R}$ to be isomorphic to the constant sheaf $\Delta(\mathbf{R})$, where $\mathbf{R}$ is the classical set of real numbers, but this turns out not to be the case. Instead, we have a rather more remarkable result:

+-- {: .num_theorem #DedekindRealsInToposOverTopologicalSpace}
###### Theorem

A Dedekind real numbers object $\mathbb{R}$ in the topos $\mathrm{Sh}(X)$ is isomorphic to the sheaf of real-valued [[continuous functions]] on $X$.

=--

This is shown in ([MacLane-Moerdijk, Chapter VI, &#167;8, theorem 2](#MM94)); see also below.

+-- {: .num_remark}
###### Remark

Theorem \ref{DedekindRealsInToposOverTopologicalSpace} allows us to define various further constructions on $X$ in internal terms in $\mathrm{Sh}(X)$; for example, a [[vector bundle]] over $X$ is an internal [[projective object|projective]] $\mathbb{R}$-[[module]].

=--

### In sheaves on a gros site of topological spaces
 {#InGrosToposOnTopologicalSpaces}


+-- {: .num_theorem}
###### Theorem

Let $\{\mathbb{R}\} \hookrightarrow S \hookrightarrow Top$ be a [[small category|small]] [[full subcategory]] of [[Top]] including the [[real line]].  If $S$ is closed under forming [[open subspaces]] and pullbacks of open subspaces and we equip it with the open-cover [[coverage]], then the Dedekind real number object internal to $Sh(S)$ is [[representable functor|represented]] by $\mathbb{R}^1$.
=--

This is proven as ([MacLane-Moerdijk,  chapter VI &#167;9, theorem 2](#MM94)) under the stronger assumption that $S$ is closed under open subspaces and finite limits, by showing that over each object in the site the argument reduces essentially to that of theorem \ref{DedekindRealsInToposOverTopologicalSpace} for that object.  However, the finite limits are not necessary; see also below.  The more general version includes the cases

* $S =$ $\{$ [[locally contractible topological spaces]] $\}$

* $S =$ $\{$ [[topological manifolds]] $\}$

(for which $Sh(S)$ is [[cohesive topos]] and $Sh_\infty(S)$ is an [[cohesive (∞,1)-topos]]).


### In a general sheaf topos
 {#InASheafTopos}

We can generalize the above theorem as follows.  Let $S$ be any [[site]], and for any object $X\in S$ let $L(X)$ denote the [[locale]] whose [[frame]] of opens is the frame of [[subobjects]] of the sheafified representable $y X \in Sh(S)$.  We have an induced functor $L:S\to Loc$.  We can also regard the ordinary real numbers $\mathbb{R}$ as a locale.

+-- {: .num_theorem}
###### Theorem
The Dedekind real number object in $Sh(S)$ is the functor $Loc(L-,\mathbb{R})$.
=--
+-- {: .proof}
###### Proof
The sheaf topos $Sh(\mathbb{R})$ is the classifying topos of the geometric theory of a real number, in the sense that for any Grothendieck topos $E$, geometric morphisms $E \to Sh(\mathbb{R})$ are equivalent to global points of the real numbers object $\mathbb{R}_E$ in $E$.  Since pullback functors are logical, they preserve the real numbers object; thus for any $X\in E$, maps $X\to \mathbb{R}_E$ are equivalent to geometric morphisms $E/X \to Sh(\mathbb{R})$.  But $Sh(\mathbb{R})$ is localic, so such geometric morphisms factor through the localic reflection of $E/X$, and therefore are equivalent to continuous $\mathbb{R}$-valued functions defined on the "little locale of $X$", i.e. the locale associated to the frame of subobjects of $X$ in $E$.

Therefore, if $E = Sh(S)$ for some site $S$, then $\mathbb{R}_E$ is the sheaf on $S$ where $\mathbb{R}_E(X)=$ the set of continuous $\mathbb{R}$-valued functions on the little locale of $y X \in E$, which is what we have called $L X$.
=--

To deduce the previous theorem from this one, it suffices to observe that if $S\subset Top$ is closed under open subspaces and their pullbacks and equipped with the open-cover coverage, then every subobject of $y X\in Sh(S)$, for any $X\in S$, is uniquely representable by an open subset of $X$.

+--{: .query}
There is some dispute about this, see [here](http://nforum.ncatlab.org/discussion/6289/when-is-the-internal-real-line-the-external-real-line/?Focus=50275#Comment_50275).

Resolution seems to be [here](http://mathoverflow.net/a/186165/381)

=--


## Generalizations

### Cauchy real numbers
It is also possible to define the notion of a [[Cauchy real number]] object and construct one in any $\Pi$-pretopos with an NNO, but as the internal logic in general lacks [[weak countable choice]], these are usually inequivalent.  (There is also potentially a difference between the *classical* Cauchy RNO and the *modulated* Cauchy RNO; see definitions at [[Cauchy real number]], to be interpreted in the [[stack semantics]].) 


### Classical Dedekind real numbers
In any [[extensive category|finitely extensive]] [[cartesian closed category]], one could define an object that roughly behaves like the Dedekind real numbers in classical mathematics. Instead of using [[subobjects]] of $\mathbb{Q}$ in defining a cut, one instead uses [[decidable object|decidable subobjects]] of $\mathbb{Q}$, or functions $L, U: \mathbb{Q} \rightarrow 1\coprod 1$ to define decidable cuts, and constructs the classical Dedekind real numbers as pairs of decidable cuts. The classical and constructive Dedekind real numbers are usually inequivalent, the classical Dedekind real numbers being equivalent to classical [[Cauchy real numbers]] and the constructive Dedekind real numbers being equivalent to generalised Cauchy real numbers

## Related concepts

* [[real number]]

* [[Cauchy real number]]

* [[one-sided real numbers]]

* [[natural number]]

* [[natural numbers object]]

* [[smooth structure on a topos]]


## References

Discussion in [[topos theory]] is in

* [[Peter Johnstone]], section D4.7 of  _[[Sketches of an Elephant]]_

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint New York 2014). (section 6.6. pp.210-23)

* {#MM94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], section VI.8 of _[[Sheaves in Geometry and Logic]]_ .

* [[Eduardo Dubuc]], _Logical Opens and Real Numbers in Topoi_ , JPAA **43** (1986) pp.129-143.

* {#Fourman75} [[Michael Fourman]], _Comparaison des R&#233;els d'un Topos - Structures Lisses sur un Topos El&#233;mentaire_ , Cah. Top. G&#233;om. Diff. Cat. **16** (1975) pp.233-239. ( _Colloque Amiens 1975 proceedings_ ) (p. 18-24 in [NUMDAM](http://www.numdam.org/item?id=CTGDC_1975__16_3_217_0)))

* [[Michael Fourman]], _T$_1$ Spaces over Topological Sites_ , JPAA **27** (1983) pp.223-224.

* [[Michael Fourman]], [[Martin Hyland]], _Sheaf Models for Analysis_ , pp.280-301 in Fourman, Mulvey, Scott (eds.), _Applications of Sheaves_ , LNM **753** Springer Heidelberg 1979. ([draft](https://www.dpmms.cam.ac.uk/~martin/Research/Oldpapers/analysis79.pdf), 6.64 MB)

* [[André Joyal]], [[Gonzalo E. Reyes]], _Separably Real Closed Local Rings_ , JPAA **43** (1986) pp.271&#8211;279.

* [[Ieke Moerdijk]], [[Gonzalo E. Reyes]], _Smooth Spaces versus Continuous Spaces in Models of Synthetic Differential Geometry_ , JPAA **32** (1984) pp.143-176.

* J. Z. Reichman, _Semicontinuous Real Numbers in a Topos_ , JPAA **28** (1983) pp.81-91.

* L. Stout, _Unpleasant Properties of the Reals in a Topos_ , Cah. Top. G&#233;om. Diff. Cat. **16** (1975) pp.320-322. ([Colloque Amiens 1975 proceedings](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1975__16_3/CTGDC_1975__16_3_217_0/CTGDC_1975__16_3_217_0.pdf),6.81 MB)

* L. N. Stout, _Topological Properties of the Real Numbers Object in a Topos_ , Cah. Top. G&#233;om. Diff. Cat. **17** no.3 (1976) pp.295-326. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1976__17_3/CTGDC_1976__17_3_295_0/CTGDC_1976__17_3_295_0.pdf))

Discussion in [[homotopy type theory]] is in

* [[Univalent Foundations Project]], section 11 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

[[!redirects real numbers object]]
[[!redirects real numbers objects]]
[[!redirects real number object]]
[[!redirects real number objects]]
[[!redirects real-numbers object]]
[[!redirects real-numbers objects]]
[[!redirects real-number object]]
[[!redirects real-number objects]]

[[!redirects real numbers object in a topos]]
[[!redirects real numbers objects in a topos]]
[[!redirects real numbers objects in toposes]]
[[!redirects real numbers objects in topoi]]
[[!redirects real number object in a topos]]
[[!redirects real number objects in a topos]]
[[!redirects real number objects in toposes]]
[[!redirects real number objects in topoi]]
[[!redirects real-numbers object in a topos]]
[[!redirects real-numbers objects in a topos]]
[[!redirects real-numbers objects in toposes]]
[[!redirects real-numbers objects in topoi]]
[[!redirects real-number object in a topos]]
[[!redirects real-number objects in a topos]]
[[!redirects real-number objects in toposes]]
[[!redirects real-number objects in topoi]]

[[!redirects Dedekind real numbers object]]
[[!redirects Dedekind real numbers objects]]
[[!redirects Dedekind real number object]]
[[!redirects Dedekind real number objects]]
[[!redirects Dedekind real-numbers object]]
[[!redirects Dedekind real-numbers objects]]
[[!redirects Dedekind real-number object]]
[[!redirects Dedekind real-number objects]]

[[!redirects Cauchy real numbers object]]
[[!redirects Cauchy real numbers objects]]
[[!redirects Cauchy real number object]]
[[!redirects Cauchy real number objects]]
[[!redirects Cauchy real-numbers object]]
[[!redirects Cauchy real-numbers objects]]
[[!redirects Cauchy real-number object]]
[[!redirects Cauchy real-number objects]]
