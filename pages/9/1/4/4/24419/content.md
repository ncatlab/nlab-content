
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

By a *multifunctor* one may mean:

1. a "functor of several variables", i.e., the [[categorification]] of the notion of a *[[multifunction]]*)

1. a *[[morphism of multicategories]]*.


## Functor of several variables

There are multiple ways to generalize the notion of a functor to have several inputs $C_0,\ldots \to D$. The most common is the following, which could be called *jointly functorial* 

1. A [[multifunction]] on objects $F : |C_0|,\ldots \to |D|$
2. For morphisms $f_0 : C_0(a_0,b_0),\ldots$, a morphism $F(f_0,\ldots) : F(a_0,\ldots) \to F(b_0,\ldots)$.
3. Preserving identity $F(id_a,\ldots) = id_{F(a,\ldots)}$
4. And composition $F(f_0 \circ g_0,\ldots) = F(f_0,\ldots) \circ F(g_0,\ldots)$

Such a jointly functorial action is precisely equivalent to an ordinary functor $C_0 \times \cdots \to D$. In the case of one input this is an ordinary functor, for zero it is just an object of $D$ and for 2 it is a [[bifunctor]].

On the other hand, rather than requiring an action on morphisms from each domain category simultaneously, we might require that an action on each domain category separately, which we could call *separately functorial*. I.e., a separately functorial action $C_0,\ldots \to D$ would consist of

1. A multifunction on objects $F : |C_0|,\ldots \to D_0$
2. Such that for each domain category $C_i$, and objects $a_0,\ldots\hat{a_i},\ldots$, the action $F(a_0,\ldots,\hat {a_i},\ldots) : C_i \to D_0$ extends to a functor from $C_i$ to $D$.

This definition is equivalent to an ordinary functor out of the [[funny tensor product]] of the domain categories $$C_0 \Box \cdots \to D$$. This gives the same notion for 0 or 1 input, but is different in general for 2 or more inputs. See the [[funny tensor product]] for more detail.

## References

On "functors of several variables":

* [[eom]]: *[Multi-functor](https://encyclopediaofmath.org/wiki/Multi-functor)*



[[!redirects multifunctors]]

[[!redirects multi-functor]]
[[!redirects multi-functors]]

