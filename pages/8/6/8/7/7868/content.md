Each [[category with star-morphisms]] gives rise to a category (<b>abrupt
category</b>, see a remark below why I call it "abrupt"), as described below.
Below for simplicity I assume that the set $M$ and the set of our indexed
families of functions are disjoint. The general case (when they are not
necessarily disjoint) may be easily elaborated by the reader.

% Objects are indexed (by $\operatorname{arity}m$ for some
$m \in M$) families of objects of the category $C$ and an (arbitrarily
choosen) object $\operatorname{None}$ not in this set

% There are the following disjoint sets of morphisms:

* indexed (by $\operatorname{arity} m$ for some $m \in M$) families of morphisms of $C$

* elements of $M$

* the identity morphism $\operatorname{id}_{\operatorname{None}}$ on $\operatorname{None}$

% Source and destination of morphims are defined by the formulas:

* $\operatorname{Src}f = \lambda i \in
    \operatorname{dom}f : \operatorname{Src}f_i$;

* $\operatorname{Dst}f = \lambda i \in
\operatorname{dom}f : \operatorname{Dst}f_i$

* $\operatorname{Src}m =\operatorname{None}$

* $\operatorname{Dst}m
    =\operatorname{Obj}_m$.

% Compositions of morphisms are defined by the formulas:

* $g \circ f = \lambda i \in \operatorname{dom}f : g_i
    \circ f_i$

* $f \circ m =\operatorname{StarProd} \left( m ; f
\right)$

* $m \circ \operatorname{id}_{\operatorname{None}} = m$

* $\operatorname{id}_{\operatorname{None}} \circ \operatorname{id}_{\operatorname{None}} = \operatorname{id}_{\operatorname{None}}$

% Identity morphisms for an object $X$ are:

* $\lambda i \in X : \operatorname{id}_{X_i}$ if $X \neq
\operatorname{None}$

* $\operatorname{id}_{\operatorname{None}}$
if $X =\operatorname{None}$

We need to prove it is really a category.

**Proof** We need to prove:

* Composition is associative

* Composition with identities complies with the identity law.

Really:

* $\left( h \circ g \right) \circ f = \lambda i \in \operatorname{dom} f :
\left( h_i \circ g_i \right) \circ f_i = \lambda i \in \operatorname{dom} f : h_i
\circ \left( g_i \circ f_i \right) = h \circ \left( g \circ f \right)$;

$g \circ \left( f \circ m \right) = \operatorname{StarComp} \left( \operatorname{StarComp}
\left( m ; f \right) ; g \right) = \operatorname{StarComp} \left( m ; \lambda i \in
\operatorname{arity} m : g_i \circ f_i \right) = \operatorname{StarComp} \left( m ; g \circ
f \right) = \left( g \circ f \right) \circ m$;

$f \circ \left( m \circ \operatorname{id}_{\operatorname{None}} \right) = f \circ m = \left(
f \circ m \right) \circ \operatorname{id}_{\operatorname{None}}$.

* $m \circ \operatorname{id}_{\operatorname{None}} = m$; $\operatorname{id}_{\operatorname{Dst} m} \circ
m = \operatorname{StarComp} \left( m ; \lambda i \in \operatorname{arity} m :
\operatorname{id}_{\operatorname{Obj}_m i} \right) = m$.

**Remark** I call the above defined category <b>abrupt category</b> because (excluding identity morphisms) it allows composition with an $m \in M$ only on the left (not on the right) so that the morphism $m$ is "abrupt" on the right.

[[category with star-morphisms|Categories with star-morphisms]] and **abrupt categories** arise in research of [[cross-composition product]].