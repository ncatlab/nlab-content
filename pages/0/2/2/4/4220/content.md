
# The quadratic formula
* table of contents
{: toc}

## Idea

Consider the equation
\[ \label{eqn} a x ^ 2 + b x + c = 0 ,\]
which we wish to solve for $x$.


## Discussion

The coefficients $a,b,c$ are commonly taken from an [[algebraically closed field]] $K$ of [[characteristic]] $0$, such as the field $\mathbb{C}$ of [[complex numbers]], although any quadratically closed field whose characteristic is not $2$ would work just as well.  Alternatively, the coefficients can be taken from a [[real closed field]] $K$, such as the field $\mathbb{R}$ of [[real numbers]]; then the solutions belong to $K[\mathrm{i}]$.  (Note that $\mathbb{R}[\mathrm{i}]$ is simply $\mathbb{C}$ again.)  More generally, starting from any [[integral domain]] $K$ whose characteristic is not $2$, the solutions belong to some [[splitting field]] of $K$.  (Of course, there are solutions in *some* splitting field, regardless of the characteristic, but they are not given by the quadratic formula.)

Explicitly, the solutions of (eq:eqn) may be given by the __usual quadratic formula__
\[ \label{usual} x_\pm = \frac { - b \pm \sqrt { b ^ 2 - 4 a c } } { 2 a } ,\]
which works as long as $a \ne 0$.  There is also an __alternate quadratic formula__
\[ \label{alt} x_\pm = \frac { 2 c } { - b \mp \sqrt { b ^ 2 - 4 a c } } ,\]
which may be obtained from (eq:usual) by rationalising the numerator; this works as long as $c \ne 0$.  (Note that $\pm$ and $\mp$ appear here simply to indicate the two [[square roots]] of the determinant $b^2 - 4 a c$ and how they correspond to the two solutions $x_\pm$; we do not need to have a [[function]] $\sqrt{}$ which always chooses a 'principal' square root.)

These two formulas are reconciled in the [[projective line]] of $K$.  As long as $(a,b,c) \ne (0,0,0)$, there are two solutions (which might happen to be equal) in the projective line.  If $a = 0$, then one of these solutions is $\infty$, and (eq:usual) correctly gives us that solution (as long as $b \ne 0$) for one choice of square root, although it gives $0/0$ for the other choice.  Similarly, (eq:alt) correctly gives us $x = 0$ when $c = 0$ and $b \ne 0$, but it does not give us the other root when $c = 0$.  Note that if $a,c = 0$ but $b \ne 0$, then (eq:usual) gives us one root ($\infty$) while (eq:alt) gives us the other ($0$).

So in general, we should be given $a \ne 0$, $b \ne 0$, or $c \ne 0$ for a nondegenerate equation (eq:eqn).  If $a \ne 0$, then we use (eq:usual); if $c \ne 0$, then we use (eq:alt).  Finally, if $b \ne 0$, then we use both; each root will be successfully given by at least one formula for some choice of square root of $b^2 - 4 a c$.

When the coefficients come from an [[ordered field]] $K$ (which we assume real closed), then we can write down a formula specially for the case when $b \ne 0$.  This is the __numerical analysts\' quadratic formula__
\[ \label{numanal} \begin {gathered}
   x_{\hat{b}} = \frac { 2 c } { - b - \hat{b} \sqrt { b ^ 2 - 4 a c } } ;\\
   x_{-\hat{b}} = \frac { - b - \hat{b} \sqrt { b ^ 2 - 4 a c } } { 2 a } .\\
\end {gathered} \]
In this formula, $\hat{b}$ is the sign of $b$, that is ${|b|}/b$; also, we must choose a nonnegative principal square root, so that $\sqrt{b^2 - 4 a c} \lt 0$ in $K$ is avoided (and thus the common denominator of $x_{\hat{b}}$ and numerator of $x_{-\hat{b}}$ is nonzero even if not imaginary).  Despite the name, this formula is not sufficient for all purposes in [[numerical analysis]]; one still needs all three formulas and chooses between them based on whether $a \ne 0$, $b \ne 0$, or $c \ne 0$ is best established.

There is also an interesting issue about whether $b^2 - 4 a c \ne 0$.  Everything above is valid in weak forms of [[constructive mathematics]], except for the statement that $\mathbb{C}$ is algebraically closed.  That claim follows from [[weak countable choice]] (WCC), which in turn will follow from either [[excluded middle]] or [[countable choice]], which is accepted by most constructive mathematicians.  Nevertheless, the statement
$$ \forall a , b , c \colon \mathbb{C} , \; \exists r \colon \mathbb{C} , \; r ^ 2 = b ^ 2 - 4 a c $$
is false in (for example) the [[internal language]] of the [[sheaf topos]] over the [[real line]].  (Essentially, this is because there is no [[continuous map]] $\sqrt{}$ on any neighbourhood of $0$ in $\mathbb{C}$.)  If we are given that $a,b,c$ are real, or if we are given that $b^2 \ne 4 a c$, then there is no problem.  But in general, we cannot define this square root, which appears in every version of the quadratic formula.

However, there is a more subtle sense in which $\mathbb{C}$ is algebraically closed even without WCC; essentially, this allows us to approximate the [[subset]] of $\mathbb{C}$ whose elements are the two solutions of (eq:eqn) (using two-element subsets of the field of, say, [[Gaussian number]]s) even if we can\'t approximate any one solution (using individual, say, Gaussian numbers).  See [Richman (1998)](#Richman) for details.

Sometimes one considers the equation
$$ a x ^ 2 + 2 p x + c = 0 $$
instead of (eq:eqn); then (eq:usual) simplifies to
$$ x _ \pm = \frac { - p \pm \sqrt { p ^ 2 - c } } a .$$
This is valid even in characteristic $2$, but unfortunately then it is fairly useless, since $2 p = 0$.  In fact, (eq:eqn) is [[solvable group|solvable]] in characteristic $2$ only if $b = 0$.


## References

*  [[Fred Richman]]; 1998; _The fundamental theorem of algebra: a constructive development without choice_; [Fred Richman's Documents](http://math.fau.edu/richman/HTML/DOCS.HTM)
{#Richman}


[[!redirects quadratic formula]]
[[!redirects quadratic formulas]]
[[!redirects quadratic formulae]]
[[!redirects quadratic formulæ]]
