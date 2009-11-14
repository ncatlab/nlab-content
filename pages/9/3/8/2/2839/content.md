In [[algebraic topology]] a cocylinder is a dual construction to a cylinder or a [[cylinder object|mapping cylinder]].

The cocylinder $Cocyl(X)$ of a space $X$ is simply the path space $X^I$, see entry [[path object]]. The terminology is however rather used in its extension to the mappings where the path terminology is less often used: a **(mapping) cocylinder** of a continuous map $f:X\to Y$ is the pullback
$$\array{
Cocyl(f)&\to& X\\
\downarrow&&\downarrow f \\
Y^I&\stackrel{ev_0}{\to}&Y
}$$
where $Y^I$ is the path object. In other words,
that is the subspace $Cocyl(f)\subset Y^I\times X$ whose elements are pairs $(s,x)$ such that $s(0)=f(x)$. For a usage see [[Hurewicz connection]]. George Whitehead in his old book "Elements of homotopy theory" instead uses the terminology *mapping path space* with notation $M_f Y$. In Brown's theory of higher stacks via categories of fibred objects, mapping cocylinders take a role of total spaces of a relative version universal principal bundles associated to map $f$; the projection of such a bundle is the composition $Cocyl(f)\to Y^I\stackrel{ev_1}\to Y$. Note that the other leg $ev_1$ is used here. 

If we interchanges $ev_0$ and $ev_1$ then we have an upside-down version of a cylinder, sometimes called inverse (or inverted) mapping cocylinder; but usually it is clear just from the context which version is used. 

[[!redirects mapping cocylinder]]