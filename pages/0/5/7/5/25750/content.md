
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

A [[morphism]] between a [[pair]] of monoidally-pointed objects is then typically taken to be a morphism of the [[underlying]] objects which respects these "points" under [[precomposition]]. This means that the [[category]] of monoidally-pointed objects is the [[coslice category]] $\mathcal{C}^{I/}$. 

(Therefore, yet more generally, one might regard any [[coslice category]] as a category of generalized-pointed objects.)

## Examples 

\begin{example}
A [[pointed endofunctor]] on a category $C$ is an [[endofunctor]] $F$ together with a [[natural transformation]] $1_C \to F$ out of the [[identity functor]]. Since the [[endofunctor category]] $[C, C]$ may be viewed as a [[strict monoidal category]] whose monoidal unit is the identity functor, this is an example of a pointed object in a monoidal category. 
\end{example}

\begin{example}
A [[pointed abelian group]] is a an [[abelian group]] $A$ equipped with a morphism $\mathbb{Z} \to A$, where $\mathbb{Z}$ is the unit for the [[tensor product of abelian groups]]. 
\end{example}


\begin{example}
Under change of [[base of enrichment]], pointed objects in the current sense may be compared to pointed objects in the classical sense. For example, if $V$ is a monoidal category, there is a [[lax monoidal functor|lax monoidal]] change of base functor 
$$U = V(I, -): V \to Set$$ 
and a pointing of an object $v$ of $V$ is equivalent to a pointing of its underlying object in the classical sense, $1 \to U(v)$. 
\end{example}

## References

The term appears, for instance, in:

* [[Paul-André Melliès]], Nicolas Tabareau & Christine Tasson, p. 4 of: *An Explicit Formula for the Free Exponential Modality of Linear Logic*, in: *Automata, Languages and Programming. ICALP 2009*, Lecture Notes in Computer Science, **5556**, Springer (2009) &lbrack;[doi:10.1007/978-3-642-02930-1_21](https://doi.org/10.1007/978-3-642-02930-1_21)&rbrack;

     
[[!redirects pointed objects in a monoidal category]]
[[!redirects pointed objects in monoidal categories]]

