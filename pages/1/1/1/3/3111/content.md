
# Generic proofs
* table of contents
{: toc}

## Definition

A **generic proof** in a [[category]] $C$ is a map ([[morphism]]) $\theta\colon \Theta\to\Lambda$ with all [[pullbacks]] such that, for every map $f\colon Y\to X$, there exists a (not necessarily unique) map $\nu\colon X\to \Lambda$ such that $f$ and the [[pullback|pulled back]] map $\nu^*\theta\;\colon\; \Theta \times_\Lambda X \to X$ each factor through each other, i.e. they are equivalent in the [[preorder reflection]] of the [[slice category]] $C/X$.

$$ \array {
   Y \\
   \uparrow \downarrow & \searrow^f \\
   \Theta \times_\Lambda X & \overset{\nu^*\theta}\longrightarrow & X \\
   \downarrow & & \downarrow\mathrlap{\nu} \\
   \Theta & \overset{\theta}\longrightarrow & \Lambda
} $$

The main interest of generic proofs is in the following:

+-- {: .un_theorem}
###### Theorem
If $C$ has [[finite limits]], then its [[ex/lex completion]] $C_{ex/lex}$ is a [[topos]] if and only if $C$ has [[weak dependent product]]s and a generic proof.
=--

In particular, if $C$ is a [[locally cartesian closed category]], then $C_{ex/lex}$ is a topos if and only if $C$ has a generic proof.

A counterpart of generic proofs in [[type theory]] is Russell's [[axiom of reducibility]].


## Axioms of choice

If $C$ is a [[topos]] satisfying the [[axiom of choice]], then its [[subobject classifier]] is a generic proof, since any $f\colon Y\to X$ factors through, and (assuming AC) is factored through by, its [[image]], a subobject of $X$.  In fact, for such a $C$, $C_{ex/lex}$ is equivalent to $C$.

The statement "$Set$ has a generic proof," or equivalently "$Set_{ex/lex}$ is a topos," is weaker than the full axiom of choice. Indeed, [Menni 2007](#Menni2007) shows that the exact completion of a Boolean Grothendieck topos with enough points is also a topos. 

An even weaker statement is "$Set_{ex/lex}$ is [[well-powered category|well-powered]]."  Note that if $X$ is a set, then the subobject lattice of (the image of) $X$ in $Set_{ex/lex}$ is precisely the preorder reflection of $C/X$; thus this second statement says in particular that all such preorder reflections are essentially small.  This can be regarded as saying that although full AC may not hold, it is only violated in a "small way" at each set.  It is sufficient, for instance, to show that the category of [[anafunctors]] between two small categories is essentially small.

An instructive example is $C_{ex/lex}$ where $C = Set^{\to}$ (the [[arrow category]] of $Set$): this is an example of an exact completion of a topos that is well-powered but not itself a topos (because $C$ lacks a generic proof). It also shows, taking $D$ to be the [[coproduct completion]] of the [[walking arrow]], that we can have $D_{ex}$ (which is $Set^\to$ here) a topos but $(D_{ex})_{ex}$ not a topos. Details may be found in Menni's [2003 paper](#Menni2), section 5.3. 


## References

* Mat&#237;as Menni, "Exact completions and toposes", Ph.D. Thesis, U. Edinburgh 2000. ([web](http://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-424/))  

* Mat&#237;as Menni, A characterization of the left exact categories whose exact completions are toposes, J. Pure Appl. Algebra 177 (2003) 287-301. ([pdf](http://www.lifia.info.unlp.edu.ar/papers/2003/Menni2003a.pdf)) 
  {#Menni2}

* Mat&#237;as Menni, Cocomplete toposes whose exact completions are toposes, J. Pure Appl. Alg. 210 (2007), 511&#8211;520. ([pdf](http://www.lifia.info.unlp.edu.ar/papers/2007/Menni2007.pdf)) 
  {#Menni2007} 


[[!redirects generic proof]]
[[!redirects generic proofs]]
