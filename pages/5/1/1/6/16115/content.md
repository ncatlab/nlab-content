
A __Pythagorean triple__ is an [[integer|integral]] solution $(a, b, c)$ to the [[Diophantine equation]] $a^2 + b^2 = c^2$. For example, $(3, 4, 5)$ is a solution. 

Dividing through by $c^2$, the solution set may be described in terms of _[[rational number|rational]]_ solutions to $x^2 + y^2 = 1$. This is a smooth [[conic]] and can be parametrized by the [[projective line]] $\mathbb{P}^1(\mathbb{Q})$ by means of [[stereographic projection]]. Specifically, by stereographically projecting from the point $(-1, 0)$ on the conic to the projective line $x = 1$ (in the [[projective space|projective plane]]), each rational solution $(r, s)$ is taken to a point with rational coordinate $t = \frac{2 s}{1 + r}$. In the other direction, given a rational point $(1, t)$, the line connecting this to $(-1, 0)$ indeed intersects the conic in two rational points (or a double point if $t = \infty$), viz. $(-1, 0)$ and $(r = \frac{4 - t^2}{4 + t^2},\; s = \frac{4 t}{4 + t^2})$, or more recognizably, $(\frac{1 - t'^2}{1 + t'^2},\; \frac{2 t'}{1 + t'^2})$ if $t' = t/2$. 

In this way all rational solutions are accounted for. Putting $t' = \frac{u}{v}$ for integers $u, v$, this shows that any integral solution to $a^2 + b^2 = c^2$ is of the form $a = v^2 - u^2$, $b = 2 v u$, $c = v^2 + u^2$ (up to reordering $a$ and $b$, obviously). 


[[!redirects Pythagorean triple]]
[[!redirects Pythagorean triples]]
