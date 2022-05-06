[[!redirects Natural transformation]]
[[!redirects Natural transformations]]
[[!redirects natural transformation]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Basic category theory
+--{: .hide}
[[!include Basic category theory content]]
=--
#### Category theory
+--{: .hide}
[[!include Category theory content]]
=--
=--
=--

\tableofcontents

##Definition##

* If $\mathbf{C}$ and $\mathbf{D}$ are two categories, then
the functors $\mathbf{C}\to \mathbf{D}$ are the objects of a category
$[\mathbf{C},\mathbf{D}]$ called the _functor category_.
A morphism $\alpha:F\to G$ between two functors 
$F, G:\mathbf{C} \to \mathbf{D}$ is called a _natural transformation_. 
It assigns to every _[object]_ $A\in \mathbf{C}$ a _[morphism]_ 
$\alpha_A:F A \to G A$ in $\mathbf{D}$ 
such that the following diagram commutes
\begin{xymatrix}
F A\ar[d]_{F(f)}\ar[r]^{\alpha_A}& G A \ar[d]^{G(f)} \\ F B \ar[r]^{\alpha_B}&G B
\end{xymatrix}
for every morphism $f:A \to B$ in $\mathbf{C}$.



We shall often write $\alpha:F\to G:  \mathbf{C}\to \mathbf{D}$
to indicate that $\alpha$ is a natural transformation between
two functors $\mathbf{C}\to \mathbf{D}$.  


The _composite_ of two natural transformations $\alpha:F\to G$ and $\beta:G\to H$ in the category $[\mathbf{C},\mathbf{D}]$
is the natural transformation $\beta \alpha:F\to H$ 
obtained by putting $(\beta\alpha)_A=\beta_{A}\alpha_A$
for every object $A\in \mathbf{C}$,
\begin{xymatrix}F A\ar[d]_{F(f)}\ar[r]^{\alpha_A}& G A \ar[d]^{G(f)} 
\ar[r]^{\beta_A}& H A \ar[d]^{H(f)} \\ 
F B \ar[r]^{\alpha_B}&G B\ar[r]^{\beta_B}&H B.
\end{xymatrix}





#### Remark

The category $[\mathbf{C},\mathbf{D}]$ is locally small if $\mathbf{C}$ is small and $\mathbf{D}$ locally small, in which
case we shall often denote it by $\mathbf{D}^{\mathbf{C}}$.
The category $\mathbf{D}^{\mathbf{C}}$ is small, if additionally $\mathbf{D}$ is small.


##Examples##




* Recall that a _[presheaf]_ on a small category $C$ is defined to be a [contravariant functor] $C\to \mathbf{Set}$, or equivalently
a covariant functor $C^o\to \mathbf{Set}$. If $X$ and $Y$ are presheaves on $C$, then a _map_  $X\to Y$ is defined to be a natural transformation $X\to Y$. The category of presheaves $[C^o,\mathbf{Set}]$ is locally small
and we shall denote it by $\mathbf{P}(C)$.

* Recall that a _[simplicial set]_ is defined to be a presheaf on the 
[simplicial category] $\Delta$. We shall denote the 
category of simplicial sets $\mathbf{P}(\Delta^o)$ by $\mathbf{SSet}$.  


* If $K\mathbf{Vect}$ is the category of 
$K$-vector spaces over a field $K$ and $G$ is a group,
then the functor category $[\mathbf{B}G,K\mathbf{Vect}]$ is the category of a $K$-linear _representations_ of $G$. 


* Let $I$ be the category defined by the poset $[1]=\{0,1\}$, and let $i$ be the unique arrow $0\to 1$. If $\mathbf{C}$ is a category,
then a functor $X:I\to \mathbf{C}$ 
the same thing as a morphism $x:X_0\to X_1$
in $\mathbf{C}$, where $X_0=X 0$, $X_1=X 1$ and $x=X(i)$.
If $Y:I\to \mathbf{C}$  is another morphism $y:Y_0\to Y_1$, then
a natural transformation $f:X\to Y$ is a commutative square
\begin{xymatrix}X_0\ar[d]_{x}\ar[r]^{f_0}& Y_0 \ar[d]^{y} \\ 
X_1 \ar[r]_{f_1} &Y_1
\end{xymatrix}
in the category $\mathbf{C}$.
The category $[I,\mathbf{C}]= \mathbf{C}^I$
is called the *arrow category* of $\mathbf{C}$. 



