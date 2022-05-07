
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### Lift of morphisms

A **lift** of a morphism $f: Y\to B$ along an [[epimorphism]] (or more general map) $p:X\to B$ is a morphism $\tilde{f}: Y\to X$ such that $f = p\circ\tilde{f}$.

The dual problem is the [[extension]] of a morphism $f: A\to Y$ along a monomorphism $i: A\hookrightarrow X$, which is a morphism $\tilde{f}:X\to Y$ such that $\tilde{f}\circ i = f$. One sometimes extends along more general morphisms than monomorphisms. 

## Idea


The '''lifting property''' is a property of a pair of [[morphism (category theory)|morphism]]s in a [[category (mathematics)|category]]. It is used in [[homotopy theory]] within [[algebraic topology]] to define properties of morphisms starting from an explicitly given class of morphisms. It appears in a prominent way in the theory of [[model categories]], an axiomatic framework for [[homotopy theory]] introduced by [[Daniel Quillen]]. It is also used in the definition of a [[factorization system]], and of a [[weak factorization system]], notions related to but less restrictive than the notion of a model category. A number of elementary notions may also be expressed using the lifting property starting from a list of (counter)examples.

==Formal definition==
A morphism ''i'' in a category has the ''left lifting property'' with respect to a morphism ''p'', and ''p'' also has the ''right lifting property'' with respect to ''i'', sometimes denoted <math>i\perp p</math> or <math>i\downarrow p</math>, iff the following implication holds for each morphism ''f'' and ''g'' in the category:

* if the outer square of the following diagram commutes, then there exists ''h'' completing the diagram, i.e. for each <math>f:A\to X</math> and <math>g:B\to Y</math> such that <math>p\circ f = g \circ i</math> there exists <math>h:B\to X</math> such that <math>h\circ i = f</math> and <math>p\circ h = g</math>.


$$
  \array{
    a &\stackrel{u}{\to}& c
    \\
    \downarrow^f
    &{}^{\exists \gamma}\nearrow&
    \downarrow^g
    \\
   b &\stackrel{v}{\to}& d    
  }
$$





This is sometimes also known as the morphism ''i'' being ''weakly orthogonal to'' the morphism ''p''; however, this can also refer to
the stronger property that whenever ''f'' and ''g'' are as above, the diagonal morphism ''h'' exists and is also required to be unique.

For a class ''C'' of morphisms in a category, its ''left weak orthogonal'' or its ''left Quillen negation''
 <math>C^{\perp \ell}</math> or <math>C^\perp</math> with respect to the lifting property, respectively its ''right weak orthogonal'' and its ''right Quillen negation'' 
<math>C^{\perp r}</math> or <math>{}^\perp C</math>, is the class of all morphisms which have the left, respectively right, lifting property with respect to each morphism in the class ''C''. In notation,

:<math>\begin{align}
C^{\perp\ell} &:= \{ i \mid \forall p\in C, i\perp p\} \\
C^{\perp r} &:= \{ p \mid \forall i\in C, i\perp p\}
\end{align}</math>

