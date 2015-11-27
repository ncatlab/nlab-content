#Idea#
Although just another way of writing down the axioms of a strict [[2-group]], the form of specification used for $cat^1$-groups, and, adapted for [[cat-n-group]]s, is very useful as it is in purely group theoretic terms and so is often easier to check than the more categorically phrased version, for instance, in deriving a $cat^1$-group structure from a [[simplicial group]], or a $cat^n$-group structure from an $n$-fold simplicial group.

The inclusion of this entry is to help the user move between the various forms used in the literature: see references below.

#Definition#

A **$cat^1$-group** is a triple, $(G,s,t)$, where
$G$ is a group and $s,t$ are [[endomorphism]]s of $G$ satisfying conditions
1. $s t = t$ and $t s = s$.
2. $[Ker\,s, \,Ker\,t ] = 1$.

#Discussion#

A cat$^1$-group is just a reformulation of an [[internal category]] in [[Grp]].  (The [[interchange law]] is given by the [[kernel]] [[commutator]] condition.)  As we know these latter objects are equivalent to [[crossed module]]s, we expect to be able to go between $cat^1$-groups and crossed modules without hindrance, and we can:

+--{.un_lemma}
######Lemma
**(Form of the Brown&#8211;Spencer theorem).**
The categories of $cat^1$-groups and crossed modules are equivalent.
=--

+--{.proof}
######Proof
Setting $M = Ker s$, $N = Im s$ and $\partial = t | M,$ then the action of $N$ on $M$ by [[conjugation]] within $G$ makes $\partial: M\to N$ into a crossed module.  Conversely if $\partial: M\to N$ is a crossed module, then setting $G = M \rtimes N$ and letting $s,t$ be defined by
$$
s(m,n) = (1,n)
$$
and
$$
t(m,n) = (1,\partial(m)n)
$$
for $m \in M$, $n \in N,$ we have that $(G,s,t)$ is a $cat^1$-group.

=--

#See also#

* [[single-sorted definition of a category]]

#References#

Loday introduced $cat^1$-groups in his work on the modelling of [[homotopy n-type]]s.

* J.-L. Loday, _Spaces with finitely many homotopy groups_, J.Pure Appl. Alg., 24, (1982), 179 
&#8211; 202.