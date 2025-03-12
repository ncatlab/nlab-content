
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Invariant theory_ studies _[[invariant|invariants]]_: algebraic entities -- for instance elements in a [[ring]] -- invariant under some [[group]] [[action]]. 

In _[[geometric invariant theory]]_ one regards the algebraic objects as [[Isbell duality|formally dual]] to a geometric space and interprets the invariants as functions on a [[quotient]] space.

## Examples
 {#Examples}

Let $V$ be a ([[graded vector space|graded]]) [[vector space]] equipped with the [[action]] $\rho$ of a [[group]] $G$. This induces an action on the symmetric [[tensor powers]] $Sym^n V$. A [[linear map]] out of sums of such symmetric powers is called a [[polynomial]] on $V$. It is an _[[invariant polynomial]]_ if it is invariant under the group action, hence if for every $g \in G$ we have (writing it for a homogeneous polynomial for convenience)

$$
  f(\rho_g(x_1), \cdots, \rho_g(x)) = f(x_1, \cdots, x_n)
  \,.
$$ 

For instance if $G$ is a [[Lie group]] and $V = \mathfrak{g}$ is its [[Lie algebra]], there is a canonical _[[adjoint action]]_ $\rho = Ad$ of $G$ on $Sym^n \mathfrak{g}$. The corresponding _[[invariant polynomials]]_ play a central role in [[Lie theory]], notably via [[Chern-Weil theory]]. 
In this case the $Ad$-invariance is often expressed in its differential form (obtained by differentiating the above equation at the neutral element), where it says that for all $y \in \mathfrak{g}$ we have

$$
  f([y,x_1], \cdots, x_n) + \cdots + 
  f(x_1, \cdots, [y,x_n])
  = 0
  \,.
$$

## Related concepts

* [[invariant]], [[group averaging]], [[logicality and invariance]]

## References

* Jean Dieudonn&#233;, James B. Carrell, _Invariant theory, old and new_, Advances in Mathematics 4 (1970) 1-80. Also published as a book (1971).
* Hanspeter Kraft, [[Claudio Procesi]], _Classical invariant theory -- A primer_ ([pdf](https://www.math.iitb.ac.in/~shripad/Wilberd/KP-Primer.pdf))
* [[Claudio Procesi]], _Lie groups, an approach through invariants and representations_, Universitext, Springer 2006, [gBooks](http://books.google.co.in/books?id=Sl8OAGYRz_AC&printsec=frontcover&hl=hr&source=gbs_atb)
* [[Igor Dolgachev]], _Lectures on invariant theory_, [ps](http://modular.math.washington.edu/people/dolgachev/invbook.ps)

* William Crawley-Boevey, _Lectures on representation theory and invariant theory_ ([pdf](www.amsta.leeds.ac.uk/~pmtwc/repinv.pdf))

* [[David Mumford]], John Fogarty, Frances Clare Kirwan, _Geometric invariant theory_, Ergebnisse der Mathematik und ihrer Grenzgebiete (2) __34__, Springer-Verlag

* Hanspeter Kraft, _Geometrische Methoden in der Invariantentheorie_, Aspects of Mathematics, D1. Friedr. Vieweg & Sohn, Braunschweig, 1984. x+308 pp. 

* &#1069;. &#1041;. &#1042;&#1080;&#1085;&#1073;&#1077;&#1088;&#1075;, &#1042;. &#1051;. &#1055;&#1086;&#1087;&#1086;&#1074;, _&#1058;&#1077;&#1086;&#1088;&#1080;&#1103; &#1080;&#1085;&#1074;&#1072;&#1088;&#1080;&#1072;&#1085;&#1090;&#1086;&#1074;_, &#1048;&#1090;&#1086;&#1075;&#1080; &#1085;&#1072;&#1091;&#1082;&#1080; &#1080; &#1090;&#1077;&#1093;&#1085;. &#1057;&#1077;&#1088;. &#1057;&#1086;&#1074;&#1088;&#1077;&#1084;. &#1087;&#1088;&#1086;&#1073;&#1083;. &#1084;&#1072;&#1090;. &#1060;&#1091;&#1085;&#1076;&#1072;&#1084;. &#1085;&#1072;&#1087;&#1088;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1103;, 1989, &#1090;&#1086;&#1084; 55, &#1089;. 137&#8211;309 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=intf&paperid=158&what=fullt&option_lang=rus)

* [[B. Kostant]], S. Rallis, _Orbits and representations associated with symmetric spaces_, Amer. J. Math. __93__ (1971), 753&#8211;809 [MR0311837](http://www.ams.org/mathscinet-getitem?mr=0311837) [doi](http://dx.doi.org/10.2307/2373470)

* [[Edward Formanek]], _Noncommutative invariant theory_, in: Group actions on rings (Brunswick, Maine, 1984), 87&#8211;119, Contemp. Math. 43, Amer. Math. Soc. 1985 [doi](http://dx.doi.org/10.1090/conm/043)

* [[Peter Olver]]: *Classical Invariant Theory*, Cambridge University Press (1999) &lbrack;[doi:10.1017/CBO9780511623660](https://doi.org/10.1017/CBO9780511623660)&rbrack;



[[!redirects classical invariant theory]]

