A loop $(L,\cdot)$ (in the algebraic sense, of a [[quasigroup]] with unit element) is a __left Bol loop__ (resp. __right Bol loop__) if all triples $a,b,c$ of its elements satisfy 
the left  Bol identity
$$
(a (b a)) c = a (b (a c))
$$
and resp. right Bol identity
$$
((b a) c) a = b ((a c) a)
$$ 
Equivalently, the left multiplication operators $L_a$ and right multiplication operators $R_a$ satisfy the corresponding properties
$$
L_{a(b a)} = L_a L_b L_a
$$
or
$$
R_{(a c) a} = R_a R_c R_a
$$
A loop is a [[Moufang loop]] iff it is simultaneously a left Bol loop and a right Bol loop. 

A __core__ of a right Bol loop $(L,\cdot)$ is the binary algebraic structure $(L,+)$ where
$$
a + b = (a\cdot b^{-1})\cdot a
$$
(due nonassociativity pay attention to the order of brackets!)

Every [[isotopy (algebra)|isotopy]] of right Bol loops induces an isomorphism between the corresponding cores.

The core of a [[Moufang loop]] has the following properties: 

$$
a + a = a
$$ 
$$
a + (a + b) = b
$$
$$
a+(b+c)=(a+b)+c
$$
$$
(a+b)^{-1}=a^{-1}+b^{-1}
$$
$$
(a+b)\cdot c = a\cdot c + b\cdot c 
$$
$$
c\cdot(a+b) = c\cdot a + c\cdot b
$$

Related notions: [[Moufang loop]], [[Bol algebra]], [[identities of Bol-Moufang type]]

* wikipedia, [Bol loop](http://en.wikipedia.org/wiki/Bol_loop)
* D. A. Robinson, _Bol loops_, Trans. Amer. Math. Soc. __123__ (1966);  _Bol quasigroups_, Publ. Math. Debrecen __19__ (1972), 151--153
* A. Van&#382;urov&#225;, _Cores of Bol loops and symmetric groupoids_, Bul. Acad. &#350;tiin&#355;e Repub. Mold. Mat., 2005, no. 3, 153&#8211;164 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=basm&paperid=144&what=fullt&option_lang=rus)
* V. Volenec, _Grupoidi, kvazigrupe i petlje_, Zagreb 1982

category: algebra
[[!redirects Bol loops]]