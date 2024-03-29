
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


\tableofcontents

## Idea 

Just as the classical notion of *[[pointed objects]]* refers to *morphisms* whose [[domain]] is [[terminal object|terminal]], which in the context or [[doctrine]] of [[cartesian monoidal categories]] is the monoidal unit, so one can generalize such "pointing": a pointed object in a [[monoidal category]] $\mathcal{C}$ is an [[object]] $X$ equipped with a [[morphism]] $I \to X$ from the [[monoidal unit]] $I$. 

A [[morphism]] between a [[pair]] of monoidally-pointed objects is then typically taken to be a morphism of the [[underlying]] objects which respects these "points" under [[precomposition]]. This means that the [[category]] of monoidally-pointed objects is the [[coslice category]] $I \downarrow \mathcal{C}$. 

Therefore, yet more generally, one might regard any [[coslice category]] as a category of generalized-pointed objects. But the coslice under a monoidal unit has further good properties, such as itself canonically inheriting the structure of a monoidal category.

## Examples 

\begin{example}
A [[pointed endofunctor]] on a category $C$ is an [[endofunctor]] $F$ together with a [[natural transformation]] $1_C \to F$ out of the [[identity functor]]. Since the [[endofunctor category]] $[C, C]$ may be viewed as a [[strict monoidal category]] whose monoidal unit is the identity functor, this is an example of a pointed object in a monoidal category. 
\end{example}

\begin{example}
A [[pointed abelian group]] is an [[abelian group]] $A$ equipped with a morphism $\mathbb{Z} \to A$, where $\mathbb{Z}$ is the unit for the [[tensor product of abelian groups]]. 
\end{example}

\begin{example}
A [[pointed module]] is a [[module]] $M$ equipped with a morphism $R \to M$ from the [[ground ring]] $R$, where $R$ is also the unit for the [[tensor product of modules]]. Similarly, a [[pointed vector space]] is a [[vector space]] $V$ equipped with a morphism $F \to V$ from the ground [[field]] $F$, where $F$ is also the unit for the [[tensor product of vector spaces]]. 
\end{example}

\begin{example}
A [[bi-pointed object|bi-pointed set]] is a [[pointed set]] $S$ equipped with a morphism $\mathbb{B} \to S$ from the [[boolean domain]] $\mathbb{B}$, where the [[smash product]] is the [[tensor product]] and the [[boolean domain]] is the [[tensor unit]] of the [[monoidal category]] of pointed sets. 
\end{example}

\begin{example}
Under change of [[base of enrichment]], pointed objects in the current sense may be compared to pointed objects in the classical sense. For example, if $V$ is a monoidal category, there is a [[lax monoidal functor|lax monoidal]] change of base functor 
$$U = V(I, -): V \to Set$$ 
and a pointing of an object $v$ of $V$ is equivalent to a pointing of its underlying object in the classical sense, $1 \to U(v)$. 
\end{example} 

\begin{example} 
If $C$ is a monoidal category, then $C^{op}$ acquires a monoidal category structure as well, and the coslice $I \downarrow C^{op}$ of monoidally pointed objects is equivalent to the slice $C \downarrow I$. This can be important in practice. See for example the discussion at [[affine space]] which relates the definition of affine space to the slice $Vect_k/k$, and see even more particularly the discussion of the [[affine space#ClosedMonoidal|closed monoidal]] structure of affine spaces. 
\end{example} 

## References

The term appears, for instance, in:

* {#Melliès09} [[Paul-André Melliès]], Nicolas Tabareau & Christine Tasson, p. 4 of: *An Explicit Formula for the Free Exponential Modality of Linear Logic*, in: *Automata, Languages and Programming. ICALP 2009*, Lecture Notes in Computer Science, **5556**, Springer (2009) &lbrack;[doi:10.1007/978-3-642-02930-1_21](https://doi.org/10.1007/978-3-642-02930-1_21)&rbrack;

     
[[!redirects pointed objects in a monoidal category]]
[[!redirects pointed objects in monoidal categories]]

