\tableofcontents

## Definition

The [[category]] of [[classes]] has [[classes]] as objects
and maps of classes as morphisms.

In the [[Zermelo-Fraenkel set theory]],
a [[class]] is a [[proposition]] $P$ with a designated [[free variable]] $x$.
We interpret $P(x)$ as saying that $x$ belongs to the class $P$.
We also write $x\in P$, while understanding that $P$ is not a set,
but $x$ is.

For example, any [[set]] $A$ is a [[class]],
whose proposition is $a\in A$ and the designated [[free variable]] is $a$.

The proposition $a=a$ defines the [[class]] of all sets, which
does not arise via the above construction from any [[set]].

## Relations and maps

Given two classes $A$ and $B$, we can form their [[product]] $A\times B$
as the class $A\times B$ such that $P(x)$ means $x=(a,b)$ for some $a\in A$ and $b\in B$,
where $(a,b)$ denotes the usual [[ordered pair]] constructed
in [[Zermelo-Fraenkel set theory]] as $(a,b)=\{\{a\},\{a,b\}\}$
or $(a,b)=\{\{\emptyset,a\},\{b\}\}$
or $(a,b)=\{\{\{\emptyset\},a\},\{b\}\}$.

If $P(x)$ implies $Q(x)$, we say that $P$ is a subclass of $Q$.

A [[relation]] from $A$ to $B$ is a subclass of $A\times B$.

A [[map]] $f$ from $A$ to $B$ is a relation $R$ from $A$ to $B$
such that for any $a\in A$ there is a unique $b\in B$ such that $R(a,b)$.
In this case we write $f(a)$ for this unique $b$,
so $f(a)=b$ means $R(a,b)$.

[[maps|Maps]] of [[classes]] can be [[composed]] in the usual manner,
which produces a [[category]].
Here a category is understood in the sense of a [[first-order logic]]
with two sorts (objects and morphisms),
but at no point we attempt to consider all [[classes]] as a single unified whole.

A [[family]] $f$ of [[classes]] indexed by a class $I$
is a [[map]] of classes $f\colon T\to I$.
The [[class]] indexed by $i\in I$ is the [[preimage]] $f^*\{i\}$.
Such families can be pulled back along maps of classes $J\to I$ and pushed forward along maps $I\to J$.

We can now define [[large categories]] as having a [[class]] of objects,
a [[class]] of morphisms,
together with [[composition]] and [[identities]] satisfying the usual axioms.
The [[category]] of [[classes]] considered above is not a [[large category]] in this sense.

We do not require [[large categories]] to be [[locally small]].

## Diagrams

Suppose $I$ is a [[large category]].
An $I$-indexed [[diagram]] of classes is defined as follows.
First, we have an $I$-indexed family of classes $f\colon T\to I$.
Secondly, we have a transition map
$$tr\colon\{(t,h)\mid t\in T, h\in Mor(I), f(t)=dom(h)\}\to T,$$
which is a map of classes such that $f(tr(t,h))=codom(h)$.
(The [[domain]] of $tr$ is a [[class]] because $t$ and $h$ are [[sets]].)
Finally, the transition map satisfies the usual axioms expected from a functor.

## Limits

The category of [[classes]] admits all [[small limits]].

First, it admits [[equalizers]]: the equalizer of $f,g\colon A\to B$
is the subclass $E$ of $A$ defined by $E(e)=(e\in A \land f(e)=g(e))$.

Secondly, it admits [[small products]]: the [[small product]] of
an $I$-indexed family of classes $f\colon T\to I$,
where $I$ is an arbitrary [[set]] (considered as a [[class]] when used with $f$)
can be constructed as the class $P$ such that $p\in P$
if $p$ is a [[map of sets]] whose [[domain]] is $I$
and for all $i\in I$ we have $p(i)\in T$ and $f(p(i))=i$.
(Observe that $P$ is indeed a class.)

Finally, it admits all [[small limits]] because the usual
reduction of [[small limits]] to [[equalizers]] of [[small products]]
continues to work provided that we adhere to the above convention
on the definition of families of classes.

## Colimits

