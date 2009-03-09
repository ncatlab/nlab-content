A _relation_ is the extension of a [[predicate]].  That is, if you have a statement whose [[truth value]] may depend on some variables, then you get a relation that consists of those instantiations of the variables that make the statement true.  Equivalently, you can think of a relation as a [[function]] whose [[target]] is the set of truth values.

# Definitions #

## General case ##

Given a family $(A_i)_{i: I}$ of [[set]]s, a **relation** on that family is a [[subset]] of the [[cartesian product]] $\prod_{i: I} A_i$.  Equivalently, a **relation** is a [[function]] from $\prod_{i: I} A_i$ to the set $\TV$ of [[truth value]]s (because $\TV$ is the [[subobject classifier]] in [[Set]]).

## Special cases ##

A __nullary relation__ is a relation on the empty family of sets.  This is the same as a [[truth value]].

A __unary relation on $A$__ is a relation on the singleton family $(A)$.  This is the same as a [[subset]] of $A$.

A __binary relation on $A$ and $B$__ is a relation on the family $(A,B)$, that is a subset of $A \times B$.  This is also called a __relation from $A$ to $B$__, especially in the context of the $2$-category [[Rel]] described below.

A __binary relation on $A$__ is a relation on $(A,A)$, that is a relation from $A$ to itself.  This is sometimes called simply a __relation on $A$__.

An __$n$-ary relation__ on $A$ is a relation on a family of $n$ copies of $A$, that is a subset of $A^n$.

For a binary relation, one often uses a symbol such as $\sim$ and writes $a \sim b$ instead of $(a,b) \in \sim$.  Actually, even when a relation is given by a letter such as $R$, one often sees $a R b$ instead of $(a,b) \in R$, although now that does not look so good.

# Binary relations #

Binary relations are especially widely used.

## Kinds of binary relations ##

Special kinds of relations from $A$ to $B$ include:
* [[functional relation]]s;
* [[entire relation]]s.

A [[function]] can be seen as a binary relation that is both functional and entire.

Special kinds of binary relations on $A$ additionally include:
* [[reflexive relation|reflexive]] and [[irreflexive relations|irreflexive]] relations;
* [[symmetric relation|symmetric]]s, [[antisymmetric relation|antisymmetric]], and [[asymmetric relation|asymmetric]] relations;
* [[transitive relation]]s and [[comparison]]s;
* [[well-founded relation]]s.

Combinations of the above properties of binary relations produce [[equivalence relation]]s and the various kinds of [[order]]s.  There are also [[total relation|total]] and [[linear relation|linear]] relations, although these are properties of partial orders and quasiorders that aren\'t usually considered by themselves.

## The $2$-poset of binary relations ##

Binary relations form a $2$-[[2-category|category]] (in fact a $2$-[[2-poset|poset]]) [[Rel]], which is the basic example of an [[allegory]].

The objects are [[set]]s, the morphisms from $A$ to $B$ are the binary relations on $A$ and $B$, and there is a $2$-morphism from $R$ to $S$ (both from $A$ to $B$) if $R$ implies $S$ (that is, when $(a,b) \in R$, then $(a,b) \in S$).

The interesting definition is composition:  If $R$ is a relation from $A$ to $B$ and $S$ is a relation from $B$ to $C$, then the composite (written $S \circ R$ or $R;S$) from $A$ to $C$ is defined as follows:
$$(a,c) \in R;S \;\Leftrightarrow\; \exists b: B,\; (a,b) \in R \;\wedge\; (b,c) \in S.$$
The identity morphism is given by [[equality]].

The special properties of the kinds of binary relations listed earlier can all be described in terms internal to $\Rel$ and therefore make sense in any allegory (I think ...).

As a [[function]] may be seen as a special kind of relation, so the category [[Set]] of sets and functions is a [[subcategory]] of [[Rel]].

# Generalisation #

Most of the preceding makes sense in any [[category]] with enough [[product]]s.  Probably the trickiest bit is the definition of composition of binary relations, so not every category with finite products has an allegory of relations.