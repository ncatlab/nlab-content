A [[continuous map]] $i:A\hookrightarrow X$ is a **Hurewicz cofibration** if it satisfies the **homotopy extension property**: for any topological space $Y$, continuous maps $f:A\to Y$, $\tilde{f}:X\to Y$ such that $\tilde{f}\circ\tilde{i}=f$ and a [[homotopy]] $F:A\times I\to Y$ such that $F(-,0)=f$ there is a homotopy $\tilde{F}:X\times I\to Y$ such that $\tilde{F}\circ(i\times id_I)=F$ and $\tilde{F}(-,0)=\tilde{f}$. There is also a version for [[pointed space]]s. We say that a Hurewicz cofibration $i:A\to X$ is **closed** if $i(A)$ is closed in $X$.

[[Hurewicz fibration]]s, closed Hurewicz cofibrations and [[homotopy equivalences]] make one of the standard Quillen [[model category]] structures on the category [[Top]] of all topological spaces; see [[Strøm's model category]]. 

Every Hurewicz cofibration $i$ is an injective map and if the image $i(A)$ is closed then it is a homeomorphism onto its image. In the category of [[weakly Hausdorff space|weakly Hausdorff]] [[compactly generated spaces]], $i(A)$ is always closed, but in the category of all topological spaces there are pathological counterexamples. If $A\subset X$ is closed and the inclusion is a cofibration, then the pair $(X,A)$ is an [[NDR-pair]].

* Dieter Puppe, _Bemerkungen &#252;ber die Erweiterung von Homotopien_, Arch. Math. (Basel) 18 1967 81--88; MR0206954 (34 #6770) [doi](http://dx.doi.org/10.1007/BF01899475)

* Arne Str&#248;m, _Note on cofibrations_,  Math. Scand.  19  1966 11--14 [file](http://www.mscand.dk/article.php?id=1782) MR0211403 (35 #2284); _Note on cofibrations II_,  Math. Scand.  22  1968 130--142 (1969) [file](http://www.mscand.dk/article.php?id=1867) MR0243525 (39 #4846) 


[[!redirects Hurewicz cofibrations]]