The [[category]] of classes admits all [[colimits]] indexed
by arbitrary [[large categories]] $I$, i.e., large colimits.

First, the standard reduction of $I$-indexed [[colimits]]
to a [[coequalizer]] of a pair of arrows between [[coproducts]] indexed by $Mor(I)$ and $Ob(I)$
still works in this context since class-indexed families of classes can be pulled back
along source and target maps $Mor(I)\to Ob(I)$.

Secondly, class-indexed [[coproducts]] of [[classes]] can be computed simply by taking
the total class $T$ of the corresponding class-indexed family $f\colon T\to I$ of classes.

Thirdly, [[coequalizers]] of [[classes]] exist by [[Scott's trick]].
Observe that given a pair of arrows $f,g:X\to Y$ between classes,
we can define an [[equivalence relation]] on $Y$
by saying that $y~y'$ if there is a map $h:[0,n]\to Y$
such that $h(0)=y$, $h(n)=y'$
and for any $i\in[0,n)$ there is $x\in X$ such that $h(i)=f(x)$ and $h(i+1)=g(x)$
or $h(i)=g(x)$ and $h(i+1)=f(x)$.
The quotient of $Y$ by this equivalence relation exists by [[Scott's trick]]
and is precisely the desired coequalizer.

### Definable classes 

If one is working in the category of (definable) classes for [[ZF]] or [[ZFC]], or the category of classes of [[NBG]], then all finite _external_ diagrams $D\to Class$ have colimits.
The reduction to a coequaliser of a pair of finite coproducts works as per usual.
_Finite_ coproducts exist as one can use finite disjunctions of the defining formulas (in ZF(C)) or Class Separation (in NBG) to define a new class.
Coequalisers then exist by the above argument, as [[Scott's trick]] is available due to the class $V$ of sets having well-founded stratifications by sets (for instance the von Neumann [[cumulative hierarchy]] $V = \bigcup_{\alpha\in ORD} V_\alpha$).

## Other categorical properties

The category of classes is a [[regular category]]:
the obvious notion of [[image factorization]] is stable under [[pullbacks]].
It is also a [[Barr-exact category]]:
every [[equivalence relation]] $R$ on a class $C$ is induced by
the [[quotient map]] $C\to C/R$.

It is also an [[infinitary extensive category]],
where “infinitary” means “class-indexed”.
Indeed, [[pullbacks]] of [[coproduct]] injections along arbitrary maps of classes exist and class-indexed [[coproducts]] are [[disjoint coproducts|disjoint]] and stable under [[pullback]].

It is also [[well-pointed category|well-pointed]]:
for every two maps between classes $f,g:X\rightarrow Y$ and every element $x\in X$, if $f(x) = g(y)$, then $f = g$, 
and the category of classes is not the [[terminal category]]. 

It likewise has all objects corresponding to [[large cardinal]]s, most notably a [[natural numbers object]]. Otherwise, the category of finite sets [[FinSet]] is vacuously a category of classes, as the notions of 'finitary' and 'class-indexed'/'infinitary' coincide. 

As such, the category of classes is a well-pointed infinitary [[Heyting category|Heyting]] or [[Boolean category|Boolean]] [[pretopos]] with a natural numbers object and other large cardinals, 
depending upon the external logic used, 
and where “infinitary” is used in the rather strong sense of “class-indexed”.

The category of classes is not [[cartesian closed]] or [[locally cartesian closed]]
and does not have [[power objects]].
Indeed, the class of all sets $S$ does not have a [[power object]],
or, equivalently, there is no [[internal hom]] $Hom(S,\{0,1\})$.

## Category with class structure

The category of [[classes]] is a primordial example
of a [[category with class structure]].
Its open maps are precisely those maps of classes $f\colon T\to I$
such that $f^*\{i\}$ is a [[set]] for each $i\in I$.
Small maps coincide with open maps.
The powerclass of a class $C$ is the class of all sets $A$ such
that $A$ is a subclass of $C$.
The universal class is the class of all sets.

## Related notions

* [[class]]

* [[proper class]]

* [[large category]]

* [[category with class structure]]


[[!redirects categories of classes]]
[[!redirects Class]]