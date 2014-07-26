+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

[[!redirects graphic monoid]]
[[!redirects graphics]]

##Idea
A simple class of finite monoids and categories that permit an effective graphic display via their presheaf categories.


##Definition
A finite monoid $M$ is called _graphic_ if all $x,y\in M$ satisfy the so called _graphic identity_ $xyx=xy$. A finite category $\mathcal{G}$ is called _graphic_ if the endomorphism monoid $End(x)$ is a graphic monoid for all objects $x$.

##Example

* The principal example of a graphic category is $\Delta_1$ the three element monoid $\{\delta_1,\delta_2,1\}$ with $\delta_i\delta_j=\delta_i$, or its Cauchy completion $\overline\Delta_1$. The presheaf topos $\mathcal{S}^{\Delta_1^{op}}$ is the topos of reflexive **graphs**.

##Properties

* Lawvere (1989b, p.53) calls the graphic identity _'the least common generalization of constant (x=c) and identity (x=1)_'.

* In a graphic monoid every element is [[idempotent]] as can be directly seen from the graphic identity with $y=1$.

##Related Pages

* [[graphic topos]]

* [[Aufhebung]]

* [[graph]]

##References

* N. Kimura _The structure of idempotent semigroups I_ , Pacific
Journal of Mathematics **8** no.2 (1958) pp.257-275. ([pdf](msp.org/pjm/1958/8-2/pjm-v8-n2-p07-p.pdf))

* F. W. Lawvere, _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* F. W. Lawvere, _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_ , Proceedings of the first international conference on algebraic methodology and software technology University of Iowa, May 22-24 1989, Iowa City, pp.51-74. 

* F. W. Lawvere, _More on Graphic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **XXXII** no. 1 (1991) pp.5-10. ([pdf](archive.numdam.org/article/CTGDC_1991__32_1_5_0.pdf))
&#8206;
* F. W. Lawvere, _Linearization of graphic toposes via Coxeter groups_ , JPAA **168** (2002) pp.425-436.

* M. P. Sch&#252;tzenberger, _Sur certains treillis gauches_ , C. R. Acad. Sci. Paris, **225** pp.277&#8211;278, 1947. ([pdf](http://igm.univ-mlv.fr/~berstel/Mps/Travaux/A/1947TreillisGauchesCras.pdf))