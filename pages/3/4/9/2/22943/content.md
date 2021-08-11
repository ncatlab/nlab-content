
# Wheels
* table of contents
{: toc}

## Idea

A wheel is an algebraic concept similar to a [[field]] but in which division is *always* defined, even division by zero.  This naturally requires modifications to the usual axioms.  Every [[commutative ring]] gives rise to a wheel using a simple modification of the construction of the [[field of fractions]], although there are other examples.

The terminology 'wheel' comes from the example of the wheel of [[real numbers]], which geometrically consists of a circle (the circle of [[extended real numbers]]) together with an additional point (thought of as the spoke of the wheel), thus looking like $\odot$.


## Notation

In elementary algebra, it\'s traditional to write $-x$ for the opposite (or additive inverse) of $x$, although one could write $0 - x$ (or perhaps $-1x$, meaning $-1 \cdot x$) instead.  This overloads the symbol $-$, with one meaning as a unary operator and another as a binary operator, related since $y - x = y + (-x)$.  However, it is *not* common to write $/x$ for the reciprocal (or multiplicative inverse) of $x$, but only to write $1/x$ (or perhaps $x^{-1}$) instead.  But it would work just as well to overload the symbol $/$, again with one meaning as a unary operator and another as a binary operator, related since $y/x = y \cdot /x$.

In a wheel, the unary operator $/$ is a fundamental part of the structure, and the binary $/$ is only defined using it.  Although it remains true that $y/x = y \cdot /x$, so that we could reasonably write $1/x$ instead of $/x$, this puts the emphasis the wrong way.  And while we could probably write $x^{-1}$ instead of $/x$, this is dangerous, since it\'s not true that $/x$ is always the multiplicative inverse of $x$ in a wheel.  (But for that matter, $-x$ is not always the additive inverse of $x$ in a wheel, even though we can still write it, and indeed define it, as $-1 \cdot x$, when this makes sense.)

If we write multiplication as juxtaposition, then $y /x$ is naturally interpreted as $y \cdot /x$, and so rather than think explicitly of the derived binary operation $/$, it\'s best to think of $y /x$ as always meaning $y \cdot /x$.  So only the unary version of $/$ really matters.  But notice that $/x y$ means $/x \cdot y$, not $/(x y)$ (which is different, and in fact equal to $/x \cdot /y$, or $/x /y$ for short).  So we are coming down on the side of $8 /2 (2 + 2) = 16$ in the great PEMDAS debate.


## Definition

A __wheel__ consists of an [[underlying set]] $W$ equipped with two binary operations written with any common notation for addition and multiplication, a unary operation written with $/$ as a prefix (called the reciprocal), and two constants $0$ and $1$, such that:

* Addition and multiplication are each associative and commutative, with $0$ and $1$ (respectively) as identities;
* The reciprocal is an [[involution]]: $//x = x$;
* Reciprocals get along with multiplication: $/(x y) = /x /y$ and $/1 = 1$;
* Multiplication sort of distributes over addition, but not quite: neither $0 x$ nor $(x + y) z$ can be simplified in general, but instead we have $(x + y) z + 0 z = x z + y z$;
* An axiom that would imply that reciprocals are multiplicative inverses if distributivity held: $(x + y z) /z = x / z + y + 0 z$;
* Special properties of $0$ that are needed since distributivity doesn\'t hold: $0 0 = 0$, $(x + 0 y) z = x z + 0 y$, and $/(x + 0 y) = /x + 0 y$; and
* Although $0 /0$ doesn\'t simplify, it\'s an [[absorbing element]] for addition: $0 /0 + x = 0 /0$.

Although these rules are somewhat odd, we need some unusual behaviour to prevent a wheel from collapsing to a triviality via $0 = 0 x = 0 /0 x = 1 x = x$.  In fact, only the last step is generally valid in a wheel.  The paradigmatic example is the wheel of fractions of a commutative ring, for which all of the axioms are easily checked, but for which simpler (invalid) statements have counterexamples.

