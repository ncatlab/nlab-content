#Idea#

$L_\infty$-algebras are a [[vertical categorification]] of Lie algebras: in an $L_\infty$-algebra the Jacobi identity is allowed to hold only up to higher coherent homotopy. 


#Definition#

The quickest definition is:

an $L_\infty$-algebra is a degree -1 coderivation 
$D : \vee V \to \vee V$ on the free graded co-commutatuive algebra $V$ generated from a $\mathbb{N}$-grade vector space $V$ such that $D^2 = 0$.

Using the fact that coderivations on free coalgebras are already fixed by their action on "cogenerators", i.e. by their preimage in $V$, one can decompose this $D$ into it $k$-ary components
$$
  D = D_1 + D_2 + D_3 + \cdots
  \,.
$$
In terms of these the condition $D^2 = 0$ is a somewhat complicated looking condition. In terms of this condition $L_\infty$-algebras had been originally conceived.


#Special cases and generalizations#

* An $L_\infty$-algebra for which $V$ is concentrated in the first $n$ degree is a **Lie $n$-algebra**.

* An $L_\infty$-algebra in which only $D_n$ is nontrivial is an **$n$-Lie algebra**. But beware: in the literature on $n$-Lie algebras the condition that $D_n$ is of homogeneous degree -1 is often dropped.

+-- {: .query}
My, that is a profusion of terminology! So Lie $n$-algebras and $n$-Lie algebras are different. How about $L_n$-algebras? Has anybody introduced those?

_[[Urs Schreiber|Urs]] says:_ Yes, I am sure I have seen authors write $L_n$-algebra for Lie $n$-algebra: those authors who don't know/care about the higher categorical interpretation but take the $L_\infty$-algebra definition as the starting point. 

And, yes, it is a problem that there is so much different but equivalent terminology. Just recently, it has led to a huge industry of wheel-reinventing by string theorists. I have added references to that below.

=--

* The skew-symmetry of the Lie bracket is retained strictly in $L_\infty$-algebras. It is expected that weakening this, too, yields a more general [[vertical categorification]] of Lie algebras. For $n=2$ this has been worked out by Dmitry Roytenberg: [On weak Lie 2-algebras](http://arxiv.org/abs/0712.3461).

* The [[horizontal categorification]] of $L_\infty$-algebras are [[L-infinity-algebroid]]s.

#References#

The original references are:

* T. Lada and J. Stasheff,   Introduction to sh Lie algebras for physicists.  Int. J. Theo. Phys. 32, 1087-1103 (1993) ([arXiv](http://arxiv.org/abs/hep-th/9209099))

* Tom Lada, Martin Markl, _Strongly homotopy Lie algebras_ ([arXiv](http://arxiv.org/abs/hep-th/9406095))


A quick web entry is

* Marilyn Daily, [$L_\infty$-structures](http://www.aei.mpg.de/~md/hl.html).


The standard reference for Lie 2-algebras is

* [[John Baez]], Alissa Crans, _Higher-Dimensional Algebra VI: Lie 2-Algebras_ ([arXiv](http://arxiv.org/abs/math/0307263))

A discussion of $n$-Lie algebras (without the grading) and their relation to $L_\infty$-algebras is in

* A. S. Dzhumadil'daev, _Wronskians as $n$-Lie multiplications_ ([arXiv](http://arxiv.org/PS_cache/math/pdf/0202/0202043v1.pdf))


## Re-inventions of $n$-Lie algebras ##

The notion of $n$-Lie algebras, for $n=3$, was re-invented by string physicists in 

* Jonathan Bagger, Neil Lambert, _Gauge Symmetry and Supersymmetry of Multiple M2-Branes_ ([arXiv](http://arxiv.org/abs/0711.0955))

which sparked a tremendous amount of [activity](http://people.physik.hu-berlin.de/~ahoop08/klose.pdf). See the blog entry

* [Lie 3-Algebras on the Membrane](http://golem.ph.utexas.edu/category/2008/11/linfinity_algebras_on_the_memb.html)

for further details and links.

Further re-inventions of the concept in this context are appearing. The latest is 

* Tamar Friedman, _Orbifold singularities, the LATKe, and Yang-Mills with Matter_ ([arXiv](http://arxiv.org/abs/0806.0024))