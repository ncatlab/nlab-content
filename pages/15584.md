+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects graphic monoid]]
[[!redirects graphics]]
[[!redirects unital left regular band]]
[[!redirects left regular band monoid]]

##Idea

A simple class of [[monoids]] and [[categories]] that permit an effective graphic display via their [[presheaf]] categories.

Graphic monoids arise in the study of [[arrangement of hyperplanes|hyperplane arrangements]] and are often called **left regular band monoids** in this context.

## Definition

A monoid $M$ is called _graphic_ if all $x,y\in M$ satisfy the so called _graphic identity_ $x y x=x y$ . A category $\mathcal{G}$ is called _graphic_ if the endomorphism monoid $End(x)$ is a graphic monoid for each object $x$.

### Remark

The terminology originates with Lawvere ([1989b](#Law89b)) where graphic monoids and categories $\mathcal{G}$ are demanded to be _finite_. This restriction is supported by the fact that finitely generated graphic monoids are necessarily finite ([see below](#fin_gen)).

_Graphic toposes_ are defined then as $FinSet^{\mathcal{G}^{op}}$ resulting in  presheaf categories of finite graph-like 'displays' that come with a well-behaved lattice of subtoposes permitting the kind of 'Hegelian analysis' that were a primary concern for [[Lawvere]] in ([Law89b](#Law89b), [Law91](#Law91), [Law02](#Law02)).

In particular, the graphic monoid $\Delta_1$ in the [example](#ex) and the eight-element [[Hegelian taco]] monoid of (Lawvere [1989b](#Law89b)) express diagrammatically configurations of [[level|essential subtoposes]] occuring in Lawvere's mathematical rendering of basic concepts of Hegel's dialectic logic.[^hegel]

[^hegel]: For more on Lawvere's approach to Hegelian dialectics see [[Aufhebung]], [[adjoint cylinder]], or [[Science of Logic]].

This bears some resemblance to the other context, namely hyperplane arrangements, in which such monoids mainly arise.

In the literature that approaches graphic monoids as special class of semigroups, they are called **unital left regular bands** or _left regular band monoids_ (cf. Brown ([2000](#brown00)), Aguiar-Mahajan ([2006](#AgMah06)), Margolis-Saliola-Steinberg ([2015](#MSS15))).

##Example{#ex}

The principal example of a graphic category is $\Delta_1$ the three element monoid $\{\delta_1,\delta_2,1\}$ with $\delta_i\delta_j=\delta_i$. The presheaf topos $Set^{\Delta_1^{op}}$ is the topos of [[reflexive graphs]].

To see this, recall that a _reflexive graph_ consists of a set of vertices $V$, a set of edges $E$, source and target maps $s, t : E \to V$, and a map $i : V \to E$ assigning to each vertex an 'identity edge' from that vertex to itself, so that $s(i(v)) = t(i(v)) = v$.  

We can describe a reflexive graph without ever mentioning its vertices by using the identity edge $i(v)$ as a stand-in for $v$.  To do this, we 
define operations $\delta_1, \delta_2 : E \to E$ by 

$$  \delta_1(e) = i(s(e)), \qquad \delta_2(e) = i(t(e)) $$

and note that

$$ \delta_1(\delta_1(e)) = \delta_2(\delta_1(e)) = \delta_1(e) $$

$$ \delta_1(\delta_2(e)) = \delta_2(\delta_2(e)) = \delta_2(e) $$

Thus, the reflexive graph determines a functor $F : \Delta_1^{op} \to \Set$, where we think of the monoid $\Delta_1$ as a one-object category.  In other words, it gives a presheaf on $\Delta_1$.  Conversely, any presheaf on $\Delta_1$ determines a reflexive graph.

The more familiar two-sorted 'signature' for reflexive graphs can be obtained from the [[Cauchy completion]] $\overline\Delta_1$ by identifying the isomorphic descendents of $\delta_1,\delta_2$: the resulting $\tilde\Delta_1$ has two objects and is basically an augmentation with reflexivity data of the familiar diagram $V\rightrightarrows E$ that underlies the topos of ("irreflexive") directed graphs, or [[quiver|quivers]]. All three of $\Delta_1,\overline\Delta_1,\tilde\Delta_1$ are graphic categories and the resulting presheaf toposes are, of course, equivalent.

##Properties

* Lawvere calls the graphic identity _'the least common generalization of constant (x=c) and identity (x=1)_' ([1989b](#Law89b), p.53). By a _constant_ $c$ is meant here a $c\in M$ such that $c y=c$ for all $y\in M$. In the context of monoids arising from hyperplane arrangements constants are also called '_chambers_' (cf. [Aguiar-Mahajan 2006](#AgMah06)).

* In a graphic monoid every element is [[idempotent]] as can be directly seen from the graphic identity with $y=1$.

* It follows that a commutative graphic monoid is the same as a [[semilattice]], or equivalently, a commutative monoid where every element is idempotent.

* More generally, one can define a partial order on $M$ by $x\leq y$ iff $x y=y$ ('$x$ is a face of $y$'). In fact, the graphic identity is precisely the condition needed for the anti-symmetry of this relation on monoids whose elements are all idempotent - the reflexivity being a direct consequence of the idempotency.[^semigroups]

[^semigroups]: Semigroup theorists typically order a graphic monoid by $x\leq y$ if $y x=x$ because this is equivalent to $x M\subseteq y M$.

* The _free graphic monoid_ on a set $X$ is the set of totally ordered finite subsets of $X$, where the product of finite subsets $S$ and $T$ is the union $S \cup T$ ordered in such a way that the inclusion $S \hookrightarrow S\cup T$ is order-preserving, the inclusion $T \hookrightarrow S\cup T$ is order-preserving for all elements of $T$ not in $S$, and all the elements of $T$ not in $S$ are greater than all elements of $S$.  This is easy to understand from an example.  Consider the free graphic monoid on $X = \{a,b\}$.  This contains:

  1 (corresponding to the empty subset of $X$), 

  $a$ (corresponding to the subset $\{a\}$), 

  $b$ (corresponding to $\{b\}$), 

  $a b$ (corresponding to $\{a,b\}$ ordered so that $a \lt b$),

  $b a$ (corresponding to $\{a,b\}$ ordered so that $b \lt a$),

  and nothing else, since for example $a b b = a b$ and $b a b = b a$ (since the union of ordered subsets $\{a,b\} \cup \{b\} = \{a, b\}$ inherits the same ordering that $\{a,b\}$ had).

* {#fin_gen}In particular, for a finite set of generators the free graphic monoid is finite and consists of all words without repetitions of which there are exactly $n!\sum_{i=0}^n \frac{1}{i!}$ over an alphabet with $n$ letters.[^schuetz]

[^schuetz]: The finiteness was basically already observed in Sch&#252;tzenberger ([1947](#Sch&#252;tz47)). See also Lawvere ([1989b](#Law89b)).

* The variety (in the sense of universal algebra) of graphic monoids is generated by $\Delta_1$ (cf. Lawvere ([1991](#Law91))).

### Graphic monoids as shelves

There is a relation between graphic monoids and [[shelf|shelves]]:


+-- {: .num_prop #GraphicsAsShelves}
###### Theorem

A graphic monoid is the same as a _unital [[left shelf]]_, meaning a set equipped with a binary operation that obeys the left self-distributive law

$$  a (b c) = (a b)(a c) $$

and has an element $1$ serving as a left and right unit:

$$  1 a = a = a 1$$

=--

+-- {: .proof}
###### Proof

First start with a unital left shelf.  Note that the graphic identity
holds:

   $$ a  b = a (b 1) = (a b) (a 1) = (a  b)  a $$

   and also

   $$ a  b = a  (1  b) = (a  1)  (a  b) = a  (a  b) $$

   Using these and self-distributivity we can deduce the associative law as follows:

   $$\begin{aligned}
a  (b  c) &= (a  b)  (a  c) \\
&= ((a  b)  a)  ((a  b)  c) \\
&= (a  b)  ((a  b)  c) \\
&= (a  b)  c
\end{aligned}$$

   So, we have a graphic monoid.

   Conversely, suppose we start with a graphic monoid.  Then we can prove the left self-distributive law as follows:

   $$ a (b c) = (a b) c = (a b a) c = (a b)(a c)  $$

=--

Note in particular that, somewhat surprisingly, the **associativity** in a unital left shelf comes for free! For more background see the comments on:

   * [The origin of the word "quandle"](https://golem.ph.utexas.edu/category/2015/05/the_origin_of_the_word_quandle.html#c049149), $n$-Category Caf&#233;.


## Related Pages

* [[graphic topos]]

* [[Hegelian taco]]

* [[shelf]]

* [[band]]

* [[rectangular band]]

* [[Aufhebung]]

* [[graph]]

* [[band]]

## References

* {#AgMah06}M. Aguiar, S. Mahajan, _Coxeter Groups and Hopf Algebras_ , AMS Providence 2006. ([draft](http://www.math.cornell.edu/~maguiar/monograph.pdf))

* {#brown00}K. S. Brown, _Semigroups, Semirings, and Markov Chains_ , J. Theor. Prob. **13** no.3 (2000) pp.871-938. 

* R. Guitart, _Autocategories: II. Autographic algebras_ , Cah. Top. Géom. Diff. Cat. **LV** (2014) pp.151-160.  

* N. Kimura, _The structure of idempotent semigroups I_ , Pacific
Journal of Mathematics **8** no.2 (1958) pp.257-275. ([pdf](http://msp.org/pjm/1958/8-2/pjm-v8-n2-p07-p.pdf))

* F. Klein-Barmen, _&#220;ber eine weitere Verallgemeinerung des Verbandsbegriffs_ , Math. Z. **46** (1940) pp.472-480.([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN00237921X))

* [[F. W. Lawvere]], _Qualitative distinctions between some toposes of generalized graphs_, Contemp. Math. **92** (1989) pp. 261-299.

* {#Law89b} [[F. W. Lawvere]], _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_  Proceedings of the first international conference on algebraic methodology and software technology University of Iowa, May 22-24 1989, Iowa City, pp. 51-74. 

* {#Law91} [[F. W. Lawvere]], _More on graphic toposes_, Cah. Top. G&#233;om. Diff. Cat. **XXXII** no. 1 (1991) pp.5-10. ([pdf](http://archive.numdam.org/article/CTGDC_1991__32_1_5_0.pdf)) 

* {#Law02} [[F. W. Lawvere]], _Linearization of graphic toposes via Coxeter groups_, JPAA **168** (2002) pp. 425-436. ([pdf](http://www.sciencedirect.com/science/article/pii/S0022404901001074/pdfft?md5=a4ca9bc67df6ae63ddf53c559bd71315&pid=1-s2.0-S0022404901001074-main.pdf)) 

* {#MSS15} S. Margolis, F. Saliola, B. Steinberg, _Cell Complexes, Poset Topology and the Representation Theory of Algebras Arising in
Algebraic Combinatorics and Discrete
Geometry_ , arXiv:1508.05446 (2015). ([abstract](http://arxiv.org/abs/1508.05446v1))

* M.-P. Sch&#252;tzenberger, _Sur certains treillis gauches_, C. R. Acad. Sci. Paris **225** (1947) pp.277&#8211;278. ([pdf](http://igm.univ-mlv.fr/~berstel/Mps/Travaux/A/1947TreillisGauchesCras.pdf)) {#Sch&#252;tz47}