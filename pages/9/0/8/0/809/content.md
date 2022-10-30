
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In a [[cubical set]], you are guaranteed for every $n$-cell (which can be drawn as a 1-cell)

$$a\stackrel{f}{\to}b$$

that there is the identity $(n+1)$-cell (which can be drawn as a 2-cell) of the form

$$\array{
a & \stackrel{f}{\to} & b \\
\darr^{Id} & \Downarrow^{Id} & \darr^{Id} \\
a & \stackrel{f}{\to} & b
}$$

A cubical set is said to have _connections_ if in addition it has for every $n$-cell $a\stackrel{f}{\to}b$ also $(n+1)$-cells of the form

$$\array{
a & \stackrel{f}{\to} & b \\
\darr^{f} & \Downarrow & \darr^{Id} \\
b & \stackrel{Id}{\to} & b
}$$

And so forth. You should think of this as saying that the "thin" cell

$$a\underoverset{f}{f}{\rightrightarrows}b$$


is regarded as a degenerate cube by the cubical set in all the possible ways.

So it's a very natural condition,  particularly if you think of all these cubical cells as cubical paths in some space.

## Definition

If $K= \{K_n| n \geq 0\}$ is a [[cubical set]], then a **connection structure on $K$** consists of functions $\Gamma^+_i, \Gamma^- _i: K_n \to K_{n+1}$, $i=1, \ldots \, , n; n \geq 1$, satisfying the relations for $\alpha, \beta=\pm$: 

1. $\Gamma^\alpha_i\Gamma^\beta_j= \Gamma^\beta_{j+1} \Gamma^\alpha _i$ if $i \lt j$; 

1.  $\Gamma^\alpha_i\Gamma^\alpha_i= \Gamma^\alpha_{i+1} \Gamma^\alpha _i$;

1. $\partial^\alpha_j \Gamma^\alpha_j= \partial ^\alpha_{j+1} \Gamma ^\alpha_j = id$;

1. $\partial^\alpha_j \Gamma^{-\alpha}_j= \partial ^\alpha_{j+1} \Gamma ^{-\alpha}_j = \varepsilon _j \partial^\alpha_j$;

1. $ \partial^\alpha_i \Gamma ^\beta_j = \begin{cases}\Gamma^\beta_{j-1} \partial ^\alpha _i & \text{if }\; i \lt j \\    \Gamma^\beta_j \partial ^\alpha _{i-1} & \text{if }\;  i \gt j+1; \end{cases} $

1. $ \Gamma^\alpha_j \varepsilon_j = \varepsilon^2_j = \varepsilon_{j+1}\varepsilon _j$;

1. $\Gamma^\alpha_i \varepsilon _j = \begin{cases}
\varepsilon_{j+1} \Gamma^\alpha _i & \text {if }\;  i \lt j \\
\varepsilon _j \Gamma^\alpha_{i-1} & \text{if }\;  i \gt j ;
\end{cases}$  

The connections are to be thought of as "extra degeneracies". A degenerate cube of type $\varepsilon_j x$ has opposite faces equal and all other faces degenerate.

A cube of
type  $ \Gamma_i^\alpha  x$  has a pair  of adjacent faces equal and
all other faces of type $\Gamma_j^\alpha  y$  or $\varepsilon_j y$ . So this makes the cubical theory nearer to the simplicial. 
Cubical complexes with this, and other, structures  have  also
been considered by Evrard.

The first appearance of this notion in dimension $2$ was in the paper by Brown and Spencer listed below, and used to obtain an equivalence between crossed modules and edge symmetric double groupoids with connection. 

Such connections on cubical sets were introduced in 1981 by Brown and Higgins in order to obtain the equivalence of their "cubical [[∞-groupoids]]" with [[crossed complexes]]. They are also essential to allow the notion of "commutative $n$-shell" in such a structure. 




## Properties

### As a model for homotopy theory

The ordinary [[cube category]] is a _[[test category]]_. This means that bare [[cubical sets]] carry the structure of a [[category with weak equivalences]] whose [[homotopy category]] is that of [[∞-groupoids]].