We can generalize the quasi-distributive rule beyond two terms as
$$ (\sum_{i=1}^n x_i) y + \sum_{i=1}^{n-1} (0 y) = \sum_{i=1}^n (x_i y) .$$
That is, to multiply $y$ by the sum of $n$ terms, you need to add in $n-1$ copies of $0 y$ as well, and then the result is the sum of $n$ products.

Wheels are like [[rigs]] in that there is generally no notion of subtraction.  However, if the wheel happens to have a (necessarily unique) additive inverse of $1$, we may write it as $-1$, define $-x$ as $-1 x$, and define $y - x$ as $y + -x$.  But notice that $-x$ is *not* in general an additive inverse of $x$; rather, we have $x - x = 0 x + 0 x$ (using the modified general form of distributivity).

It is common to write $/0$ as $\infty$ and $0 \infty$ as $\bot$.


## Examples

The original example is the __wheel of real numbers__, denoted $\mathbb{R}^\odot$.  An element of $\mathbb{R}^\odot$ is an equivalence class of pairs of real numbers under a certain equivalence relation.  Morally, $(a,b)$ and $(c,d)$ are set equivalent iff $a d = b c$; however, this is not quite right, because it makes $(0,0)$ equivalent to every other pair (and so it\'s not even transitive).  So we additionally require that $(a,b) \ne (0,0)$ iff $(c,d) \ne (0,0)$, so that $(0,0)$ is actually equivalent only to itself.  We may write the equivalence class of $(a,b)$ as $a/b$, but let\'s write it as $a : b$ instead until we\'ve established what $a /b$ means in $\mathbb{R}^\odot$.  Now, we can define addition and multiplication in the usual way for fractions: $(a : b) + (c : d) \coloneqq (a d + b c) : (b d)$ and $(a : b) (c : d) \coloneqq (a c) : (b d)$.  Reciprocals are immediate: $/(a : b) \coloneqq b : a$.  The identities $0$ and $1$ in $\mathbb{R}^\odot$ are $0 : 1$ and $1 : 1$ respectively.  More generally, any real number $a$ gives us an element $a : 1$ of $\mathbb{R}^\odot$.  This function from $\mathbb{R}$ to $\mathbb{R}^\odot$ is one-to-one and respects addition and multiplication; it also respects reciprocals in that $/(a : 1) = (1/a) : 1$ if $a \ne 0$.  Now we\'re justified in writing $a /b$ for $a : b$.  We also write $\infty$ for $1 : 0$ and $\bot$ for $0 : 0$; these are the only elements of $\mathbb{R}^\odot$ that don\'t come from $\mathbb{R}$.  We have $x + \infty = \infty$ whenever $x \ne \infty, \bot$, while $\infty + \infty = \bot$ and $x + \bot = \bot$ always; and $\infty x = \infty$ whenever $x \ne 0, \bot$, while $0 \infty = \bot$ and $\bot x = \bot$ always.  In particular, $-\infty = \infty$, and $-\bot = \bot$.  Of course, $/0 = \infty$ and $/\infty = 0$, while $/\bot = \bot$.  Then $x - x = 0$ whenever $x \ne \infty, \bot$, while $\infty - \infty, \bot - \bot = 0$; and $x/x = 1$ whenever $x \ne 0, \infty, \bot$, while $0/0, \infty/\infty, \bot/\bot = \bot$.  Fortunately, $x + 0 = x$ and $1 x = x$ remain true always.  One way to think of all of this is that we are using the usual arithmetic on the version of the [[extended real numbers]] in which $\infty = -\infty$ (the [[projective line]]), but whenever the result is undefined, we take it to be $\bot$ (and any calculation involving $\bot$ stays $\bot$, as in [[domain theory]]).


## References

* Jesper Carlström (2001). _Wheels: On Division by Zero._ [Web](https://www2.math.su.se/reports/2001/11/).


[[!redirects wheel]]
[[!redirects wheels]]
