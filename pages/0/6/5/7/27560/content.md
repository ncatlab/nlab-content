## Idea

Betweeness is a ternary relation on a set of points of the same line in geometry. It brings into attention the essential difference between a segment and a line into axiomatic geometry by means of an ordering.

## Axiomatic definition

Suppose we are in the setup of incidence geometry. We introduce the notion of order of betweeness as follows (yielding an ordered incidence geometry). Here we shall work with strict betweeness.

Each line $l$ in ordered incidence geometry is equipped with a ternary relation $a b c$ among where $a,b,c$ are three distinct points on $l$ (that is, incident with $l$). We then say that $b$ is between $a$ and $c$. If $a\neq c$ denote by $(a,c)$, the open interval determined by $a$ and $c$, as the set of all points on line $l$ between $a$ and $c$. The segment $\overline{a c}$ is the set of all points between $a$ and $c$ including also the end points $a$ and $c$.

Axioms (see [Ben-Tal, Ben-Israel](#BenTalBenIsrael))

A1 If $a b c$ then $c b a$.

A2 If $a\neq b$ then there are $c, d$ such that $a c b$ and $a b d$.

A3 If $a,b,c$ are colinear and distinct then precisely one of them is between the other two.

A4 (Pasch's axiom) If $a,b,c$ are three noncolinear points, and $l$ a line in their affine hull (the plane determined by $a,b,c$) then if $l$ intersects $(a,b)$ then it intersects either $(a,c)$ or $(b,c)$.

## From linear order relations

One can alternatively postulate that on every line one is given two mutually opposite [[linear order]]s $\leq_1,\leq_2$ and define the non-strict betweeness $[a b c]$ if $a \leq b\leq c$ in (at least) one of the distinguished orders and a strict betweeness $a b c$ if $a \lt b \lt c$ in (presicely) one of the distinguished orders (thus excluding the possibility that $b$ equals either $a$ or $c$ in the strict case). 
Then one requires just the Pasch's axiom (e.g. [PavkovićVeljan](#PavkovicVeljan)). 

## History

This approach is devised by M. Pasch around 1882.

## Literature

* {#BenTalBenIsrael} Aharon Ben-Tal, Adi Ben-Israel, _Ordered incidence geometry and the geometric foundations of convexity theory_, Journal of Geometry __30__ (1987)
* M. Pasch, [[Max Dehn]], _Vorlesungen ueber die neuere Geometrie_,. Springer-Verlag, Berlin, 1926 (reprinted 1976), x + 275 pp
* {#PavkovicVeljan} B. Pavković, D. Veljan, _Elementarna matematika I_, Školska knjiga 2004, Zagreb (in Croatian)

category: geometry

[[!redirects ordered incidence geometry]]