But the category of cubes _with connection_  is even a _[[strict test category]]_ ([Maltsiniotis, 2008](#Maltsiniotis)). This means that under [[geometric realization]] (see the discussion at [[homotopy hypothesis]]) the [[cartesian product]] of cubical sets with connection is sent to the correct product [[homotopy type]].

The lack of this property for cubical sets without connection was one of the original reasons reasons for abandoning Kan's initial cubical approach to combinatorial [[homotopy theory]] in favour of the simplicial approach; the implications of this new result have yet to be thought through. Another reason was that cubical groups were in general not Kan complexes; however cubical groups with connection are Kan complexes. See the paper by Tonks listed below. 

## Examples

The prime example of  a  cubical   set  with  connections  is the
singular cubical complex  $KX$  of a [[topological space]] $X$.   Here for $n
\ge 0$ $K_n$ is  the  set  of singular $n$-cubes in $X$ (i.e.
continuous maps $I^n   \to   X$)  and the connection $
\Gamma_i^\alpha :K_{n } \to   K_{n+1}$  is induced by the map
$\gamma_i^\alpha   : I^{n+1} \to
 I^{n}$    defined by

   $$   \gamma _i^\alpha (t_1 ,t_2 ,\ldots \, ,t_{n+1} ) =
             (t_1 ,t_2 ,\ldots\, ,t_{i-1},A(t_i ,t_{i+1}),t_{i+2},\ldots \, ,t_{n+1} )
             $$

 where $A(s,t)=\max(s,t), \min(s,t)$ as $\alpha=-,+$ respectively.

The first hint of such a general structure came in the paper by Brown and Spencer given below. The term "[[connection]]" was used there because of a relation of a generalisation of this idea to [[connection on a bundle|path-connections]] in differential geometry. A principal $G$-bundle $E$ over $B$ gives rise to the Ehresmann  groupoid $Equ(E)$ of $G$-maps between the fibres, and the Moore paths $\Lambda$ on this form a double category $D$ with $Equ(E)$ and $\Lambda(B)$ as edge categories. A connection $\Gamma$ is then a functor from $\Lambda(B)$ to one of the category structures on $D$ which gives a smooth lifting of paths to transport of the fibres. This is the origin of the term [[transport law]] for the relation of connections to composition. 



## References

* [[Ronnie Brown]] and C.B. Spencer,  "Double groupoids and crossed modules'', Cah.  Top. G&#233;om. Diff. 17 (1976) 343--362.

* Evrard, M., "Homotopie des complexes simpliciaux et cubiques", Preprint(1976).

* Brown, R.  and  Higgins, P.J., "On the algebra of cubes", _J. Pure Appl.  Algebra_ 21 (1981) 233--260.

* F. Al-Agl, R. Brown and R. Steiner, "Multiple categories: the equivalence between a globular and cubical approach", _Advances in Mathematics_, 170 (2002), 71--118.

* M. Grandis and L. Mauri, "Cubical sets and their site",  _Theory Applic. Categories_, 11 (2003) 185--201.

*  P.J. Higgins,
"Thin elements and commutative shells in cubical  $\omega$-categories", _Theory Appl. Categ._ 14 (2005) 60--74. 

The statement that cubical groups with connections are Kan complexes is due to 

* A. Tonks,  "Cubical groups which are Kan", _J. Pure Appl. Algebra_, 81 (1992) 83--87.

Cubical sets with connection are used in the following paper:

* I. Patchkoria "Cubical approach to derived functors" Homology Homotopy Appl.
Volume 14, Number 1 (2012), 133-158.

and in the following in preference to simplicial methods:

* A Vezzani - "A motivic version of the theorem of Fontaine and Wintenberger"  arXiv:1405.4548, 


The statement that cubes with connection form a [[strict test category]] is due to 

* [[Georges Maltsiniotis]], _La cat&#233;gorie cubique avec connections est une cat&#233;gorie test stricte_, preprint, 2009, 1--16. ([web](http://www.intlpress.com/HHA/v11/n2/a15/))
 {#Maltsiniotis}

based on 

* [[Denis-Charles Cisinski]], _Les pr&#233;faisceaux comme mode&#232;le des types d'homotopie_, Ast&#233;risque, 308 (2006) 


[[!redirects connection on cubical sets]]
[[!redirects connections on a cubical set]]
[[!redirects connections on cubical sets]]