Given a set $G$, an _$G$-graded vector space_ is a map $V$
assigning to each element $g \in G$ a [[vector space]] $V_g$.  Given $G$-graded vector spaces $V$ and $W$, a morphism $f : V \to W$ assigns to each element $g \in G$ a linear operator $f_g : V_g \to W_g$.

In other words, a $G$-graded vector space is a functor $V: G \to Vect$, where the set $G$ is treated as a [[discrete category]], and [[Vect]] is the category of vector spaces. Similarly, a morphism of $G$-graded vector spaces is a natural transformation between such functors.  In short, the category of $G$-graded vector spaces is the [[functor category]] $Vect^G$.  

People are usually interested in $G$-graded vector spaces when the set $G$ is equipped with extra structure.  If the set $G$ is a [[monoid]], $Vect^G$ is a [[monoidal category]].  If $G$ is a commutative monoid, $Vect^G$ is a [[symmetric monoidal category]].  If $G$ is a group, every finite-dimensional $G$-graded vector space has a [[left dual object|left dual]] and a [[right dual object|right dual]].  And if $G$ is an abelian group, these duals coincide.

By far the most widely-used examples are $G = \mathbb{Z}$ and $G = \mathbb{N}$.  Indeed, the term _graded vector space_ is often used to mean a $G$-graded vector space with one of these choices of $G$.  The case $G = \mathbb{Z}/2$ is also important: a $\mathbb{Z}/2$-graded vector space is also called a [[supervector space]]. However, in this case one often uses a different braiding on $\Vect^G$, one which uses the [[ring]] structure of $\mathbb N$; see [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Super_vector_space#The_category_of_super_vector_spaces).

It is also interesting to consider $G$-graded objects in other categories.  A _$G$-graded object_ in the category $C$ is a functor $F :G \to C$, and the category of $G$-graded objects in $C$ is the [[functor category]] $C^G$.

#Remarks#

For the case that $G$ is a group,
this means that the category of $G$-graded vector spaces is a [[vertical categorification|categorification]] of the [[category algebra|group algebra]] of $G$, where numbers are replaced by vector spaces. Recalling from the remark in [[category algebra]] that the group algebra of a group can be identified with the monoid of spans of the form
$$
  \array{
     && G
     \\
     & \swarrow && \searrow
     \\
     pt &&\Rightarrow&& pt
     \\ 
     & \searrow && \swarrow
     \\
     &&
     Vect
  }
\,,
$$
where $pt \to Vect$ goes to the ground field $k$,
the monoidal category of $G$-graded vector spaces can be identified with the monoid of spans of the form
$$
  \array{
     && G
     \\
     & \swarrow && \searrow
     \\
     pt &&\Rightarrow&& pt
     \\ 
     & \searrow && \swarrow
     \\
     &&
     2Vect
  }
  \,.
$$
Here $2Vect$ denotes some version of the category of 2-vector spaces with the property that the category $Vect$ is one of its objects and such that $End_{2Vect}(Vect) \simeq Vect$ (in analogy to how $End_{Vect}(k) \simeq k$) and $pt \to 2Vect$ maps to $Vect$. Possible choices for $2Vect$ is the 2-category of [[Kapranov-Voevodsky 2-vector space]]s or the bigger bicategory [[Bimod]] of algebras and [[bimodule]]s.

More details on this perspective on graded vector spaces are in [[schreiber:Nonabelian cocycles and their quantum symmetries]].

#Special case of $\mathbb{Z}$-graded vector spaces.#

{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
###### Lexicon

[[Tim Porter|Tim]]:
The case  $G = \mathbb{Z}$ serves as a base for many other applications of the same basic idea. It has some of its own 'traditional' terminology and structure that links it to [[differential object|differential objects]], so that a 'differential graded vector space' is a [[chain complex]] of vector spaces. I will use 'gvs' as an abbreviation for this sort of graded vector space and 'dgvs' for the differential form. (Of course, the theory easily adapts to handle graded modules over a ring, and with some restriction, to graded groups.) Basing algebras on dgvs gives differential graded algebras ([[dg-algebra]]) and so on.

I want to put here a sort of lexicon of some terms which are taken from a source on [[rational homotopy theory]]. 

This will, for the moment, be more or less 'as-is' from the source (except translating it from  the original French that is!), i.e. without too much editing. This means that there may be conflicts with other entries, which will need resolving later. Some links to other entries have been given but more could be made. There WILL initially be some duplication but that will be eliminated later on.

I have put this in the main area so as to encourage feedback and the identification of potential clashes of notation, terminology and conventions.  I have typed this in but do not like it in some of its terminology. (I am using a latex file from some years ago.) Once I have everything I have in my lexicon down in the nLab I hope we can make the entries  fit more closely to others.

The lexicon will be spread over a number of entries with links at least at the end of each. It will be a list of specialised vocabulary with definitions but not the motivational material that the usual entries attempt to provide. 
=--

#Lexicon#

**Note** With $\mathbb{Z}$-graded vector spaces (and sometimes with other examples as well), some authors work with a direct sum of the various vector spaces instead of using an indexed family.



**(Pre-)graded vector spaces**

 A _pre-$\mathbb{Z}$-graded vector space_ (pre-gvs) is a direct sum $V = \bigoplus_{p\in \mathbb{Z}} V_p$.  The elements of $V_p$ are said to be _homogeneous of degree $p$_.  If $x \in V_p$, write $|x| = p$. 

Sometimes it may be convenient to write $\bar{x} = (-1)^{|x|}x$ and $V_+ = \bigoplus_{p\gt 0}V_p$.  Another very useful piece of notation is $V^p = V_{-p}$.  In this case we will refer to an 'upper grading' with, in contrast, the other notation being a 'lower grading'.  These are merely for convenience and have little or no mathematical significance.



For the purposes of this lexicon:

A _graded vector space_ (gvs) is a positively or negatively graded pre-gvs that is either $V = \sum_{p\geq 0}V_p$ or $V = \sum_{p\leq 0}V^p$. (This effectively restricts from a $\mathbb{Z}$-grading to one over $\mathbb{N}$
 
We consider the field $k$ to be a pre-gvs with $(k)_0 = k$, and $(k)_p =0$ if $p\neq 0$.  We say $V$ is of _finite type_ if $dim(V_p) \lt \infty$ for all $p$.

A linear map $f :V\to W$ between pre-gvs is _of degree $p$_ if $f(V_q) \subseteq W_{p+q}$ for all $q$. (Note this may also occur as $f(V^q) \subseteq W^{q-p}$.)

A _morphism_ $f : V\to W$ is a linear map of degree zero. Pregraded vector spaces and the morphisms between them define the category ${pre GVS}$.

The set of all linear maps of degree $p$ from $V$ to $W$ will be denoted $Hom_p(V,W)$ and we set 

$$Hom(V,W) = \bigoplus_p Hom_p(V,W).$$

Of course, we now have two notations for the same object, ${pre GVS}(V,W) = Hom_0(V,W)$.

**Suspension**

If $r\in \mathbb{Z}$, the $r$-suspension of $V$ is given by $(s^r V)_n = V_{n-r}.$

We will need $s$, the 1-suspension, and $s^{-1}$ in particular.  Of course, $(s^{-1}V)_n = V_{n+1}$.  It is also useful to note $(s^r V)^p = V^{p+r}$. Again, of course, $s^r: V\to s^r V$ is an isomorphism of degree $-r$ having $s^{-r}$ as its inverse.

(This is the basic example of the **suspension functor** discussed in [[triangulated category]].)


**Duals**

The dual of a (pre-)gvs $V$ is $\#V$ defined by 

$$
  \begin{aligned}
     (\#V)_p &: = Hom_p(V,k)\\
             &\cong{Vect}(V_{-p},k)\\
	     &\cong\#(V_{-p})\\
	     & =\#(V^p).
\end{aligned}
$$

If $f : V\to W$ is of degree $|f|$, then its _transpose_
 
$$^t f : \#W \to \#V$$

is given by 

$$(^t f)(\psi)(x) = (-1)^{|f||\psi|}\psi f(x),$$

for $\psi \in \#W$ and $x\in V$.  Thus if 
$V\stackrel{f}{\to}W\stackrel{g}{\to}X$, then

$^t (g\circ f)   = (-1)^{|f||g|}(^t f\circ {}^t g).$}
In particular, for $f$ an isomorphism
$$( ^t f)^{-1} = (-1)^{|f|} ^t (f^{-1}).$$


**Duality**

Let $V$ be a gvs, by convention in the duality

$$\langle \quad ; \quad \rangle: V \leftrightarrow \#V,$$

we will usually assume $V$ is non-negatively graded (so $V = \bigoplus_{p\geq 0}V_p$), whilst the right hand side is non-positively graded.   

If $V$ is of finite type then $\#\#V \cong V$, of course. The suspension of the dual $s(\#V)$ can be identified with $\#(s^{-1}V)$ and similarly 
$s^{-1}(\#V) = \#s(V)$.  These identifications are via the rules:

$$\begin{aligned}
\langle s^{-1}z;su\rangle &= (-1)^{|z|} \langle z;u \rangle,\\
\langle s z;s^{-1}u  \rangle &= (-1)^{|z|+1}\langle z;u \rangle.\end{aligned}$$

This sign convention is needed to ensure that $s s^{-1} = id$.



**Tensor products**

The _tensor product_ of two pre-gvs, $V$ and $W$, is $V\otimes W$, where

$$(V\otimes W)_n = \bigoplus_{p + q = n}V_p\otimes W_q.$$

On morphisms

$$(f\otimes g) (v\otimes w) = (-1)^{|g||f|}(f(v) \otimes g(w))$$

and is of degree $|f| + |g|$.

In particular there is a natural injection $(\#V)\otimes (\#W) \to \#(V\otimes W)$, and this is an isomorphism if either $V$ or $W$ is of finite type.

{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
######Links to next part and other things:
A [[differential object]] in the category of gvs is a [[differential graded vector space]] or dgvs. This is just a [[chain complex]] or cochain complex.
=--

category: lexicon