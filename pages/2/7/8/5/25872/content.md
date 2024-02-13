
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea

[Lavers (1997)](#Lavers97) introduced the [[monoid]] $V_n$ of *$n$-vines*,  whose elements are thought of as paths between two sets of $n$ distinct points in $\mathbb{R}^3$ which are allowed to merge into a single path, but not separate again. Some examples, from Lavers' original paper, are depicted below.

\begin{imagefromfile}
        "file_name": "vinesJPEG.jpg",
        "width": 300
    \end{imagefromfile}

Notice that $V_n$ is not a group because a general vine cannot be untangled to give the trivial vine which is $n$ paths straight down. However, via pre- and post-composition, the vine monoid is acted on by the [[braid group|braid group on $n$ strands]]. When two $n$-vines are composed any resulting strands which are only attached to one endpoint get retracted down to that endpoint, as in the following image (again from [Lavers 97](#Lavers97)):

\begin{imagefromfile}
        "file_name": "vinescompose.jpg",
        "width": 300
    \end{imagefromfile}

More generally, one can consider vines from $n$ points to $m$ points. As a result vines can be assembled into a category, as described below.


## Definition

What is called the *category of vines* is the [[free construction|free]] [[braided monoidal category|braided]] [[strict monoidal category]] containing a [[braided monoid]] (i.e. an [[E2-algebra|$E_2$-algebra]]). It is also the [[PRO|PROB]] for braided monoids.  

Concretely:

\begin{defn}
Let 

* $P_I \coloneqq \big\{ (i,0,1) \,\big\vert\, i=1, 2, \ldots, m \big\}$ 

* $P_T \coloneqq \big\{ (i,0,0) \,\big\vert\, i=1, 2, \ldots,n \big\}$ 

be [[linear order|linearly ordered]] collections of points in [[Cartesian space|$\mathbb{R}^3$]]. 

Then an *$(m,n)$-vine* is a set of arcs $\{v_1,\ldots,v_m\}$ (i.e. piecewise linear maps from $[0,1]$ to $\mathbb{R}^3$) with the following properties: 

1. $v_i(0)=(i,0,1)$, 

1. $v_i(1)\in P_T$, 

1. for all $h\in [0,1]$, $v_i(h)$ has $z$-coordinate $1-h$,

1. if $v_i(t)=v_j(t)$ for any $t\in (0,1]$ then $v_i(s)=v_j(s)$ for all $t\leq s\leq 1$. 

\end{defn}

\begin{defn}\label{CategoryV}
Let $\mathbb{V}$ be the category with set of [[objects]] the [[natural numbers]] with set of [[morphisms]] $\mathbb{V}(m,n)$ being $(m,n)$-vines modulo a suitable notion of ambient isotopy that allows arcs to be deformed up to homotopy but not pass through one another.
\end{defn}

##Properties

The [[monoidal category|monoidal structure]] of $\mathbb{V}$ is given by addition of [[natural numbers]] and juxtaposition of vines. Because $\mathbb{V}$ contains the [[braid category]] as a [[subcategory]], it cannot be [[symmetric monoidal]], but it is [[braided monoidal category|braided monoidal]]. The braiding is the same as that of the braid category, the "$m$-over-$n$" braid depicted below.

\begin{imagefromfile}
        "file_name": "braiding.jpg",
        "width": 300
    \end{imagefromfile}



\begin{exercise}
Show that the above is a braided monoidal structure on $\mathbb{V}$.
\end{exercise}



## References

* {#Lavers97} T. G. Lavers, *The theory of vines*, Comm. Algebra **25** 4 (1997) 1257–1284 &lbrack;[doi:10.1080/00927879708825919](https://doi.org/10.1080/00927879708825919)&rbrack;

* {#Weber2015}[[Mark Weber]], §6.3 of: _Internal algebra classifiers as codescent objects of crossed internal categories_. Theory and Applications of Categories, **30** 50 (2015) 1713–1792 &lbrack;[tac:30/50](http://www.tac.mta.ca/tac/volumes/30/50/30-50abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/30/50/30-50.pdf)&rbrack;



[[!redirects vines]]

[[!redirects vine monoid]]
[[!redirects vine monoids]]

[[!redirects vine category]]
[[!redirects vine categories]]





