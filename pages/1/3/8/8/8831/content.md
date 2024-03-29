In [section 4](http://arxiv.org/PS_cache/math/pdf/0502/0502155v2.pdf#page=11)
of

* Clemens Berger, [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ ([arXiv](http://arxiv.org/abs/math.AT/0502155))

the following definition is given:

Let $H$ be a [[monoidal model category]] and write $pt$ for the tensor unit in $H$ (not necessarily the terminal object). 

A **[[segment object|segment (object)]]** $I$ in a [[monoidal model category]] $H$ is 

* a factorization 

  $$
    pt \amalg pt \stackrel{[0 , 1]}{\to} 
    I \stackrel{\epsilon}{\to} pt
  $$

  of the [[codiagonal morphism]]

  $$
    pt \amalg pt \stackrel{[Id , Id]}{\to} pt
  $$ 

  from the [[coproduct]] of $pt$ with itself that 
  sends each component identically to $pt$.

* together with an associative morphsim 

  $$
    \vee : I \otimes I \to I
  $$ 

  which has 0 as its _neutral_ and 1 as 
  its _absorbing_ element, and for which 
  $\epsilon$ is a counit.

If $H$ is equipped with the structure of a [[model category]] then a segment object is an **interval** in $H$ if 

$$
  [0, 1]\colon pt \amalg pt \to I
$$ 

is a cofibration and $\epsilon : I \to pt$ a weak equivalence.


The axioms of a segment are expressed by the commutativity of the following five diagrams (all isomorphisms being induced by the symmetric monoidal structure):

$$\array{
(H\otimes H)\otimes H&\to^\sim&H\otimes(H\otimes H)\\\downarrow^{\vee\otimes H}&&\downarrow_{H\otimes\vee}\\H\otimes H&\overset{\vee}{\leftarrow} H\overset{\vee}{\longleftarrow}&H\otimes H
}$$

$$\array{I\otimes H&\rightarrow^{0\otimes H}& H\otimes H&\leftarrow^{H\otimes 0}&H\otimes I\\&\searrow_\sim&\downarrow_\vee&\swarrow_\sim&\\&&H&&
}$$

$$\array{&&I\otimes H&\rightarrow^{1\otimes H}&H\otimes H&\leftarrow^{H\otimes 1}&H\otimes I&&\\&\swarrow^{I\otimes\epsilon}&\downarrow&&\downarrow_\vee&&\downarrow&\searrow^{\epsilon\otimes I}&\\I\otimes I&\rightarrow^\sim&I&\rightarrow^1&H&\leftarrow^1&I&\leftarrow^\sim&I\otimes I}$$

$$\array{H\otimes H&\rightarrow^{\epsilon\otimes\epsilon}&I\otimes I&\quad&I&\rightarrow^0&H\\\downarrow^\vee&&\downarrow_\sim&\quad&\downarrow_1&\searrow^{id}&\downarrow_\epsilon\\H&\rightarrow^\epsilon&I&\quad&H&\rightarrow^\epsilon&I}$$
