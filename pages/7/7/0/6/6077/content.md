## Idea 

Typically spectra of categories involve utilization of some preordering and looking for "almost final" objects in that preordering and declaring them points of spectra. For example, one can look at some class of topologizing subcategories and equip that class with a preordering. A deeper inspection shows that an additional functor may be involved. 

#### Historical motivation

While the spectrum of a commutative ring $R$ is obtained just from studying the ideal in a ring, that is $R$-submodules in $R$, the structure of various sets of ideals in a noncommutative ring usually is too small and otherwise inadequate for geometric purposes. One needs to consider not only ideals, but the whole category of (say left) $R$-modules, thus not necessarily submodules of $R$. A similar thing is with the reconstruction of commutative schemes: the whole abelian category of [[quasicoherent sheaves]] of $\mathcal{O}$-modules, not only the quasicoherent $\mathcal{O}$-submodules of $\mathcal{O}$, is needed for the reconstruction.

#### The development of spectral machinery for categories 

[[Pierre Gabriel]] introduced his spectrum of indecomposable injectives to reconstruct Noetherian separated schemes from their categories of qausicoherent sheaves; now it is often called the Gabriel spectrum. Later many other spectra of abelian categories were invented, including the 1980-s [[A. L. Rosenberg]]'s spectrum used for the reconstruction of quasicompact quasiseparated schemes. Around 2000, Rosenberg noticed that the zoo of many spectra has their common feature and that all the spectra can be produced in analogous way. This pattern for producing spectra is introduced as a __spectral cookbook__ in 

* (RosenbergSpectraNSp) A. L. Rosenberg, _Spectra of noncommutative spaces_, MPIM2003-110 [ps](http://www.mpim-bonn.mpg.de/preblob/1946) [dvi](http://www.mpim-bonn.mpg.de/preblob/1945) (2003)

## The cookbook

#### Local categories and local spectrum 

(RosenbergSpectraNSp 1.1) A category $C$ is __local__ if the full subcategory generated by all objects which are not initial, has itself an initial object. In particular, every local category has initial objects. 

(RosenbergSpectraNSp 1.2) The __local spectrum__ of an arbitrary small category $C$ is the full subcategory $\mathfrak{Spec}^1(C)\hookrightarrow C$ whose objects are all $x$ in $Ob C$ such that the [[undercategory]] $x\backslash C$ is local. 

#### Support of an object

(RosenbergSpectraNSp 1.3) If $x$ is an object in $C$, its support in $C$ is the full subcategory $\mathfrak{Supp}_C(x)\subset C$ whose objects are all objects $y$ in  $C$ such that $C(x,y)=\emptyset$. 

#### $\mathfrak{Spec}^0$

(RosenbergSpectraNSp 1.4) $\mathfrak{Spec}^0(C)\subset C$ is the full subcategory of $C$ generated by those objects $x$ in $C$ whose support $\mathfrak{Supp}_C(x)$ has a final object, $\hat{x}$ (in particular the support is nonempty). 

(RosenbergSpectraNSp 1.4.4) A choice of a final object $\hat{x}$ for every object $x$ in $\mathfrak{Spec}^0(C)$ extends to a functor $\theta_c : \mathfrak{Spec}^0(C)\to C$. 

#### When $C$ is a preorder

(RosenbergSpectraNSp 1.4.6) Now specialize to the case where $C$ is a [[preorder]] category having finite coproducts (equivalently supremum for every pair of objects). Then the functor $\theta_c : \mathfrak{Spec}^0(C)\to C$ factors through the embedding $\mathfrak{Spec}^1(C)\to C$. Consequently, it corestricts to a functor 
$\mathfrak{Spec}^0(C)\to \mathfrak{Spec}^1(C)$ which may also be denoted as $\theta_C$. 

#### Relative spectra 


(RosenbergSpectraNSp 1.6) Given a functor between small categories $F: C\to D$ the relative spectra $\mathfrak{Spec}^0(C,F), \mathfrak{Spec}^1(C,F)$ are defined as isocomma objects ("2-categorical pullbacks")

$$\array{
\mathfrak{Spec}^0(C,F)&\stackrel{\theta_F}\longrightarrow&C\\
{\pi_F^0}_\mathrlap{}\downarrow&&\downarrow{}_\mathrlap{F}\\
\mathfrak{Spec}^0(C)&\underset{\theta_C}\longrightarrow&D
}
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
\array{
\mathfrak{Spec}^1(C,F)&\stackrel{\theta^1_F}\longrightarrow&C\\
{\pi_F^1}_\mathrlap{}\downarrow&&\downarrow{}_\mathrlap{F}\\
\mathfrak{Spec}^1(C)&\underset{\theta^1_C}\longrightarrow&D
}
$$

It appears that, for a fixed target category $D$, the constructions $(C,F)\mapsto \mathfrak{Spec}^0(C,F)$ and $(C,F)\mapsto \mathfrak{Spec}^1(C,F)$ extend to pseudofunctors $Cat/D\to Cat$. If $D$ is a preorder with finite coproducts then every functor $F: C\to D$
induces a canonical functor 

$$
\theta_{C,F} : \mathfrak{Spec}^0(C,F)\longrightarrow \mathfrak{Spec}^1(C,F)
$$

which are the components of a natural transformation of pseudofunctors $Cat/D\to Cat$

$$
\theta : \mathfrak{Spec}^0\longrightarrow \mathfrak{Spec}^1
$$

## Applications to spectra of Abelian categories

#### Idea

Starting with an Abelian category $A$ we proceed in three steps. In the first step we construct some preorder $C_A$ from $A$, or of a functor $F_A: C_A\to D_A$ with a preorder category $D_A$ and then apply the spectral cookbook. The objects of $C_A$ may be some special subcategories of $A$ (e.g. some class of [[topologizing subcategories]]), of multiplicative systems of morphisms, as used in the localization theory and so on. In a third step, one often passes to the equivalence classes of objects in the obtained spectra.

Additionally, one may add construction of some sort of topology or additional "structure stack" to obtained spectrum using possibly supplemental knowledge about the input data. 

#### Remark on monoidal case

Some reconstruction theorems (like the theorems of Balmer and of Garkusha) consider abelian symmetric monoidal categories instead; their spectra are very analogous but the subcategories used to construct the intermediate preorder category are monoidal subcategories as well and various constructions respect the monoidal structure. The pattern is still the same. 

category: noncommutative geometry