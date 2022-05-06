[[!redirects decidable objects]]
[[!redirects separable object]]
[[!redirects separable objects]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

##Idea

The concept of _decidable object_ is the generalization to [[category theory]] of the concept of a [[decidable set]] from [[computability theory]]. 

This corresponds to the algebraic and topological concepts _[[unramified morphism|unramified]]_, respectively _[[separable topological space|separable]]_ object, as pointed out by [[William Lawvere]].

## Definition

An [[object]] $X$ of a [[coherent category]] $\mathcal{C}$ is called _decidable_ if its [[equality relation]] (i.e. its [[diagonal morphism]])

$$
  \Delta_X
  \;\colon\;
  X  
    \longrightarrow 
  X \times X
$$

is [[complement|complemented]], as a [[subobject]] of the [[Cartesian product]] $X \times X$. 

A [[morphism]] $f \colon A \to B$ is called _decidable_ if it is a decidable object in the [[slice category]] $\mathcal{C}/B$.

## Remarks

* For an object $X$ this means that in the [[internal logic]] of the category, it is true that "for any $x,y\in X$ , either $x=y$ or $x\neq y$".

* In [[constructive mathematics]], where [[Set]] is not assumed Boolean, one says that a set $X$ has _[[decidable equality]]_ if it is a decidable object of $\Set$.

* A _decidable subobject_ simply means a [[complemented subobject]].  Again, in constructive mathematics, a decidable subobject in $\Set$ is called a _[[decidable subset]]_.

* An object $X$ in a topos $\mathcal{E}$ is called _anti-decidable_ if $\neg\neg (x=y)$ in the internal language of $\mathcal{E}$ holds for all $x,y\in X$. A formula $\varphi$ is called _almost decidable_ iff $\neg\varphi\vee\neg\neg\varphi$ holds and an object $X$ is called _almost decidable_ if $x=y$ is almost decidable for $x\in X$.


## Examples

* An [[initial object]] and [[terminal object]] are always decidable, and so is every [[natural numbers object]] $N$ in a topos

* A [[subobject]] of a decidable object is decidable.

* Decidable [[morphisms]] $f:A\to B$ in the [[opposite category|opposite]] of the [[category of commutative rings]] $CommRing^{op}$ are precisely the [[separable algebra|separable]] $B$-algebras $A$.

* Of course, in a [[Boolean category]], every object is decidable. Conversely in a [[topos]] $\mathcal{E}$, or more generally a coherent category with a [[subobject classifier]], every object is decidable precisely if $\mathcal{E}$ is Boolean.


## Related concepts

* [[theory of decidable objects]]

* [[locally decidable topos]]

* [[finite object]]

* [[separable algebra]]

## References

* B. P. Chisala, M.-M. Mawanda, _Counting Measure for Kuratowski Finite Parts and Decidability_ , Cah.Top.G&#233;om.Diff.Cat. **XXXII** 4 (1991) pp.345-353. ([pdf](archive.numdam.org/article/CTGDC_1991__32_4_345_0.pdf))

* [[Aurelio Carboni|A. Carboni]], [[G. Janelidze]], _Decidable (=separable) objects and morphisms in lextensive categories_ , JPAA **110** (1996) pp.219-240.

* [[Peter Johnstone]], _Sketches of an Elephant_ vols. I,II, Oxford UP 2002.

