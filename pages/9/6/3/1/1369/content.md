#Idea#

As discussed at the end of the entry on 
[[monoidal category]],
an ordinary [[monoidal category]] may be thought of as a lax functor

$$
  * \to \mathbf{B} Cat
$$

from the terminal category to the one-object 3-category whose single 
[[hom-object]] is the [[2-category]] [[Cat]] of all categories and for which composition is the [[cartesian monoidal category|cartesian monoidal structure]] on [[Cat]].

More concretely, as also described there, such a lax functor is a 
kind of [[descent]] object in 
a [[weighted limit]] $lim^{\Delta} const_{\mathbf{B}Cat}$, namely
a diagram

$$
  \array{
    F \Delta^4 &\stackrel{=}{\to}& \mathbf{B} Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F \Delta^3 &\stackrel{\alpha}{\to}& \mathbf{B} Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F \Delta^2 &\stackrel{\otimes}{\to}& \mathbf{B} Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F \Delta^1 &\stackrel{C}{\to}& \mathbf{B}Cat
    \\
    \uparrow && \uparrow^{Id} 
    \\
    F\Delta^0 &\stackrel{\bullet}{\to}& \mathbf{B}Cat
  }
$$

where $F \Delta^n$ is the free 3-category of the $n$-[[simplex]] 
(an [[oriental]]), where the horizontal morphisms are the chosen data 
 -- the category $C$, product $\otimes$, associator $\alpha$ and, 
in degree 4, the respect for the pentagon identity --
and the condition is that this commutes for all vertical morphisms 
$F(\Delta^n \to \Delta^m)$.

So this is a 4-functor

$$
  F(\Delta^4) \to \mathbf{B}Cat
$$

subject to a certain constraint. 

Using the general mechanism of [[generalized universal bundle]]s, this 
classifies a [[Cat]]-bundle

$$
  \array{
    C^\otimes \to F(\Delta^4)
  }
  \,.
$$

With a bit more time than I have on the train one can figure out
that conversely suitable such fibrations are equivlent to monoidal
categoriesy. Alternatively, one can read pages 5 and 6 of
_LurieNonCom_ cited below.

In any case, this motivates the following definition.

#Definition#

A **monoidal ($\infty,1$)-category** $(C, \otimes)$
is 

* a [[simplicial set]] $C^\otimes$;

* and a coCartesian fibration of simplicial 
sets $ p_\otimes : C^\otimes \to N(\Delta)^{op}$

* such that for each $n \in \mathbb{N}$ the induced [[(infinity,1)-functor]]
$C^\otimes_{[n]} \to C^\otimes_{\{i,i+1\}}$ determines an
equivalence of [[(infinity,1)-category|(infinity,1)-categories]]

$$
  C^\otimes_{[n]}
  \to
  C^\otimes_{\{0,1\}}
  \times
  \cdots
  \times
  C^\otimes_{\{n-1,n\}}
  \simeq
  (C^\otimes_{[1]})^n
  \,.
$$

Here $\Delta$ is the [[simplex category]] and $N(\Delta)$ its [[nerve]].


#References#

this is definition 1.1.2 in 

* [[Jacob Lurie]], _Noncommutative algebra_ ([pdf]())