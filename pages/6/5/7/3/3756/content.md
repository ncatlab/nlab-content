##Discussion

[[Eric]]: Here is a degenerate loop:
$$\array{
X & \stackrel{e}{\to} & X \\
{} & \mathllap{\scriptsize{e}}{\nwarrow} & \darr\scriptsize{e} \\
{} & {} & X
}$$

To say this loop commutes, is to say $e^3 = 1_X$. Or is it?

>[[David Roberts]]: That is correct.

[[Eric]]: Since this loop is degenerate, we may or may not have (depending on convention?), parallel identity arrows running between each vertex.

If there are hidden identity morphisms, then to say the triangle commutes is to say $e = 1_X$.

>[[David Roberts]]: No: the above version $e^3 = id$ is correct.


[[Eric]]: Here is a degenerate triangle:

$$\array{
X & \stackrel{e}{\to} & X \\
{} & \mathllap{\scriptsize{e}}{\searrow} & \darr\scriptsize{e} \\
{} & {} & X
}$$

To say this triangle commutes is to say $e^2 = e$. Or is it?

>[[David Roberts]]: That is correct.

[[Eric]]: Since this triangle is degenerate, we may or may not have (depending on convention?), parallel identity arrows running between each vertex.

If there are hidden identity morphisms, then to say the triangle commutes is to say $e = 1_X$.

[[David Roberts]]: No: the above version $e^2 = e$ is correct. For both of these wrong statements, you are assuming that arrows somehow cancel. Especially the first one, think of it in terms of dimensional analysis. If you have a quantity in physics with dimensions of something else cubed, it cannot have the dimensions of that original thing (unless both are dimensionless). But this is only a rough analogy, please don't read anything deep into it. In my comment in reply to Harry's $e^2 = e$ being a loop, then I said I would draw this as a commuting triangle. I wouldn't draw a loop (i.e. an endomorphism) (resp. a degenerate loop) as a triangle (resp. commuting triangle) in any circumstances, because we are not given that the loop factors into a composite of other arrows.

[[Eric]]: Thanks David. I think I've managed to boil it down to the basic disagreement. It is about "shape dependence". I reject the notion of shape dependence. The morphism $f:X\to X$ is a loop and this loop is the same as $f:X\righttoleftarrow$. I [explain this](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=332&Focus=7368#Comment_7368) on the n-Forum. The point is, you can accept shape dependence, in which case I agree with everything you say. Or you reject shape dependence and work with semidiagrams instead.

+-- {: .query}
I don\'t think that there\'s any doubt that $e^2 = e$ is the intended interpretation of the second diagram by everybody who uses commutative diagrams.  The fact that the same object $X$ shows up twice is irrelevant; the whole point of putting $X$ in there twice is because you *don\'t* want parallel identity arrows.  Of course, you can invent an alternative interpretation if you want, but I don\'t think that you\'ll find any usage to match it in the wild.  ---Toby
=--

##Main Article

A stub for now.

The basic goal of this page is to turn Domenico's and Urs' statements about connections into statements about commutative diagrams.

The rough is idea is:

$$\text{Higher Connection Flat}\quad\quad\simeq\quad\quad\text{Higher Diagram Commutes}$$

