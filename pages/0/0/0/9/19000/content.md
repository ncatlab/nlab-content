## Idea 

A Schwartz-Bruhat function is a certain type of complex-valued function on a general [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] [[topological abelian group|abelian group]], generalizing the familiar notion of [[Schwartz space|Schwartz function]] on a space given as a finite product of copies of the real line, of the circle, and a finitely generated abelian group. 

## Definitions 

The notion of Schwartz-Bruhat function is constructed in stages that parallel developments in the general structure theory of locally compact (Hausdorff) abelian groups. 

Recall the notion of *compactly generated topological group* $G$: it means there is a compact neighborhood of the identity which generates $G$ as a group. The structure of a compactly generated abelian Lie group is well-known: it is a product of type $K \times \mathbb{R}^m \times \mathbb{Z}^n$ where $K$ is a [[compact space|compact]] [[abelian group|abelian]] [[Lie group]] (thus of the form $T^p \times F$ where $F$ is a finite abelian group and $T = \mathbb{R}/\mathbb{Z}$ is a circle group). These are often called *elementary Lie groups*. 

+-- {: .num_defn #def1} 
###### Definition 
Let $G$ be an elementary Lie group of type $K \times \mathbb{R}^m \times \mathbb{Z}^n$ where $K$ is a compact abelian Lie group. A *Schwartz-Bruhat function* on $G$ is an [[smooth function|infinitely differentiable function]] $f: G \to \mathbb{C}$ that is *rapidly decreasing*: applications of any polynomial differential operator to $f$ is uniformly bounded in the $\mathbb{R}$- and $\mathbb{Z}$-variables, in the sense that 

$$
  \underset{\alpha \in \mathbb{N}^n}{\forall}\;\;
  \underset{\beta, \gamma \in \mathbb{N}^m}{\forall}\;\; \underset{K_{\alpha, \beta, \gamma} \gt 0}{\exists}\;
  \left(
  \underset{(j, x) \in \mathbb{Z}^n \times \mathbb{R}^m}{sup} {\Vert j^\alpha x^\beta \partial_{\gamma} f(x, j)  \Vert} \lt K_{\alpha, \beta, \gamma}
  \right)
$$

using the usual notations for multi-indices $\alpha, \beta, \gamma$. 
=-- 

Next, any locally compact abelian group is canonically a [[filtered colimit]] of the system of its open compactly generated subgroups and open inclusions between them. In particular, any abelian Lie group is canonically a filtered colimit of its open elementary Lie subgroups. In fact, an abelian Lie group is of the form $A \times \mathbb{R}^m \times T^p$, where $A$ is a discrete abelian group. We may reckon $A$ as a filtered colimit of its finitely generated subgroups $A_\alpha$; taking the product with the locally compact group $\mathbb{R}^m \times T^p$, any abelian Lie group is a filtered colimit of elementary Lie subgroups $A_\alpha \times \mathbb{R}^m \times T^p$. 

+-- {: .num_defn #def2} 
###### Definition 
A *Schwartz-Bruhat function* on an abelian Lie group $G$ is a continuous function $f: G \to \mathbb{C}$ that is supported on an open elementary Lie subgroup $H$, and whose restriction $f|_H: H \to \mathbb{C}$ is Schwartz-Bruhat in the sense of Definition \ref{def1}. (Thus $f$ is identically zero on the complement of $H$, which is a union of open cosets $g + H$.) 
=-- 

Let $\mathcal{S}(G)$ denote the [[topological vector space|TVS]] of Schwartz-Bruhat functions on an abelian Lie group $G$. We obtain a functor $\mathcal{S}(-): AbLie^{op} \to TVS$. 

Finally, the character group of a compactly generated locally compact abelian group is an abelian Lie group. By applying [[Pontryagin duality]] to the statement that a locally compact abelian group is canonically a filtered colimit of compactly generated subgroups, we see that any locally compact abelian group $G$ is canonically an inverse limit of a cofiltered diagram of abelian Lie groups $G_\alpha$: 

$$G \cong \underset{\longleftarrow}{\lim}_\alpha G_\alpha.$$

We may apply the contravariant functor $\mathcal{S}(-)$ to this cofiltered diagram to produce a filtered diagram of Schwartz-Bruhat spaces $\mathcal{S}(G_\alpha)$ of abelian Lie groups. In this notation, 

+-- {: .num_defn} 
###### Definition 
For a locally compact abelian group $G$, the Schwartz-Bruhat space $\mathcal{S}(G)$ is the colimit of the filtered diagram of spaces $\mathcal{S}(G_\alpha)$ defined according to Definition \ref{def2}. 
=-- 

In other words, a Schwartz-Bruhat function on $G$ is one that factors through one of its Lie quotients as 

$$G \twoheadrightarrow G_\alpha \stackrel{g}{\to} \mathbb{C}$$ 

where $g: G_\alpha \to \mathbb{C}$ is Schwartz-Bruhat in the sense given for Lie groups, Definition \ref{def2}. 

## References 

The extension of Schwartz functions and [[tempered distributions]] on Euclidean spaces $\mathbb{R}^n$ to more general locally compact abelian groups was given by Bruhat: 

* F. Bruhat, *Distributions sur un groupe localement compact et applications 
&agrave; l’&eacute;tude des repr&eacute;sentations des groupes p-adiques*, Bull. Soc. Math. France 89 (1961), 43-75. ([pdf](http://www.numdam.org/article/BSMF_1961__89__43_0.pdf))

References to the fact that Schwartz-Bruhat spaces can be presented as direct limits of [[topological vector spaces]] frequently appear in the literature, e.g., 

* A. Wawrzyńczyk, *On tempered distributions and Bochner-Schwartz theorem on arbitrary locally compact Abelian groups*, Colloquium Mathematicae Volume 19 Issue 2 (1968), 305-318. ([link](https://eudml.org/doc/263023)) 

(However, the precise categorical details seem to be hard to come by, or at least treated in somewhat cavalier fashion.)  

Some useful background material on the structure of locally compact Hausdorff abelian groups used in the description above can be found here: 

* Dikran Dikranjan, Luchezar Stoyanov, *An elementary approach to Haar integration and Pontryagin duality in locally compact abelian groups*, Topology and its Applications 158 (2011), 1942–1961. ([pdf](https://ac.els-cdn.com/S0166864111002604/1-s2.0-S0166864111002604-main.pdf?_tid=b5b2e8fe-134e-11e8-b733-00000aab0f26&acdnat=1518809121_303788c33fd1d38a829198fb1dd2741a)) 



[[!redirects Schwartz-Bruhat functions]] 
[[!redirects Schwartz-Bruhat space]] 
[[!redirects Schwartz-Bruhat spaces]] 
