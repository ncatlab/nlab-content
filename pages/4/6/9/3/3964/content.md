## Idea

A [[derivator]] is *pointed* if it has a [[zero object]] in the sense appropriate to a derivator.

## Definition

A derivator $D\colon Dia^{coop} \to Cat$ is **pointed**, or has a **zero object**, if each category $D(X)$ has a zero object.

By a "super-difficult" excercise in [Maltsionitis' notes](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf), this is equivalent to requiring that whenever $u\colon I\to J$ is a [[sieve]] in $Dia$, the functor $u_! \colon D(I) \to D(J)$ has a left adjoint $u^?$, and dually whenever $u$ is a cosieve, the functor $u_*$ has a right adjoint $u^!$.

## Loop and suspension

In a pointed derivator, we have a [[suspension]] functor $\Sigma\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{a_*}{\to} D \Gamma \overset{abc_!}{\to} D \square \overset{d^*}{\to} D 1$$
where $\square$ denotes the category
$$ \array{ a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d } $$
and $\Gamma$ its full subcategory on $\{a,b,c\}$.

...

[[!redirects pointed derivators]]
[[!redirects derivator with a zero object]]
[[!redirects zero object in a derivator]]
[[!redirects derivators with zero objects]]
[[!redirects zero objects in a derivator]]
