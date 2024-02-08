
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

There are at least two ways to generalize the notion of a [[functor]] to the case where its [[domain]] may an [[n-tuple]] of [[categories]]:

1. [jointly functorial maps](#JointlyFunctorialMaps)

1. [separately functorial maps](#SeparatelyFunctorialMaps)

which we discuss in turn.

In all of the following, 

* $D$ denotes a [[category]] which serves as the [[codomain]];

* $C_1, \cdots, C_n$ denotes an [[n-tuple|$n$-tuple]] of categories serving as the multi-[[domain]];

* ${\vert -\vert}$ denotes passage to the [[class]] of [[objects]] of a ([[strict category|strict]]) category.

### Jointly functorial maps
 {#JointlyFunctorialMaps}

A **jointly functorial** [[map]] from $C_1, \cdots, C_n$ to $D$ consists of:

1. a [[multifunction]] on [[objects]] 

   $$
     F 
       \,\colon\, 
    \big(
      {|C_1|}, \ldots, {\vert C_n\vert} 
    \big)
      \longrightarrow 
     {|D|}
   $$

2. For all [[n-tuples]] of [[morphisms]] 

   $$
     f_i \,\in\, C_i(a_i,b_i), 
     \;\;\;\;
     1 \leq i \leq n
   $$  

   a morphism of the form

   $$
     F(f_1,\ldots, f_n) 
      \,\colon\, 
     F(a_1,\ldots, a_n) \to F(b_1,\ldots, b_n)
   $$

   in $D$.

such that:

1. [[identity morphisms]] are preserved, in that 

   $$
    F(id_{a_1}, \ldots, id_{a_n}) 
    \;=\; 
    id_{F(a_1, \ldots, a_n)}
   $$

4. [[composition]] is respected, in thay

   $$
     F(f_1 \circ g_1,\ldots, f_n \circ g_n) 
     \;=\; 
     F(f_1,\ldots, f_n) \circ F(g_1,\ldots, g_n)
     \,.
   $$

Such a jointly functorial map is the same as an ordinary [[functor]] out of the [[product category]] of the $n$-tuple of domain categories:

$$
  C_1 \times \cdots \times C_n \longrightarrow D
  \,.
$$

In the case $n = 1$ this is an ordinary functor, while for $n = 2$ this is a "[[bifunctor]]". And if one understands multifunctions of [[zero]] arguments as functions out of the empty product of domain categories, which is the [[terminal category]], then for $n = 0$ this is just a choice of [[object]] of $D$. 


### Separately functorial maps
 {#SeparatelyFunctorialMaps}

On the other hand, rather than requiring an "action" on morphisms from each domain category simultaneously, one may want to require an action of each domain category *separately*, which we could call *separately functorial*. I.e., a separately functorial map $\big(C_1,\ldots, C_n\big) \to D$ consists of:

1. A [[multifunction]] of objects 

   $$
     F 
      \colon 
     \big(
       {|C_1|},\ldots, {\vert C_n\vert}  
     \big)
       \longrightarrow 
     D
   $$

2. Such that for each domain category $C_i$, and objects $a_1,\ldots\widehat{a_i},\ldots, a_n$, the map $F(a_1,\ldots,\widehat {a_i},\ldots, a_n) \colon C_i \to D$ extends to a functor from $C_i$ to $D$.

This definition is instead equivalent to an ordinary functor out of the [[funny tensor product]] of the domain categories 

$$
  C_1 \Box \cdots \Box C_n \longrightarrow D
  \,.
$$

For $n = 0$ and $n = 1$ this definition coincides with that of jointly functorial maps [above](#JointlyFunctorialMaps), bu for $n \geq 2$ arguments it is different. 

For more see also at *[funny tensor product -- Separate functoriality](funny+tensor+product#SeparateFunctoriality)*

### Relation Between Joint and Separate Functoriality

Every jointly functorial map defines a separately functorial map by defining the action as
$$F(a_1,\ldots,\widehat {a_i},\ldots, a_n)(f_i) = F(id,\ldots,f_i,\ldots,id)$$

On the other hand, there is not way to extend an arbitrary separately functorial map in this way to be jointly functorial. We can attempt to define 

$$F(f_1,\ldots) = F(\widehat{a_1},\ldots)(f_1) \circ F(a_1,\widehat{a_2},\ldots)(f_2) \circ \cdots$$
But note that for $n\geq 2$ this involves an arbitrary choice of which order to compose these actions, and this will only be a jointly functorial action if all such choices are equal. This can be stated as saying for any pair $i\leq j\leq n$ that
$$F(a_1,\ldots,\widehat{a_i},\ldots a_n)(f_i) \circ F(a_1,\ldots,\widehat{a_j},\ldots,a_n)(f_j) = F(a_1,\ldots,\widehat{a_j},\ldots a_n)(f_j) \circ F(a_1,\ldots,\widehat{a_i},\ldots,a_n)(f_i)$$

## Related concepts

* [[two-variable adjunction]]

## References

On "functors of several variables":

* [[eom]]: *[Multi-functor](https://encyclopediaofmath.org/wiki/Multi-functor)*



[[!redirects multifunctors]]

[[!redirects multi-functor]]
[[!redirects multi-functors]]

