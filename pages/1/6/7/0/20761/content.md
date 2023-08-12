[[!redirects pentagon relation]]
[[!redirects multiplicative unitaries]]
[[!redirects fundamental operator]]

### Idea

While the following idea is originally in operator setup and with an involution, consider the following. Let $H$ be a finite-dimensional vector space.
Consider the invertible operator $W : H\otimes H \to H\otimes H$ satisfying the pentagon identity

$$
W_{1 2} W_{1 3} W_{2 3} = W_{2 3} W_{1 2}
$$
in the space of linear endomorphisms of $H\otimes H\otimes H$. Then the formula

$$
\Delta(h) = W (h\otimes 1) W^{-1} 
$$ 

define a coassociative coproduct on $H$. Usually we replace the structure of the coproduct with knowing $W$, which can be easier to define in infinite-dimensional analogues when the coproduct needs to take values in some hard to manage completions. 

for all $h\in H$. For finite-dimensional Hopf algebras $W(g\otimes h) = g_{(1)}\otimes g_{(2)} h$ and $W^{-1}(g\otimes h) = g_{(1)}\otimes (S g_{(2)}) h$ and then we can reproduce the antipode via the formula 

$$
S h = (\epsilon\otimes id)\circ W^{-1}(h\otimes - )
$$

We can also make a discussion in terms of the dual space $H^*$. Then the coproduct on $H^*$ which is dual to the product on $H$ is also obtained from $W$ by the formula

$$
\Delta_{H^*}(\psi) = W^{-1} (1\otimes\psi) W
$$

### Literature and further directions

In the setup of operator algebras, the multiplicative unitaries were introduced as so called Kac–Takesaki operator. Following some ideas on noncommutative extensions of Pontrjagin duality (in Tannaka-Krein spirit) by George's Kac and also M. Takesaki, Lecture Notes in Mathematics. 247, Berlin: Springer; 1972. pp. 665–785. The followup work of Baaj and Skandalis introduced two more fundamental axioms, regularity and irreducibility, important in $C^*$-algebraic setup. 

* Saad Baaj, Georges Skandalis, _Unitaires multiplicatifs et dualité pour les produits croisés de $C^*$-algèbre_, Annales scientifiques de l'École Normale Supérieure __26__:4 (1993) 425-488  [numdam](https://doi.org/10.24033/asens.1677); _Transformations pentagonales (Pentagonal transformations)_, Comptes Rendus de l'Académie des Sciences, I - Mathematics __327__:7 (1998) 623-628, <a: href="https://doi.org/10.1016/S0764-4442(99)80090-1">doi</a>

