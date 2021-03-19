Game theory is the study of strategic interaction between agents. It is often used for mathematical modelling of real-world situations in which agents interact, including in microeconomics, computer science and ecology.

Game theory should not be confused with [[game semantics]], which has some terminology and history in common but has little overlap in practice.

##Via coalgebras##

Several authors have approached game theory through coalgebraic systems theory, defining games as elements of the [[terminal coalgebra for an endofunctor|terminal coalgebra]] of an appropriate functor. This puts the concepts of _state_ and _state transition_ in a game to centre stage. It is closely related to [extensive form games](https://en.wikipedia.org/wiki/Extensive-form_game), whereby a game is defined by its tree of plays.

Perhaps the first paper to use this approach is [Pavlovic 2009](#Pavlovic09). Others are [Abramsky and Winschel 2017](#AbramskyWinschel17) and [Ghani, Kupke, Lambert and Forsberg 2018](#Ghani18a), the latter of which connects coalgebraic game theory with compositional game theory.

##Compositional game theory##

Open games approach games as open systems, making them morphisms of a [[symmetric monoidal category]] which can be depicted as [[string diagram|string diagrams]], in the spirit of [[applied category theory]]. See [Ghani, Hedges, Winschel and Zahn 2018](#Ghani18b).

Open games have a close connection to [[lens (in computer science)|lenses]]. This can be used to situate open games inside a symmetric monoidal [[double category]] in a game-theoretically interesting way, see [Hedges 2018](#Hedges18).

##Topology and game theory##

Deformations between strategy profiles have been considered as a practical method to compute Nash equilibria (see [Herings and Peeters 2010](#Herings10)).

## References

* $n$Cafe: [combinatorial game categories](http://golem.ph.utexas.edu/category/2009/11/combinatorialgame_categories.html), [zero determinant strategies](http://golem.ph.utexas.edu/category/2012/07/zerodeterminant_strategies_in.html) in the iterated prisoner's dilemma
* wikipedia: [game theory](https://secure.wikimedia.org/wikipedia/en/wiki/Game_theory), [combinatorial game theory](http://en.wikipedia.org/wiki/Combinatorial_game_theory), [dominance (game theory)](http://en.wikipedia.org/wiki/Dominance_%28game_theory%29), [Nash equilibrium](http://en.wikipedia.org/wiki/Nash_equilibrium), [wild type](http://en.wikipedia.org/wiki/Wild_type) 
* William Press, Freeman Dyson, _Iterated prisoner's dilemma contains strategies that dominate any evolutionary opponent_, [PNAS open access](http://www.pnas.org/content/early/2012/05/16/1206569109.full.pdf+html), March 2012.
* [[J.R.B. Cockett]], G.S.H. Cruttwell and K. Saff, _Combinatorial game categories_, [pdf](https://www.mta.ca/uploadedFiles/Community/Bios/Geoff_Cruttwell/CGC.pdf)
* [[André Joyal]], _Remarques sur la th&#233;orie des jeux &#224; deux personnes_, Gazette des
Sciences Mathematiques du Qu&#233;bec 1(4):46&#8211;52, 1977; Robin Houston's rough translation [ps](http://www.ma.man.ac.uk/~rhouston/Joyal-games.ps)
* Andr&#233; Joyal, _Free lattices, communication and money games_, in: Logic and
scientific methods. Volume one of the proceedings of the tenth international
congress of logic, methodology and philosophy of science, Florence, Italy, Synth.
Libr. 259, pages 29&#8211;68. Dordrecht: Kluwer Academic Publishers, 1997.
* {#Pavlovic09} [[Dusko Pavlovic]], _A semantical approach to equilibria and rationality_, CALCO 2009. ([arXiv:0905.3548](https://arxiv.org/abs/0905.3548), [doi:10.1007/978-3-642-03741-2_22](http://dx.doi.org/10.1007/978-3-642-03741-2_22))
* {#AbramskyWinschel17} [[Samson Abramsky]] and [[Viktor Winschel]], _Coalgebraic analysis of subgame-perfect equilibria in infinite games without discounting_, Mathematical structures in computer science 2017. ([arXiv:1210.4537](https://arxiv.org/abs/1210.4537), [doi:10.1017/S0960129515000365](https://doi.org/10.1017/S0960129515000365))
* {#Ghani18a} [[Neil Ghani]], [[Clemens Kupke]], [[Alasdair Lambert]] and [[Fredrik Nordvall Forsberg]], _A compositional treatment of iterated open games_, Theoretical computer science 2018. ([arXiv:1711.07968](https://arxiv.org/abs/1711.07968), [doi:10.1016/j.tcs.2018.05.026](https://doi.org/10.1016/j.tcs.2018.05.026))
* {#Ghani18b} [[Neil Ghani]], [[Jules Hedges]], [[Viktor Winschel]] and [[Philipp Zahn]], _Compositional game theory_, LiCS 2018. ([arXiv:1603.04641](https://arxiv.org/abs/1603.04641), [doi:10.1145/3209108.3209165](https://doi.org/10.1145/3209108.3209165))
* {#Hedges18} [[Jules Hedges]], _Morphisms of open games_, MFPS 2018. ([arXiv:1711.07059](https://arxiv.org/abs/1711.07059), [doi:10.1016/j.entcs.2018.11.008](https://doi.org/10.1016/j.entcs.2018.11.008))
* {#Herings10} P. Jean-Jacques Herings and Ronald Peeters, _Homotopy methods to compute equilibria in game theory_, Economic Theory 2010. ([doi:10.1007/s00199-009-0441-5](https://doi.org/10.1007/s00199-009-0441-5))
