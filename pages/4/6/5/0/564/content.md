
> This entry is about a concept of duality in general [[category theory]]. For the concept of dualizing objects in a [[closed category]] as used in [[homological algebra]] and [[stable homotopy theory]] see at _[[dualizing object in a closed category]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _dualizing object_ is an object $a$ which can be regarded as being an object of two different [[categories]] $A$ and $B$, such that the concrete [[duality]] which is induced by homming into that object induces dual [[adjunctions]] between $A$ and $B$, schematically:

$$
  T : A^{op} \stackrel{Hom_A(-,a)}{\to} B
$$
$$
  S: B^{op} \stackrel{Hom_B(-,a)}{\to} A
  \,.
$$

Many famous dualities are induced this way, for instance [[Stone duality]] and [[Gelfand-Naimark duality]].

## Remark on terminology

There are various different terms for "dualizing objects". As recalled in [Porst-Tholen 91, p. 112](#PorstTholen91)

* Isbell speaks of _objects keeping summer and winter homes_;

* Lawvere speaks of _objects sitting in two categories_;

* Simmons speaks of _schizophrenic objects_.

It has been convincingly argued by [[Tom Leinster]] (blog comment [here](http://golem.ph.utexas.edu/category/2007/01/more_on_duality.html#c007089)) that the term "schizophrenic" should not be used. [[Todd Trimble]] then suggested the term "ambimorphic object."  Another suggestion was "Janusian object."

## Definition

Let $A$ and $B$ be two categories over $Set$, given by functors 

$$
  U : A \to Set
$$
$$
  V : B \to Set
  \,.
$$ 

(Traditionally in what follows, one assumed $U$ and $V$ to be faithful, i.e., one considered $A$ and $B$ to be categories of sets with [[stuff, structure, property|extra structure]], aka [[concrete categories]], although we won't actually need this. Or, sometimes one sees the hypothesis that $U, V$ are representable, but we won't require this either.) 

The situation described in the Idea section asks us to consider contravariantly [[adjoint functors]] $T: A \to B$, $S: B \to A$ such that $U S: B \to Set$ and $V T: A \to Set$ are representable, i.e., are given by isomorphisms $B(-, \mathbf{b}) \cong U S$ (with representing element $\phi \in U S \mathbf{b}$) and $A(-, \mathbf{a}) \cong V T$ (with representing element $\psi \in V T \mathbf{a}$). Let $\eta: 1_A \to S T$ and $\epsilon: 1_B \to T S$ denote the universal maps of the adjunction (so that if we write $T$ and $S$ in covariant form as $T: A \to B^{op}$ and $S: B^{op} \to A$, we would have $T \dashv S$ with $\eta$ as unit and $\epsilon$ as counit). 

+-- {: .num_prop #sitting} 
###### Proposition 
The representing data $\phi \in U S \mathbf{b}, \psi \in V T \mathbf{a}$ induce a canonical isomorphism $\omega: U \mathbf{a} \stackrel{\sim}{\to} V \mathbf{b}$. It is given by the evident composite 

$$U \mathbf{a} \stackrel{U\eta \mathbf{a}}{\to} U S T \mathbf{a} \stackrel{\sim}{\to} B(T \mathbf{a}, \mathbf{b}) \to Set(V T \mathbf{a}, V \mathbf{b}) \stackrel{eval_\psi}{\to} V \mathbf{b}.$$ 

The inverse is given by a similar composite but switching the roles of $\mathbf{a}$ and $\mathbf{b}$, $\phi$ and $\psi$, $\eta$ and $\epsilon$, $S$ and $T$, and $U$ and $V$. 
=-- 

+-- {: .proof} 
###### Proof 
Letting $x$ be an element of $U \mathbf{a}$, the element $\omega(x) \in V \mathbf{b}$ is by definition $(V g)(\psi)$ where $g: T \mathbf{a} \to \mathbf{b}$ is the unique map (by representability) such that $(U \eta \mathbf{a})(x) = (U S g)(\phi)$. The alleged inverse $\widebar{\omega}: V \mathbf{b} \to U \mathbf{a}$ takes an element $y \in V \mathbf{b}$ to $(U f)(\phi)$, where $f: S \mathbf{b} \to \mathbf{a}$ is the unique map such that $(V T f)(\psi) = (V \epsilon \mathbf{b})(y)$. 

To check these maps are inverse, one may check simply $(\omega \widebar{\omega})(y) = y$ for any $y \in V \mathbf{b}$; the other equation $\widebar{\omega} \omega = id$ follows by symmetry. With notation as above, put $x = \widebar{\omega}(y)$, so $x = (U f)(\phi) \in U \mathbf{a}$. Now we embark on a diagram chase, starting with 

$$\array{
U S \mathbf{b} & \stackrel{U f}{\to} & U \mathbf{a} & \stackrel{U \eta \mathbf{a}}{\to} & U S T \mathbf{a} \\ 
 _\mathllap{\phi} \uparrow & \searrow_\mathrlap{U \eta S \mathbf{b}} & & _\mathllap{U S T f} \nearrow & \uparrow_\mathrlap{\cong} \\ 
1 & & U S T S \mathbf{b} & & B(T \mathbf{a}, \mathbf{b}) \\ 
 & _\mathllap{\xi} \searrow & \uparrow_\mathrlap{\cong} & \nearrow _\mathrlap{B(T f, \mathbf{b})} \\ 
 & & B(T S \mathbf{b}, \mathbf{b}) & & 
}$$ 

where the top and right quadrilaterals commute by naturality, and $\xi: T S \mathbf{b} \to \mathbf{b}$ is the unique arrow making the left quadrilateral commute. In fact $\xi$ is the structure map for a $T S$-algebra structure on $\mathbf{b}$, although for our purposes we will only need the unit axiom for such a structure. Following the perimeter of this diagram, we see 

$$g = (T \mathbf{a} \stackrel{T f}{\to} T S \mathbf{b} \stackrel{\xi}{\to} \mathbf{b})$$ 

is the unique arrow $g: T \mathbf{a} \to \mathbf{b}$ such that $(U S g)(\phi) = (U \eta \mathbf{a})(x)$. Continuing on our way, applying $V$ to $g$ and evaluating at $\psi$, we have only to check that the composite 

$$1 \stackrel{\psi}{\to} V T \mathbf{a} \stackrel{V T f}{\to} V T S \mathbf{b} \stackrel{V \xi}{\to} V \mathbf{b}$$ 

equals $y: 1 \to V \mathbf{b}$. But already we said $(V T f)(\psi) = (V \epsilon \mathbf{b})(y)$, so the last composite is 

$$1 \stackrel{y}{\to} V \mathbf{b} \stackrel{V \epsilon \mathbf{b}}{\to} V T S \mathbf{b} \stackrel{V \xi}{\to} V \mathbf{b}$$ 

and all we need to do now is check the unit equation $\xi \circ (\epsilon \mathbf{b}) = 1_\mathbf{b}$. But this follows from representability of $U S$, applied to the diagram 

$$\array{
U S \mathbf{b} & \stackrel{U \eta S \mathbf{b}}{\to} & U S T S \mathbf{b} & \stackrel{U S \epsilon \mathbf{b}}{\to} & U S \mathbf{b} \\ 
 _\mathllap{\phi} \uparrow & & \uparrow_\mathrlap{\cong} & & \uparrow_\mathrlap{\cong} \\ 
1 & \underset{\xi}{\to} & B(T S \mathbf{b}, \mathbf{b}) & \underset{B(\epsilon \mathbf{b}, \mathbf{b})}{\to} & B(\mathbf{b}, \mathbf{b}) 
}$$ 

where the top horizontal composite is an identity, according to a triangular equation. 
=-- 


The canonical identification of sets $\omega: U \mathbf{a} = V \mathbf{b}$ means that we have an object "sitting in two categories" (Lawvere), namely an $A$-structure $\mathbf{a}$ on this set and a $B$-structure $\mathbf{b}$ on the same set, with $T: A^{op} \to B$ providing a lift of $A(-, \mathbf{a}): A^{op} \to Set$ through $V: B \to Set$, and $S: B^{op} \to A$ lifting $B(-, \mathbf{b}): B^{op} \to Set$ through $U: A \to Set$. 

Given functors $U: A \to Set$, $V: B \to Set$, we define $Adj_{rep}(U, V)$ to be the category whose objects are contravariantly adjoint pairs $(S: B \to A, T: A \to B)$ such that $U S$ and $V T$ are representable. Morphisms $(S, T) \to (S', T')$ are pairs of natural transformations $\alpha: S \to S'$, $\beta: T \to T'$ such that the diagrams 

$$\array{
1_A & \stackrel{\eta'}{\to} & S' T' & & & & & & T S' & \stackrel{T \alpha}{\to} & T S \\ 
 _\mathllap{\eta} \downarrow & & \downarrow_\mathrlap{S' \beta} & & & & & & _\mathllap{\beta S'} \downarrow & & \downarrow_\mathrlap{\epsilon} \\ 
S T & \underset{\alpha T}{\to} & S' T & & & & & & T' S' & \underset{\epsilon'}{\to} & 1_B 
}$$ 

commute. We define $2\text{-}Pull(U, V)$ to be the [[2-pullback]] of $U$ and $V$ in $Cat$ (i.e., the bi-iso-comma-object). In conjunction with the [[Yoneda lemma]], the preceding proposition can be read as giving the construction of a functor $\Phi: Adj_{rep}(U, V) \to 2\text{-}Pull(U, V)$. 

Here then is one key definition. 

+-- {: .num_defn #ambi} 
###### Definition 
Given $U: A \to Set$, $V: B \to Set$, a $(U, V)$-**dualizing object** (or $(U, V)$-*ambimorphic object*) is a triple $(\mathbf{a}, \mathbf{b}, \omega: U \mathbf{a} \stackrel{\sim}{\to} V \mathbf{b})$ in the essential image of $\Phi$. 
=-- 

### Naturally represented adjunctions 

Definition \ref{ambi} is reasonably general and is one of several notions of "schizophrenic object" given in [Dimov-Tholen93](#DT93). A somewhat tighter notion, also considered in [Dimov-Tholen 89](#DT89) and [Porst-Tholen 91](#PorstTholen91) and which covers many cases that arise in practice, involves initial lifts through the functors $U$, $V$. 

Again, suppose given contravariant adjoint functors $S, T$ with $U S$ and $V T$ representable as above. We have maps 

$$\gamma \coloneqq (U \stackrel{U \eta}{\to} U S T \cong B(T-, \mathbf{b})), \qquad \delta \coloneqq (V \stackrel{V \epsilon}{\to} V T S \cong A(U-, \mathbf{a}))$$ 

so that for each object $a$ of $A$ and $x \in U a$, we have a corresponding map $(\gamma a)(x): T a \to \mathbf{b}$ (playing the role of "$g$" in the proof of Proposition \ref{sitting}), and similarly for each object $b$ of $B$ and $y \in V b$, we have a map $(\delta b)(y): S b \to \mathbf{a}$ (playing the role of "$f$" in Proposition \ref{sitting}). 

+-- {: .num_defn} 
###### Definition 
The adjunction between $S$ and $T$ is *naturally* represented if the family 
$\{(\gamma a)(x): T a \to \mathbf{b}\}_{x \in U a}$ is $V$-[[topological functor|initial]] for each $a \in Ob(A)$, and the family $\{(\delta b)(y): S b \to \mathbf{a}\}_{y \in V b}$ is $U$-initial for each $b \in Ob(B)$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
The restriction of $\Phi: Adj_{rep}(U, V) \to 2\text{-}Pull(U, V)$ to the full subcategory whose objects are naturally represented adjoint pairs is full and faithful. 
=-- 

See [Dimov-Tholen](#DT93), Proposition 2.3, where the proof is sketched. Thus naturally represented adjoint pairs could be equivalently described as certain types of ambimorphic objects. We now describe these. 

Let us denote the action of $A$ on the module $U: A \to Set$, with components $A(a, a') \times U a \to U a'$, by the notation $(f, x) \mapsto f \cdot_U x$. Thus each $x \in U a$ induces a map $- \cdot_U x: A(a, \mathbf{a}) \to U \mathbf{a}$. Similarly, each $y \in V b$ induces a map $- \cdot_V y: B(b, \mathbf{b}) \to V \mathbf{b}$. 

+-- {: .num_defn #natural} 
###### Definition 
A $(U, V)$-ambimorphic object $(\mathbf{a}, \mathbf{b}, \omega: U \mathbf{a} \stackrel{\sim}{\to} V \mathbf{b})$ is *natural* if for every $a \in Ob(A)$, the $V$-structured source diagram 

$$\{A(a, \mathbf{a}) \stackrel{- \cdot_U x}{\to} U \mathbf{a} \stackrel{\omega}{\to} V \mathbf{b}\}_{x \in U a}$$ 

admits an [[topological concrete category|initial lift]] targeted at $\mathbf{b}$ (so a suitable diagram of the form $\gamma_x: T a \to \mathbf{b}$ indexed over $x \in U a$, for some object $T a$ of $B$), and for every $b \in Ob(B)$, the $U$-structured source diagram 

$$\{B(b, \mathbf{b}) \stackrel{- \cdot_V y}{\to} V \mathbf{b} \stackrel{\omega^{-1}}{\to} U \mathbf{a}\}_{y \in V b}$$ 

admits an initial lift (a diagram of type $\delta_y: S b \to \mathbf{a}$), targeted at $\mathbf{a}$. 
=-- 

Thus the category of naturally represented adjoint pairs relative to $(U, V)$ is equivalent to the category of natural $(U, V)$-dualizing objects. This is the notion of "schizophrenic object" given by [Porst-Tholen 91](#PorstTholen91); a reasonably detailed proof of the equivalence with naturally represented adjoint pairs is given in their Theorem 1.7. 

## Examples

One easy general example of the notion given in Definition \ref{ambi} is where $C$ is a [[symmetric monoidal category|symmetric]] [[monoidal closed category]] and $d$ is an object therein. Here we may take $U = V = C(I, -): C \to Set$ where $I$ is the monoidal unit, and the contravariant representable functor $C(-, d): C \to Set$ lifts to a contravariant enriched hom $[-, d]: C \to C$; the symmetry isomorphism can be exploited to show how $[-, d]$ is adjoint to itself. See [here](http://ncatlab.org/nlab/show/duality#concrete_dualities) for more. 

Further examples appear at 

* [[Stone duality]]

* [[Gelfand duality]] (see at _[[center of an adjunction]]_ the section _[Examples - Gelfand duality](fixed+point+of+an+adjunction#GelfandDuality)_)

* [[star-autonomous category]]

* [[Chu construction]]

* [[rational homotopy theory]]

* [[dualizing complex]], [[dualizing module]]

## References

* {#DT89} G. D. Dimov, [[Walter Tholen]], _A Characterization of Representable Dualities,_ In: _Categorical Topology and its Relation to Analysis, Algebra and Combinatorics,_ Prague, Czechoslovakia 22-27 August 1988,  J. Adamek and S. MacLane (eds.), World Scientific, Singapore, New Jersey, London, Hong Kong, 1989, pp. 336-357. 
  

* {#DT93} G. D. Dimov, [[Walter Tholen]], _Groups of Dualities,_ Trans. Amer. Math. Soc.,
336 (2), 901-913, 1993. ([pdf](http://www.ams.org/journals/tran/1993-336-02/S0002-9947-1993-1100693-0/S0002-9947-1993-1100693-0.pdf)) 
  
* {#PorstTholen91} [[Hans-E. Porst]], [[Walter Tholen]], _Concrete Dualities_ in H. Herrlich, [[Hans-E. Porst]] (eds.) _Category Theory at Work_, Heldermann Verlag 1991 ([pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf)) 

* [[Michael Barr]], John F. Kennison, R. Raphael, _Isbell Duality_ ([pdf](http://www.tac.mta.ca/tac/volumes/20/15/20-15.pdf))


[[!redirects dualizing objects]]
[[!redirects ambimorphic object]]
[[!redirects ambimorphic objects]]
[[!redirects schizophrenic object]]
[[!redirects schizophrenic objects]]
