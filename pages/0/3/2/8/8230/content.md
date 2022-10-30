
> This is about a notion in _[[order theory]]/[[logic]]_. For an unrelated notion of a similar name in [[group theory]]/[[quadratic form]]-theory see at _[[modular integral lattice]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents 
* table of contents
{: toc}

## Idea 

A _modular lattice_ is a lattice where "opposite sides" of a "diamond" formed by four points $x \wedge y$, $x$, $y$, $x \vee y$ are "congruent". 

## Definition 

A modular lattice is a [[lattice]] which satisfies a modular law, which we introduce after a few preliminaries. 

In any lattice $L$, given two elements $x, y \in L$ with $x \leq y$, let $[x, y]$ denote the [[interval]] $\{z \colon x \leq z \leq y\}$. Then, given any two elements $a, b \in L$, there is an [[adjunction|adjoint pair]]  

$$a \vee (-) \colon [a \wedge b, b] \stackrel{\leftarrow}{\to} [a, a \vee b] \colon (-) \wedge b$$ 

where $a \vee (-)$ is left adjoint to $(-) \wedge b$. Indeed, for any $w \in [a \wedge b, b]$, we have a [[adjunction|unit]] 

$$w \leq (a \vee w) \wedge b,$$ 

whereas for any $z \in [a, a \vee b]$, we have dually a [[adjunction|counit]] 

$$a \vee (z \wedge b) \leq z.$$ 

+-- {: .num_defn}
###### Definition 
A lattice $L$ is **modular** if for any $a, b \in L$, the adjoint pair 

$$a \vee (-) \dashv (-) \wedge b \colon [a, a \vee b] \to [a \wedge b, b]$$ 

is an [[adjoint equivalence]]. 
=-- 

This is perhaps the most memorable definition for a category theorist: it is a precise expression of the slogan given in the Idea section. 

It is immediate that the concept of modular lattice is **[[duality|self-dual]]**, i.e., if $L$ is modular, then so is $L^{op}$. 

## Alternative formulations 

In the lattice-theoretic literature, modularity is usually formulated somewhat differently. Here are three alternative conditions on a lattice, all equivalent to that of Definition 1. 

1. The **modular law** is the universal [[Horn theory|Horn sentence]] 
$$a \leq b \vdash (a \vee z) \wedge b = a \vee (z \wedge b).$$

1. The **modular identity** is the universal equation 
$$(a \vee z) \wedge (a \vee b) = a \vee (z \wedge (a \vee b))$$ 

1. "**Freyd's modular law**" (for lack of  better term; see [[allegory]]) is the universal inequality 
$$(a \vee z) \wedge b \leq a \vee (z \wedge (a \vee b)).$$ 

### Proofs of equivalence 

#### Derivation of modular identity 

To see that the modular identity follows from Definition 1, observe that for any $z \in L$ we have 

$$a \leq (a \vee z) \wedge (a \vee b) \leq a \vee b$$ 

Let $w = (a \vee z) \wedge (a \vee b)$. Under $(-) \wedge b \colon [a, a \vee b] \to [a \wedge b, b]$, this element $w$ is sent to 

$$(a \vee z) \wedge (a \vee b) \wedge b = (a \vee z) \wedge b.$$ 

Under Definition 1, this last element is sent back to $w$ by $a \vee (-)$. Therefore we have  

$$(a \vee z) \wedge (a \vee b) = w = a \vee ((a \vee z) \wedge b)$$

and since this is true for all $a, b, z$, we can interchange $z$ and $b$ and rearrange by commutativity to get 

$$(a \vee z) \wedge (a \wedge b) = a \vee (z \wedge (a \vee b))$$ 

which is the modular identity. 

#### Modular law $\Leftrightarrow$ modular identity 

To get the modular law from the modular identity, just use the fact that the hypothesis $a \leq b$ is equivalent to $a \vee b = b$, and use this to substitute $b$ for $a \vee b$ in the modular identity. Conversely, from the tautology $a \leq a \vee b$, we can instantiate the modular law to derive the modular identity. 

#### Freyd's modular law $\Leftrightarrow$ modular identity 

From the tautology $(a \vee z) \wedge b \leq (a \vee z) \wedge (a \vee b)$, it is clear that Freyd's modular law follows from the modular identity. Conversely, by substituting $a \vee b$ for $b$ in Freyd's modular law, we derive the special case 

$$(a \vee z) \wedge (a \vee b) \leq a \vee (z \wedge (a \vee b))$$ 

whereas the opposite inequality 

$$a \vee (z \wedge (a \vee b)) \leq (a \vee z) \wedge (a \vee b)$$ 

holds in any lattice, so the modular identity follows from Freyd's modular law. 

#### Modular identity $\Rightarrow$ definition 1 

Finally, we derive the adjoint equivalence of Definition 1 from the modular identity. One half of the adjoint equivalence states that if $a \leq z \leq a \vee b$, then $z = a \vee (z \wedge b)$; if this holds, then the other half follows because it is the dual statement. If $a \leq z \leq a \vee b$, then 

$$z = (a \vee b) \wedge z = (a \vee b) \wedge (a \vee z)$$ 

just by the laws of a lattice. By the modular identity (again switching $b$ and $z$), the right side equals $a \vee (b \wedge (a \vee z))$. But since $a \vee z = z$, this equals $a \vee (b \wedge z) = a \vee (z \wedge b)$, as was to be shown. 


## Examples 

* Every [[distributive lattice]], e.g., a [[Heyting algebra]], is modular. Indeed, if $a \leq b$ in a distributive lattice, we have 
$$(a \vee z) \wedge b = (a \wedge b) \vee (z \wedge b) = a \vee (z \wedge b)$$ 
which proves the modular law. 

* For any [[Mal'cev variety]] or Mal'cev [[algebraic theory]], the lattice of internal [[equivalence relations]] of an algebra is a modular lattice. The equivalence classes often arise as cosets of kernels; for example, for a [[vector space]] $V$, equivalence relations correspond to subspaces of $V$, and form a modular lattice. Other examples include the lattice of [[normal subgroups]] of a [[group]], the lattice of two-sided [[ideals]] of a [[ring]], etc. 

* In fact, any lattice of commuting equivalence relations on a [[set]] is a modular lattice (being a suballegory of the [[allegory]] of sets, one in which composition provides the join). 

* Every abstract [[projective plane]] gives rise to a modular lattice $L$ whose underlying set is the disjoint union 
$$\{0\} \cup \{1\} \cup \{points\} \cup \{lines\}$$ 
where $0$ is taken as bottom, $1$ as top, the points are atoms, and the lines are coatoms, ordered by the incidence relation. The projective plane need not be Desarguesian. 

* [[Young–Fibonacci lattice]]

## Characterization 

The smallest non-modular lattice has 5 elements and is called the _pentagon_, denoted $N_5$. It can be described as the lattice $\{\bot, a, b, c, \top\}$ where $b \leq c$ and $a$ is incomparable with $b$ and $c$. 

+-- {: .num_theorem} 
###### Theorem 
**(Dedekind)** 
A lattice $L$ is modular if and only if there is no injective function $f \colon N_5 \to L$ that preserves meets and joins. 
=-- 

(Notice we are leaving out the condition of preservation of the top and bottom elements.) The direction $\Rightarrow$ is easy enough: $L$ being modular is incompatible with an injective $f: N_5 \to L$ preserving meets and joins, since we contradict the modular law in $L$ by applying $f$ to $(b \vee a) \wedge c = \top \wedge c = c$ and $b \vee (a \wedge c) = b \vee \bot = b$. 

This is reminiscent of forbidden minor characterizations of certain classes of graphs; see [[graph minor]]. There is a similar "forbidden sublattice" characterization of [[distributive lattices]] -- see this [comment](#Lein) by Tom Leinster at the $n$-Category Caf&#233;. 

## Free modular lattices 

Free modular lattices tend to be complicated. [Dedekind](#Ded) showed that the free modular lattice on 3 elements has 28 elements; its [[Hasse diagram]] can be seen in these [lecture notes](http://www.math.hawaii.edu/~jb/math618/os9uh.pdf) by J.B. Nation (chapter 9, page 100). 

N.B.: this notion of lattice is meant with respect to the signature $(\wedge, \vee)$; if we include top and bottom constants in the signature, then the free modular lattice on three elements has 30 elements. A compelling illustration (in gif form) which exhibits [[triality]] of this lattice is given in this $n$-Category Caf&#233; [post](https://golem.ph.utexas.edu/category/2015/09/the_free_modular_lattice_on_3.html#c049649), as part of a larger discussion which explores the connection with linear representations of the [[quiver]] $D_4$ (the [[Coxeter diagram]] of $SO(8)$). 

For $n \geq 4$, the free modular lattice generated by $n$ elements is infinite and in fact has an undecidable word problem (Freese, Herrmann). 

## See also 

* [[allegory]]

* [[orthomodular lattice]]

* [[distributive lattice]] 

* [[geometric lattice]] 

## References 

* R. Dedekind, &#220;ber die von drei Moduln erzeugte Dualgruppe gemeinsamen Teiler, Math. Annalen 53 (1900), 371&#8211;403, reprinted in Gesammelte mathematische Werke, Vol. 2, pp. 236&#8211;271, Chelsea, New York, 1968. 
{#Ded}

* C. Herrmann, On the word problem for the modular lattice with four free generators, Mathematische Annalen 265 (1983), 513-527. ([Springerlink](http://www.springerlink.com/content/w862594668m2n375/))

* J.B. Nation, Revised Notes on Lattice Theory. Available here: ([web](http://www.math.hawaii.edu/~jb/)) 

* Tom Leinster, Comment on Sol&#232;r's Theorem, December 4, 2010. ([link](http://golem.ph.utexas.edu/category/2010/12/solers_theorem.html#c035900))
{#Lein} 



[[!redirects modular lattices]] 