Taking the orthogonal of a class ''C'' is a simple way to define a class of morphisms excluding [[Isomorphism#Category_theoretic_view|non-isomorphisms]] from ''C'', in a way which is useful in a [[diagram chasing]] computation.

Thus, in the category '''Set''' of [[Set (mathematics)|sets]], the right orthogonal <math>\{\emptyset \to \{*\}\}^{\perp r}</math> of the simplest [[Surjective|non-surjection]] <math>\emptyset\to \{*\},</math> is the class of surjections. The left and right orthogonals of <math>\{x_1,x_2\}\to \{*\},</math> the simplest [[Injective|non-injection]], are both precisely the class of injections, 

:<math>\{\{x_1,x_2\}\to \{*\}\}^{\perp\ell} = \{\{x_1,x_2\}\to \{*\}\}^{\perp r} = \{ f \mid f \text{ is an injection } \}.</math>

It is clear that <math>C^{\perp\ell r} \supset C</math> and <math>C^{\perp r\ell} \supset C</math>. The class <math>C^{\perp r}</math> is always closed under retracts, [[Pullback (category theory)|pullbacks]], (small) [[Product (category theory)|products]] (whenever they exist in the category) and composition of morphisms, and contains all isomorphisms of C. Meanwhile, <math>C^{\perp \ell}</math> is closed under retracts, [[Pushout (category theory)|pushouts]], (small) [[Coproduct (category theory)|coproducts]] and transfinite composition ([[filtered colimit]]s) of morphisms (whenever they exist in the category), and also contains all isomorphisms.

==Examples==
A number of notions can be defined by passing to the left or right orthogonal several times starting from a list of explicit examples, i.e. as <math>C^{\perp\ell}, C^{\perp r}, C^{\perp\ell r}, C^{\perp\ell\ell}</math>, where <math>C</math> is a class consisting of several explicitly given morphisms. A useful intuition is to think that the property of left-lifting against a class ''C'' is a kind of negation
of the property of being in ''C'', and that right-lifting is also a kind of negation. Hence the classes obtained from ''C'' by taking orthogonals an odd number of times, such as <math>C^{\perp\ell}, C^{\perp r}, C^{\perp\ell r\ell}, C^{\perp\ell\ell\ell}</math> etc., represent various kinds of negation of ''C'', so <math>C^{\perp\ell}, C^{\perp r}, C^{\perp\ell r\ell}, C^{\perp\ell\ell\ell}</math> each consists of morphisms which are far from having property <math>C</math>.

===Examples of lifting properties in algebraic topology===
A map <math>f:U\to B</math> has the ''path lifting property'' iff <math>\{0\}\to [0,1] \perp f</math> where <math>\{0\} \to [0,1]</math> is the inclusion of one end point of the closed interval into the interval <math>[0,1]</math>.

A map <math>f:U\to B</math> has the [[homotopy lifting property]] iff <math>X \to X\times [0,1] \perp f</math> where <math>X\to X\times [0,1]</math> is the map <math>x \mapsto (x,0)</math>.

===Examples of lifting properties coming from model categories===
Fibrations and cofibrations.

* Let '''Top''' be the category of [[topological space]]s, and let <math>C_0</math> be the class of maps <math>S^n\to D^{n+1}</math>, [[embedding]]s of the boundary <math>S^n=\partial D^{n+1}</math> of a ball into the ball <math>D^{n+1}</math>. Let <math>WC_0</math> be the class of maps embedding the upper semi-sphere into the disk. <math>WC_0^{\perp\ell}, WC_0^{\perp\ell r}, C_0^{\perp\ell}, C_0^{\perp\ell r}</math> are the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations.<ref>{{cite book | last = Hovey | first = Mark |title = Model Categories | url = https://archive.org/details/arxiv-math9803002 }} Def. 2.4.3, Th.2.4.9</ref>

* Let '''sSet''' be the category of [[simplicial set]]s. Let <math>C_0</math> be the class of boundary inclusions <math>\partial \Delta[n] \to \Delta[n]</math>, and let <math>WC_0</math> be the class of horn inclusions <math>\Lambda^i[n] \to \Delta[n]</math>. Then the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations are, respectively, <math>WC_0^{\perp\ell}, WC_0^{\perp\ell r}, C_0^{\perp\ell}, C_0^{\perp\ell r}</math>.<ref>{{cite book | last = Hovey | first = Mark |title = Model Categories | url = https://archive.org/details/arxiv-math9803002 }} Def. 3.2.1, Th.3.6.5</ref>

* Let '''Ch'''(''R'') be the category of [[chain complex]]es over a [[commutative ring]] ''R''. Let <math>C_0</math> be the class of maps of form
:: <math>\cdots\to 0\to R \to 0 \to 0 \to \cdots \to \cdots \to R \xrightarrow{\operatorname{id}} R \to 0 \to 0 \to \cdots,</math>
: and <math>WC_0</math> be
:: <math>\cdots \to 0\to 0 \to 0 \to 0 \to \cdots \to \cdots \to R \xrightarrow{\operatorname{id}} R \to 0 \to 0 \to \cdots.</math>
:Then <math>WC_0^{\perp\ell}, WC_0^{\perp\ell r}, C_0^{\perp\ell}, C_0^{\perp\ell r}</math> are the classes of fibrations, acyclic cofibrations, acyclic fibrations, and cofibrations.<ref>{{cite book | last = Hovey | first = Mark |title = Model Categories | url = https://archive.org/details/arxiv-math9803002 }} Def. 2.3.3, Th.2.3.11</ref>

===Elementary examples in various categories===
In '''Set''', 

* <math>\{\emptyset\to \{*\}\}^{\perp r}</math> is the class of surjections,

* <math>(\{a,b\}\to \{*\})^{\perp r}=(\{a,b\}\to \{*\})^{\perp\ell}</math> is the class of injections.

In the category ''R''-'''Mod''' of [[Module (mathematics)|modules]] over a commutative ring ''R'',

* <math>\{0\to R\}^{\perp r}, \{R\to 0\}^{\perp r}</math> is the class of surjections, resp. injections,

* A module ''M'' is [[Projective module|projective]], resp. [[Injective module|injective]], iff <math>0\to M</math> is in <math>\{0\to R\}^{\perp\ell r}</math>, resp. <math>M\to 0</math> is in <math>\{R\to 0\}^{\perp rr}</math>.

In the category '''Grp''' of [[Group (mathematics)|groups]], 

* <math>\{\Z \to 0\}^{\perp r}</math>, resp. <math>\{0\to \Z\}^{\perp r}</math>, is the class of injections, resp. surjections (where <math>\Z</math> denotes the infinite [[cyclic group]]),

* A group ''F'' is a [[free group]] iff <math>0\to F</math> is in <math>\{0\to \Z \}^{\perp r\ell},</math>

* A group ''A'' is [[Torsion (algebra)|torsion-free]] iff <math>0\to A</math> is in <math>\{ n \Z\to \Z : n>0 \}^{\perp r},</math>

* A [[subgroup]] ''A'' of ''B'' is [[Pure subgroup|pure]] iff <math>A \to B</math> is in <math>\{ n\Z\to \Z : n>0 \}^{\perp r}.</math>

For a [[finite group]] ''G'', 

* <math>\{0\to {\Z}/p{\Z}\} \perp G\to 1</math> iff the [[Order (group theory)|order]] of ''G'' is prime to ''p'',

* <math>G\to 1 \in (0\to {\Z}/p{\Z})^{\perp rr}</math> iff ''G'' is a [[p-group|''p''-group]],

* ''H'' is nilpotent iff the diagonal map <math>H\to H\times H</math> is in <math>(1\to *)^{\perp\ell r}</math> where <math>(1\to *)</math> denotes the class of maps <math>\{ 1\to G : G \text{ arbitrary}\},</math>

* a finite group ''H'' is [[Soluble group|soluble]] iff <math>1\to H</math> is in <math>\{0\to A : A\text{ abelian}\}^{\perp\ell r}=\{[G,G]\to G : G\text{ arbitrary } \}^{\perp\ell r}.</math>

In the category '''Top''' of topological spaces, let <math>\{0,1\}</math>, resp. <math>\{0\leftrightarrow 1\}</math> denote the [[Discrete space|discrete]], resp. [[Trivial topology|antidiscrete]] space with two points 0 and 1. Let <math>\{0\to 1\}</math> denote the [[Sierpinski space]] of two points where the point 0 is open and the point 1 is closed, and let <math>\{0\}\to \{0\to 1\}, \{1\} \to \{0\to 1\}</math> etc. denote the obvious embeddings.

* a space ''X'' satisfies the separation axiom [[Kolmogorov space|T<sub>0</sub>]] iff <math>X\to \{*\}</math> is in <math>(\{0\leftrightarrow 1\} \to \{*\})^{\perp r},</math>

* a space ''X'' satisfies the separation axiom [[T1 space|T<sub>1</sub>]] iff <math>\emptyset\to X</math> is in <math>( \{0\to 1\}\to \{*\})^{\perp r},</math>

* <math>(\{1\}\to \{0\to 1\})^{\perp\ell}</math> is the class of maps with [[Dense set|dense]] [[Image (mathematics)|image]], 

* <math>(\{0\to 1\}\to \{*\})^{\perp\ell}</math> is the class of maps <math>f:X\to Y</math> such that the [[Topological_space#Definitions|topology]] on ''A'' is the pullback of topology on ''B'', i.e. the topology on ''A'' is the topology with least number of open sets such that the map is [[Continuous_function#Continuous_functions_between_topological_spaces|continuous]],

* <math>(\emptyset\to \{*\})^{\perp r}</math> is the class of surjective maps, 

* <math>(\emptyset\to \{*\})^{\perp r\ell}</math> is the class of maps of form <math>A\to A\cup D</math> where ''D'' is discrete,

* <math>(\emptyset\to \{*\})^{\perp r\ell\ell} = (\{a\}\to \{a,b\})^{\perp\ell}</math> is the class of maps <math>A\to B</math> such that each [[Connected component (topology)|connected component]] of ''B'' intersects <math>\operatorname{Im} A</math>,

* <math>(\{0,1\}\to \{*\})^{\perp r}</math> is the class of injective maps,

* <math>(\{0,1\}\to \{*\})^{\perp\ell}</math> is the class of maps <math>f:X\to Y</math> such that the [[preimage]] of a [[Connected space|connected]] closed open subset of ''Y'' is a connected closed open [[subset]] of ''X'', e.g. ''X'' is connected iff <math>X\to \{*\}</math> is in <math>(\{0,1\} \to \{*\})^{\perp\ell}</math>,

* for a connected space X, each continuous function on ''X'' is bounded iff <math>\emptyset\to X \perp \cup_n (-n,n) \to \R</math> where <math>\cup_n (-n,n) \to \R</math> is the map from the [[disjoint union]] of open intervals <math>(-n,n)</math> into the [[real line]] <math>\mathbb{R},</math>

* a space ''X'' is [[Hausdorff space|Hausdorff]] iff for any injective map <math>\{a,b\}\hookrightarrow X</math>, it holds <math>\{a,b\}\hookrightarrow X \perp \{a\to x \leftarrow b \}\to\{*\}</math> where <math>\{a\leftarrow x\to b \}</math> denotes the three-point space with two open points ''a'' and ''b'', and a closed point ''x'',

* a space ''X'' is [[normal space|perfectly normal]] iff <math>\emptyset\to X \perp [0,1] \to \{0\leftarrow x\to 1\}</math> where the open interval <math>(0,1)</math> goes to&nbsp;''x'', and <math>0</math> maps to the point <math>0</math>, and <math>1</math> maps to the point <math>1</math>, and <math>\{0\leftarrow x\to 1\}</math> denotes the three-point space with two closed points <math>0, 1</math> and one open point ''x''.

In the category of [[metric space]]s with [[uniformly continuous]] maps.

* A space ''X'' is [[Complete metric space|complete]] iff <math>\{1/n\}_{n \in \N} \to \{0\}\cup \{1/n\}_{n \in \N} \perp X\to \{0\}</math> where <math>\{1/n\}_{n \in \N} \to \{0\}\cup \{1/n\}_{n \in \N}</math> is the obvious inclusion between the two subspaces of the real line with induced metric, and <math>\{0\}</math> is the metric space consisting of a single point,

* A subspace <math>i:A\to X</math> is closed iff <math>\{1/n\}_{n \in \N} \to \{0\}\cup \{1/n\}_{n \in \N} \perp A\to X.</math>

==Notes==
{{Reflist}}

==References==
* {{cite book | last = Hovey | first = Mark |title = Model Categories | url = https://archive.org/details/arxiv-math9803002 |date=1999}}






,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,oooooooooooooo




Let $K$ be a [[category]] and write $arr(K)$ for the [[arrow category]] of $K$: the category with arrows (= [[morphisms]]) $a \stackrel{f}{\to} b$ of $K$ as objects and commutative squares $g u=v f$ 

$$
  \array{
    a &\stackrel{u}{\to}& c
    \\
    \downarrow^{\mathrlap{f}}
    &&
    \downarrow^{\mathrlap{g}}
    \\
   b &\stackrel{v}{\to}& d    
  }
$$

as morphisms $(u,v) : f \rightarrow g$. We may also refer to a commutative square $g u=v f$ as a **lifting problem** between $f$ and $g$.

We say a morphism $f$ has the **left lifting property** with respect to a morphism $g$ or equivalently that $g$ has the **right lifting property** with respect to $f$, if for every commutative square $(u,v) :f \rightarrow g$ as above,  there is an arrow $\gamma$ 

$$
  \array{
    a &\stackrel{u}{\to}& c
    \\
    \downarrow^f
    &{}^{\exists \gamma}\nearrow&
    \downarrow^g
    \\
   b &\stackrel{v}{\to}& d    
  }
$$


from the codomain $b$ of $f$ to the domain $c$ of $g$ such that both triangles commute. We call such an arrow $\gamma$ a **lift** or a **solution** to the lifting problem $(u,v)$.

(If this lift is unique, we say that $f$ is **[[orthogonal]]** $f \perp g$ to $g$.)

## Examples

* [[weak factorization system]], [[model category]]

* [covering space lifting properties](covering+space#LiftingProperties)

* [[separation axioms in terms of lifting properties]]

* [Tychonoff theorem -- Proof via lifting properties](Tychonoff+theorem#ProofViaTaimanovTheoremAndLiftingProperties)


## Related concepts

* [[factorization system]]

* [[homotopy lifting property]]

* [[Kan lift]]

* [[Joyal-Tierney calculus]]

* [[lifts and extensions]]


[[!redirects lifts]]

[[!redirects lifting]]
[[!redirects liftings]]

[[!redirects lifting property]]
[[!redirects lifting properties]]

[[!redirects right lifting property]]
[[!redirects left lifting property]]
[[!redirects right lifting properties]]
[[!redirects left lifting properties]]


[[!redirects lifting problem]]
[[!redirects lifting problems]]


