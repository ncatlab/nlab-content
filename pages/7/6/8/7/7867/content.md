
+-- {: .num_remark}
###### Remark
By a _pre-category_ I mean a [[category]] without [[identity morphism|identities]] (a [[semicategory]]).
=--

+-- {: .num_defn}
###### Definition

A **pre-category with star-morphisms** consists of
1. a pre-category $C$ (**the base pre-category**);
2. a set $M$ (**star-morphisms**);
3. a function $\operatorname{arity}$ defined on $M$ (how many objects are connected by this multimorphism);
4. a function $\operatorname{Obj}_m : \operatorname{arity} m \rightarrow \operatorname{Obj}
    \left( C \right)$ defined for every $m \in M$;
5. a function (<em>star composition</em>) $\left( m ; f \right)
    \mapsto \operatorname{StarComp} \left( m ; f \right)$ defined for $m \in M$ and
    $f$ being an $(\operatorname{arity} m)$-indexed family of morphisms of $C$ such
    that $\forall i \in \operatorname{arity} m : \operatorname{Src} f_i = \operatorname{Obj}_m i$
    ($\operatorname{Src} f_i$ is the source object of the morphism $f_i$) such that
    $\operatorname{arity} \operatorname{StarComp} \left( m ; f \right) = \operatorname{arity} m$

such that:

1. $\operatorname{StarComp} \left( m ; f \right) \in M$;
2. (*associativiy law*)
    \[ \operatorname{StarComp} \left( \operatorname{StarComp} \left( m ; f \right) ; g \right)
       = \operatorname{StarComp} \left( m ; \lambda i \in \operatorname{arity} m : g_i \circ
       f_i \right) . \]

(Here $\lambda$ indicates [[function abstraction]].)
=--

The meaning of the set $M$ is an extension of $C$ having as morphisms things
with arbitrary (possibly infinite) indexed set
$\operatorname{Obj}_m$ of objects, not just two objects as
morphims of $C$ have only source and destination.

+-- {: .num_defn}
###### Definition

A **category with star-morphisms** is a pre-category with star-morphisms whose base pre-category is a category and the following equality (*the law of composition with identities*) holds for every multimorphism $m$:
  \[ \operatorname{StarComp} \left( m ; \lambda i \in
     \operatorname{arity}m :
     \operatorname{id}_{\operatorname{Obj}_m i}
     \right) = m. \]
=--

See also [[abrupt category|abrupt categories]].

Categories with star-morphisms and [[abrupt category|abrupt categories]] arise in [[Victor Porton]]\'s research on [[cross-composition product]]s.


[[!redirects category with star-morphisms]]
[[!redirects categories with star-morphisms]]