+--{.standout}
[Domenico](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=723&Focus=5015#Comment_5015): I guess this is well known, but let me try writing it here and see what happens.

If a connection on a principal G-bundle is locally represented by the 1-form $\omega$ with values in $\mathfrak{g}$, then the connection is flat if and only if the curvature 2-form $F=d\omega+\frac{1}{2}[\omega,\omega]$ vanishes, that is, if $\omega$ is a solution of the Maurer-Cartan equation.

Now, what is interesting is that one can see curvature only on 2-dimensional paths (it is a 2-form): if one restricts $\omega$ to a 1-dimensional submanifold, then there $\omega$ is clearly a solution to the Maurer-Cartan equation. so, if I think of an infinitesimal 1-simplex and look at my connection there, I could say that my connection is 1-flat. then, moving to an infinitesimal 2-simplex I see that the connection is (generally) not 2-flat: holonomy along two sides of the 2-simplex is not the same thing as holonomy along the third side. not the same, but in a very precise way: the curvature $FF$ exactly measures the gap to go from a horn of the 2-simplex to the third edge. this is very 2-categorical, and suggests I could cure the lack of flatness of my original connection by adding a copy of $\mathfrak{g}$ in degree -1 and cooking up a 2-Lie algebra $\mathfrak{l}$. Maurer-Cartan equation for this 2-Lie algebra would coincide with the original one one the 1-simplex (since only degree 1 elements are 1-forms with values in $\mathfrak{l}_0$. but on the 2-simplex we would have, in addition to these elements, also 2-forms with coefficients in $\mathfrak{l}_{-1}$, and the Maurer-Cartan equation on teh simplex would look like $d\omega+\frac{1}{2}[\omega,\omega]+\delta F=0$ where $\delta\colon \mathfrak{l}_{-1}\to \mathfrak{l}_{0}$ is the differential of the $L_\infty-algebra \mathfrak{l}$ (and it should be induced by the identity of $\mathfrak{g}$, thought as a degree 1 map from $\mathfrak{g}[-1]$ to $\mathfrak{g}$). So the original equation telling that $\omega$ had curvature $F$ is now equivalent to say that $\omega+F$ is flat.

in other words, what seemed a non-flat connection was so since I was not seeing the 2-bundle, but only a 1-bundle approximation. and on a 1-bundle I can only clearly see up to 1-simplices, wher my connection was actually flat.

once curvature has come in, we can repeat the argument: now we have a 2-flat connection and test it on the 3-simplex. if it has 3-curvature, that will presumibly be because we are not seeing the 3-bundle, yet. so I find it natural to wonder (to conjecture) whether any connection on a principal bundle (and more generally any $n$-flat connection on an n-bundle) can be seen as a flat connection on an $\infty$-bundle. 
=--

+--{.standout}
[Domenico](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=723&Focus=5050#Comment_5050): I think I could take the task of working a bit on oo-Lie algebroid valued forms in the direction sketched above. yet, I'd like to still discuss it a bit here, sicne I'm now thinking of some more radical change. what I'm thinking is that the one-step definition as it is now is too strict. I mean, we are now defining flat $\mathfrak{a}$-connections as a morphism $\prod^{inf}(X)\to\mathfrak{a}$, and then general connections as something which becomes flat in a single step, i.e., going from $\mathfrak{a}$ to $cone(\mathfrak{a}$). why should we restrict to this? it would be natural to consider thigs that become flat in 2 sterps, 3, steps, and so on. eventually we could have things which "become flat after infinity steps" (and by the way this vague notion seems to me to better fit with classical $\mathfrak{g}$-connections).

let us see things the other way round: when we say flat, we mean flat in an $\infty$-categorical sense, so let us stress this by saying that a morphism $\prod^{inf}(X)\to\mathfrak{a}$ is an $\infty$-flat connection with values in $\mathfrak{a}$. then, what we are currently calling non-necessarily-flat $\mathfrak{a}$-connections would be the $(\infty-1)$-flat connections with values in $\mathfrak{a}$. but starting from $\infty$ is not too practical.., let us start from 0 instead.

the one-step definition of non-flat connections is reflected in the one step going from the 0-groupoid $X$ to the $\infty$-groupoid $\prod^{inf}(X)$. but we have a whole tower of higher and higher groupoids in between: the $n$-skeleta of $\prod^{inf}(X)$. so we have

$$X=\prod^{inf}(X)_{(0)}\hookrightarrow \prod^{inf}(X)_{(1)}\hookrightarrow \prod^{inf}(X)_{(2)}\hookrightarrow \cdots \hookrightarrow \prod^{inf}(X)$$

and we can talk of an $n$-flat connection with values in $\mathfrak{a}$ as a morphism $\prod^{inf}(X)_{(n)}\to \mathfrak{a}$. this will not lift to a morphism $\prod^{inf}(X)_{(n+1)}\to \mathfrak{a}$ unless the connection is $(n+1)$-flat, but will lift to a morphism $\prod^{inf}(X)_{(n+1)}\to cone(\mathfrak{a})$. the limit of this procedure will produce a "true connection" with values in $cone(cone(\cdots(cone(\mathfrak{a}))\cdots)$.

I have a vague feeling that starting with a 0-falt $\mathfrak{o}(n)$-connection one will this way meet the series $\mathfrak{so}(n), \mathfrak{spin}(n), \mathfrak{string}(n), \mathfrak{fivebrane}(n), \mathfrak{uniray}(n)$,..., but I have to think more carefully to this. 
=--

##References

* n-Forum: [Is every connection flat?](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=723&page=1)
* n-Forum: [functor](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=332&Focus=7304#Comment_7304)
* Eric\'s web: [[ericforgy:Shape Dependence in Commutative Diagrams]]


[[!redirects Shape Dependence in Commutative Diagrams]]
