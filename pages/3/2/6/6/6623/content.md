
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


The notion of _well-founded coalgebra_ is due to [[Paul Taylor]] (with antecedents in the work of Gerhard Osius). Our account is largely based on ([Taylor, section 6.3)](#Taylor99)), and on his paper [The General Recursion Theorem](#tTaylor96), although in some cases we work with slightly different hypotheses. 

## Definition

Let $C$ be a [[finitely complete category]], and let $T$ be an [[endofunctor]] on $C$. We will suppose that $T$ is [[taut functor|taut]], i.e., preserves [[pullbacks]] of [[monomorphisms]] (preserves [[limits]] of [[cospans]] in which one of the cospan arrows is [[monomorphism|monic]]).  In particular, this implies that $T$ preserves monos.  A helpful example to keep in mind is the covariant power-set functor $P: Set \to Set$.

+-- {: .un_defn}
######Definition 
Let $\theta: X \to T X$ be a $T$-[[coalgebra for an endofunctor|coalgebra]] structure on $X$. A [[subobject]] $i: U \hookrightarrow X$ in $C$ is $\theta$-**inductive** if in the pullback 

$$\array{
H & \stackrel{j}{\to} & X \\ 
\downarrow & & \downarrow^\mathrlap{\theta} \\
T U & \underset{T i}{\to} & T X
}$$ 

the map $j$ factors through $i$ (note that $j$ is monic since $T$ preserves monos). 

A coalgebra $(X, \theta)$ is **well-founded** if the only inductive subobject of $X$ is $X$ itself. 
=-- 

**Example:** Suppose $X$ is an initial algebra for the endofunctor $T$, with algebra structure map $\alpha: T X \to X$. By Lambek's theorem, $\alpha$ is invertible, so that $X$ carries a coalgebra structure $\theta = \alpha^{-1}: X \to T X$. It is easy to check that an inductive subobject gives a subalgebra $i: U \to X$, but a subalgebra of an initial algebra must be the initial algebra itself. Hence $(X, \theta)$ is well-founded. 

Our goal in this article is to show that one can perform inductive arguments and recursive constructions in the abstract context of well-founded coalgebras. An interesting challenge is to make precise what is meant by a recursive construction of a map $\phi: X \to A$, where the problem is to show how to build $\phi$ from the ground up, as it were. Stages in the recursive construction of a morphism will be _partial_ maps, defined as usual as spans 

$$\array{
 & & D & & \\
 &  ^\mathllap{i} \swarrow & & \searrow^\mathrlap{f} \\ 
A & & & & B
}$$ 

for which the arrow $i$ is _monic_. Composition of partial maps is effected by span composition, for which we need only finite cocompleteness (we do not need $C$ to be a [[regular category]], as we would if we were composing general relations between $A$ and $B$). Notice that since $T$ preserves the pulling back of monos, it carries partial maps to partial maps and also preserves partial map composition. 

We denote a partial map by a dashed arrow 

$$f: A \dashrightarrow B$$ 

(generally without explicitly mentioning the domain $D$ of $f$), or sometimes by a harpoon notation. 

### Connection with initial algebras 

One way of constructing the [[initial algebra of an endofunctor]], $(X, \alpha: T X \to X)$, is by constructing first some [[fixed point]] of $T$, that is, an object $Y$ together with an isomorphism $\xi: Y \cong T Y$. (For example, it might be the terminal coalgebra, whose existence is sometimes easy to establish.) Then, inside $Y$ consider the system of well-founded subcoalgebras of $\xi$. The colimit of this system, assuming it exists, will be the initial algebra. (More theory to develop here.) 

The connection with initial algebras goes a little further. Firstly, an initial $T$-algebra is a *Peano $T$-algebra* in the sense of the following definition: 

+-- {: .num_defn} 
###### Definition 
A $T$-algebra $(X, \alpha: T X \to X)$ is *semi-Peano* if every $T$-subalgebra [[monomorphism|inclusion]] $i: Y \hookrightarrow X$ is an isomorphism, and *Peano* if in addition $\alpha$ is an isomorphism. 
=-- 

If $X$ is initial and $i: Y \to X$ is a subalgebra, then there is a unique algebra map $r: X \to Y$, and $i r = 1_X: X \to X$ by initiality, whence $i r i = i$ and then $r i = 1_Y: Y \to Y$ as $i$ is monic. Hence initial algebras are semi-Peano, and Peano by Lambek's theorem. 

Secondly, a functor $T: E \to E$ induces, for any object $X$ of $E$, a functor between slices $T_\ast: E/X \to E/ T X$, and so if $(X, \theta: X \to T X)$ is a coalgebra, we may form an endofunctor on $E/X$: 

$$E/X \stackrel{T_\ast}{\longrightarrow} E/ T X \stackrel{\theta^\ast}{\longrightarrow} E/X$$ 

and of course the terminal object $1_X: X \to X$ is automatically and uniquely a $\theta^\ast T_\ast$-algebra. The next two propositions then follow immediately from the definitions of inductive subobject and well-founded coalgebra: 

+-- {: .num_prop} 
###### Proposition 
A subobject $i: U \to X$ of a $T$-coalgebra $(X, \theta)$ is inductive precisely when $i$ is a $\theta^\ast T_\ast$-subalgebra of the terminal object $1_X$ of $E/X$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
A $T$-coalgebra $X$ is well-founded precisely when the terminal $\theta^\ast T_\ast$-algebra $1_X$ is semi-Peano. 
=-- 



## Examples

### Well-founded relations 

The prototype of the notion of well-founded coalgebra is a well-founded [[relation]], which is essentially the same thing as a well-founded coalgebra over the covariant power-set functor $P: Set \to Set$. In brief, a binary [[relation]] $\prec$ on a set $X$ corresponds to a coalgebra $\theta: X \to P X$, by saying $y \prec x$ if and only if $y \in \theta(x)$. See [[well-founded relation]] for more information. 

Most of the constructions of this article are well-illustrated by checking them against the background of this prototypical case. 

## Induction and recursion 

"One _proves_ things by [[induction]]; one _defines_ things by [[recursion]]." This slogan is not mere pedantry; it is meant to underline a difference between these processes. 

A [[proof]] by induction, say a proof of a [[property]] or [[predicate]] $R(x)$ where $x$ varies over a domain $X$, proceeds by showing that the subobject $i: U \hookrightarrow X$ defined by $R$ is an inductive subset with respect to a relation on $X$. It follows that $R$ is universally true on $X$, if the relation is well-founded. The same idiom applies more generally to well-founded coalgebras. 

A recursive construction on the other hand involves a _dependency_ on prior stages of the construction. A typical application is to define a map $f: X \to A$ by recursion with respect to a well-founded relation, where $f(x)$ is specified in three stages: 

* Consider the collection $\theta(x) = \{y: y \prec x\}$ of all elements preceding $x$; 

* Pass to the values $f(y)$ defined earlier in the construction, giving a subset $P(f)(\theta(x)) = \{f(y): y \prec x\}$ of $A$; 

* Apply a given operation $\phi: P(A) \to A$ to this subset $(P(f) \circ \theta)(x)$, to obtain $f(x)$.   

In the last step, the operation may be only partially defined on $P(A)$. In fact, the map $f$ itself may be only partially defined; $f(x)$ is defined only if $\phi((P(f) \circ \theta) (x))$ is defined "when we call for it". 

An inductive argument is used to show that $f$, so far as it is defined, is uniquely determined. The recursive equation that uniquely determines $f$ (to the extent that it exists, of course) is 

$$f = \phi \circ P(f) \circ \theta.$$ 

Letting $\downarrow x$ denote the down-closure of an element $x \in X$ with respect to $\prec$ (and containing $x$), we may then form the set 

$$\{x \in X: \exists_{g: \downarrow x \to A} (g = \phi \circ P(g) \circ \theta)\}$$ 

whence the existence of a map $f: X \to A$ satisfying the recursive equation might indeed be proven by appeal to an inductive argument. 

However, notice that this set is defined by a construction in [[dependent type theory]]. For other categories $C$, we might not have the luxury of interpreting dependent types, so there it wouldn't be right to conflate recursion with induction. 

It is nevertheless true that one can prove, in rather considerable generality, both an induction principle and recursion theorem for well-founded coalgebras; this will occupy us in the following sections. 

## Related concepts

* [[well-founded relation]]

## References 

* [[Paul Taylor]], _Practical Foundations of Mathematics_ , Cambridge University Press (1999). 
 {#Taylor99}

* [[Paul Taylor]], _Towards a unified treatment of induction_ , I: the general recursion theorem (1996). ([pdf](http://www.paultaylor.eu/ordinals/towuti.pdf))
 {#Taylor96}

[[!redirects well-founded coalgebras]]