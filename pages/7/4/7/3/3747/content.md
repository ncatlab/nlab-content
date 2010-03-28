+-- {: .standout}
The following is just moved from [[real number]]; it still neads to be cleaned up into a coherent article of its own.
=--


Consider an [[infinite sequence]] of $(x_1,x_2,x_3,\ldots)$ of [[rational numbers]] such that
$$ {|x_i - x_j|} \lt 1/i + 1/j $$
always holds.  Then we may interpret each $x_i$ as a rational number within $1/i$ of the true value of some real number $x$.  Two such sequences $x,y$ are considered [[equivalence|equivalent]] if
$$ {|x_i - y_j|} \lt 1/i + 1/j $$
always holds; then they represent the same real number.  Up to this equivalence, we can demand that the denominator of $x_i$ is always $i$ (or a factor of $i$), so that $x_i$ is $x$ rounded up or down to the nearest such rational number (in the chosen direction).

Similarly, consider an infinite sequence $(x_0,x_1,x_2,\ldots)$ of rational numbers such that
$$ {|x_i - x_j|} \lt 1/2^i + 1/2^j $$
always holds.  Then we may interpret each $x_i$ as a rational number within $1/10^i$ of the true value of some real number $x$.  Two such sequences $x,y$ are considered equivalent if
$$ {|x_i - y_j|} \lt 1/2^i + 1/2^j $$
always holds.  Up to this equivalence, we can demand that the denominator of $x_i$ is always $10^i$ (or a factor of $10^i$), so that $x_i$ is $x$ rounded up or down to the nearest such rational number (in the chosen direction), that is the nearest rational number with $i$ decimal digits (at most) after the decimal point.

More generally (or a priori more generally), given any __modulus__ $(\alpha_0,\alpha_1,\alpha_2,\ldots)$, which is an infinite sequence of positive rational numbers that diverges to infinity, a __regular Cauchy equivalence__ with modulus $\alpha$ is an infinite sequence $(x_0,x_1,x_2,\ldots)$ such that
$$ {|x_i - x_j|} \lt 1/\alpha_i + 1/\alpha_j $$
always holds.  Two such sequences $x,y$ are __regular equivalent__ with modulus $\alpha$ if
$$ {|x_i - y_j|} \lt 1/\alpha_i + 1/\alpha_j $$
always holds.  The previous examples are simply regular Cauchy sequences with modulus $(1,2,3,\ldots)$ or $(1,2,4,\ldots)$, with the appropriate notion of equivalence.

More generally still, given any modulus as above, a __modulated Cauchy sequence__ with modulus $\alpha$ is an infinite sequence $(x_0,x_1,x_2,\ldots)$ such that
$$ {|x_i - x_j|} \lt 1/\alpha_{\min(i,j)} $$
always holds.  Two such sequences $x,y$ are __modulated equivalent__ with modulus $\alpha$ if
$$ {|x_i - y_j|} \lt 2/\alpha_{\min(i,j)} $$
always holds.  Every regular Cauchy sequence with a given modulus is a modulated Cauchy sequence with the same modulus.

Instead of fixing a modulus and considering all infinite sequences satisfying this condition for that modulus, we might consider all moduli at once.  Two modulated Cauchy sequences (possibly with different moduli) will now be considered equivalent in that equivalence is given by *any* modulus.

Most generally of all, we need not specify the modulus as an actual function from $\mathbb{N}$ to $\mathbb{Q}$ but instead demand that, for each positive rational number $N$ (no matter how large), there exists a [[natural number]] $k$ such that
$$ {|x_i - x_j|} \lt 1/N $$
whenever $i,j \geq k$.  In other words, we consider a __[[Cauchy sequence]]__ of rational numbers.  Similarly, we consider two such sequences __equivalent__ if, for each $N$, there exists $k$ such that
$$ {|x_i - y_i|} \lt 1/N $$
whenever $i \geq k$.

In weak [[foundations]] (including internally to a [[topos]], or even a $\Pi$-[[Pi-pretopos|pretopos]], with [[natural numbers object]]), we can fix any modulus $\alpha$ and then prove that every modulated Cauchy sequence is equivalent to a regular Cauchy sequence with modulus $\alpha$, and also prove that any two modulated Cauchy sequences with given modulus are modulated equivalent if they are equivalent by any modulus (and regualar equivalent if they are also regular).  Thus all the constructions of real numbers in this vein are equivalent if they involve moduli at all.

We would also like to prove that every Cauchy sequence is equivalent to a modulated one, that any two equivalent Cauchy sequences are modulated equivalent, and that any Dedekind real number is represented by a Cauchy sequence.  Each of these results is equivalent to a weak form of [[countable choice]] that also follows from [[excluded middle]].  Thus, almost any foundation used in practice proves these results, but they fail in many [[sheaf topos|sheaf topoi]].  When a distinction must be made, the real numbers represented by modulated Cauchy sequences are called __Cauchy reals__.

We can also use [[nets]] instead of sequences.  In that case, we have that every Dedekind real may be represented by a Cauchy net that is modulated by a net, and that this is unique up to an equivalence modulated by a net, even in weak foundations (in particular, in any $\Pi$-pretopos).  This still will not allow us to fix a modulus in advance, however.


[[!redirects Cauchy real number]]
[[!redirects Cauchy real numbers]]
[[!redirects Cauchy real]]
[[!redirects Cauchy reals]]
[[!redirects Cantor real number]]
[[!redirects Cantor real numbers]]
[[!redirects Cantor real]]
[[!redirects Cantor reals]]
