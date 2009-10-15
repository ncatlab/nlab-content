<div class="rightHandSide toc">
[[!include supergeometry - contents]]

***

[[!include synthetic differential geometry - contents]]

</div>




#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The notion of _super smooth topos_ is to that of [[smooth topos]] as [[supergeometry]] is to [[differential geometry]].

The objects of a super smooth topos are generalizations of smooth [[supermanifold]]s that admit besides the usual odd infinitesimals of [[supergeometry]] also the even [[infinitesimal object]]s of [[synthetic differential geometry]].

The study of super smooth toposes is the content of [[synthetic differential supergeometry]]. (See there for references and details for the moment.)

# Definition #

A **super smooth topos** $(\mathcal{T}, R)$ is a [[smooth topos]] together with the refinement of the $k$-algebra structure on $R$ to that of a $k$-[[superalgebra]] structure.


So a super smooth topos is a [[topos]] $\mathcal{T}$ equipped with a [[superalgebra]] object $(R, +, \cdot)$ with even part $R_e$ and odd part $R_o$ etc.

An algebra spectrum object is now an internal object of superalgebra homomorphisms and the condition is that for every super Weil algebra $W = R \oplus m$ we have that $Spec(W) = R SAlg_{\mathcal{T}}(W,R)$ is an [[infinitesimal object]] and that $W \to R^{Spec W}$ is an [[isomorphism]]. 

This means that essentially all the standard general theory of smooth toposes goes through literally for super smooth toposes, too. The main difference is that a super smooth topos contains more types of [[infinitesimal object]]s.

There is for instance still the standard _even_ infinitesimal interval

$$
  D := D^{1|0} := \{\epsilon \in R_e | \epsilon^2 = 0\}
$$

but there is now also the _odd_ infinitesimal interval

$$
  D^{0|1} := \{\theta \in R_o \}
  \,.
$$

Notice that in the graded commutative algebra $A$ every odd element $\theta$ automatically squares to 0.

> [[Urs Schreiber]]: I'd think that the cominatorial/simplicial definition of [[differential forms in synthetic differential geometry]] applied verbatim in a super smooth topos automatically yields the right/expected notion of differential forms in supergeometry. 


# Examples #

Models for super smooth toposes are constructed in

* D. N. Yetter, _Models for synthetic supergeometry_, Cahiers, 29, 2 (1988) 

and

* H. Nishimura, _Supersmooth topoi_, International Journal of Theoretical Physics, Volume 39, Number 5 ([journal](http://www.springerlink.com/content/v2573726852x6470/))