* Saad Baaj, Étienne Blanchard, Georges Skandalis, _Unitaires multiplicatifs en dimension finieet leurs sous-objets_, Annales de l’institut Fourier, tome  49, no4 (1999), p. 1305-1344 [numdam](http://www.numdam.org/item?id=AIF_1999__49_4_1305_0)

The monograph on Kac algebras is

* M. Enock, J. M. Schwartz, _Kac algebras and duality of locally compact groups_,  Springer-Verlag, 1992, , x+257 pp. [gBooks](http://books.google.com/books/about/Kac_algebras_and_duality_of_locally_comp.html?id=U6e6aD1gj3oC), [MR94e:46001](http://www.ams.org/mathscinet-getitem?mr=1215933)

and a more recent view of duality between Hopf algebra approach and an approach to quantum groups via multiplicative unitaries is in the book

* Thomas Timmermann, _An invitation to quantum groups and duality: From Hopf algebras to multiplicative unitaries and beyond_, Europ. Math. Soc. 2008.

Introduction to Ch. 7 says in Timmerman's book says

> Multiplicative unitaries are fundamental to the theory of quantum groups in the setting of $C^*$-algebras and [[von Neumann algebra]]s, and to generalizations of [[Pontrjagin duality]]. Roughly, a multiplicative unitary is one single map that encodes all structure maps of a quantum group and of its generalized Pontrjagin dual simultaneously.

Woronowicz has introduced managaeble multiplicative unitaries

* [[S. L. Woronowicz]], _From multiplicative unitaries to quantum groups_, Internat. J. Math. __7__ (1996), 127–149.

It is useful to look at the survey

* Johan Kustermans, Stefaan Vaes, _The operator algebra approach to quantum groups_, 
Proc Natl Acad Sci USA 97(2): 547–552 (2000) [doi](https://doi.org/10.1073/pnas.97.2.547)

* A. Van Daele, S. Van Keer, _The Yang-Baxter and pentagon equation_, Compositio Mathematica __91__:2 (1994)  201-221 [numdam](http://www.numdam.org/item/CM_1994__91_2_201_0)

The categorical background of the pentagon equation has been studied in

* [[Ross Street]], _Fusion operators and cocycloids in
monoidal categories_, Applied Categorical Structures 6: 177–191 (1998) [doi](https://doi.org/10.1023/A:1008655911796)

A finite dimensional version is reformulated in section 3 of

* S. Majid, _Quantum random walks and time reversal_ [doi](https://doi.org/10.1142/S0217751X93001818)

and reprinted in Majid's, _Foundations of quantum group theory_, 1995, as Theorem 1.7.4. Majid has stated in this finite-dimensional case, ideas about [[quantum group Fourier transform]] (see there and Majid's book). This has been used in

* Laurent Freidel, [[nlab:Shahn Majid]], _Noncommutative harmonic analysis, sampling theory and the Duflo map in $2+1$ quantum gravity_, Classical Quantum Gravity __25__ (2008), no. 4, 045006 [MR2009f:83058](http://www.ams.org/mathscinet-getitem?mr=2388191), [doi](http://dx.doi.org/10.1088/0264-9381/25/4/045006)

More categorical treatment and relation to [[Hopf-Galois extension]]s is in 

* A. A. Davydov, _Pentagon equation and matrix bialgebras_, Commun. Alg. __29__(6), 2627–2650 (2001) [doi](https://doi.org/10.1081/agb-100002412)

In the language of finite-dimensional Heisenberg doubles see also the treatment of fundamental operator in

* [[Gigel Militaru]], _Heisenberg double, pentagon equation, structure and classification of finite-dimensional Hopf algebras_, J. London Math. Soc. (2) 69 (2004) 44--64 [doi](https://doi.org/10.1112/S0024610703004897)

Kashaev has explained the pentagon relations for quantum [[dilogarithm]] as coming from the pentagon for the canonical element in the double.

* R.M. Kashaev, _Heisenberg double and the pentagon relation_, St. Petersburg Math. J. 8 (1997) 585&#8211; 592 [q-alg/9503005](http://arxiv.org/abs/q-alg/9503005).

The multiplicative unitary representing quantum dilogarithm has been studied analytically, in the disguise of a quantum exponential, in relation to the construction of "noncompact quantum ax+b group" in

* [[S. L. Woronowicz]], _Quantum exponential function_, Reviews in Mathematical Physics __12__:06,  873-920 (2000) [doi](https://doi.org/10.1142/S0129055X00000344)

The formalism is also in

* S. L. Woronowicz, From multiplicative unitaries to quantum groups, Internat. J. Math. 7(1) (1996) 127–149 [doi](https://doi.org//10.1142/S0129167X96000086), MR 1369908
* P. M. Sołtan, S. L. Woronowicz, _From multiplicative unitaries to quantum groups. II_, J. Funct. Anal
252(1), 42–67 (2007) [doi](https://doi.org/10.1016/j.jfa.2007.07.006)
* [[Ralf Meyer]], Sutano Roy, [[S. L. Woronowicz]], _Quantum group-twisted tensor products of $C^*$-algebras_, Int. J. __25__:02, 1450019 (2014) [doi](https://doi.org/10.1142/S0129167X14500190); _Semidirect products of $C^*$-quantum groups: multiplicative unitaries approach_, Commun. Math. Phys. __351__, 249–282 (2017) [doi](https://doi.org/10.1007/s00220-016-2727-3)
* Ralf Meyer, Sutanu Roy, _Braided multiplicative unitaries as regular objects_, Adv. Stud. Pure Math., Operator Algebras and Mathematical Physics, M. Izumi, Y. Kawahigashi, M. Kotani, H. Matui, N. Ozawa, eds. (Tokyo: Mathematical Society of Japan, 2019) 153 - 178 [doi](https://doi.org/10.2969/aspm/08010153)

The role of quantum torus is here quite clear; later treatments of more general quantum [[dilogarithm]]s influenced by Kontsevich-Soibelman work on [[wall crossing]] and related Goncharov's cluster varieties quantization also witness the appearance of the similar quantum torus. 