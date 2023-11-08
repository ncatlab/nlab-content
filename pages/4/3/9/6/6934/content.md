
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Overview

A [[dependent type|dependently typed]] [[functional programming language]] with applications to [[certified programming]]. It is also  used as a [[proof assistant]]. 

Besides [[Coq]], Agda is one of the languages in which [[homotopy type theory]] has been implemented ([Brunerie](#Brunerie)).

Agda can be compiled to [[Haskell]], Epic or Javascript.

## Variants

### Cubical Agda
 {#CubicalAgda}

[Cubical Agda](https://agda.readthedocs.io/en/latest/language/cubical.html)  is a mode of Agda (turned on by the flag `--cubical`) that implements a type theory similar to CCHM (De Morgan) [[cubical type theory]], and thus a form of [[homotopy type theory]].

Its main difference from CCHM is that instead of an exotype of "cofibrant propositions" it uses the interval itself, replacing cofibrant propositions by statements of the form $r \equiv 1$ for some dimension expression $r$.  This change does not prevent the construction of a model for the theory in De Morgan [[cubical sets]], although it doesn't technically fall under the Orton-Pitts axioms since $I$ is not a subobject of $\Omega$, and no one has checked whether this model can be strengthened to a [[Quillen model category]].

More problematically, to support [[identity types]] a la Swan (which are distinct from both cubical "path types" and Martin-Lof "identity types" -- the latter sometimes called "jdentity types" to emphasize their definition relative to the J-eliminator) the type of cofibrant propositions must support a [[dominance]].  Cubical Agda thus assumes that $I$ supports a dominance, but this is not true in De Morgan cubical sets.  So the semantics of the entirety of Cubical Agda, with Swan identity types, is unclear.  (For this reason, the Cubical Agda library generally avoids using Swan identity types, although Cubical Agda supports them.)

Ordinary Martin-Löf [[identity types]] should, in principle, also be definable in Cubical Agda as an indexed inductive family, with computational behavior as usual for any inductive types in cubical type theory.  As of March 2021, however, there is a bug in Cubical Agda that prevents jdentity types from computing correctly.

### Guarded Cubical Agda

The guarded cubical variant extends cubical Agda to support [[guarded recursive]] definitions which can be used to formalize [[synthetic guarded domain theory]].

### Agda-flat
  {#AgdaFlat}

`Agda-flat` is a mode of Agda that implements a [[comonad|co-]][[idempotent monad|monadic]] [[modal operator]] $\flat$ ("flat", following the notation used in [[cohesive homotopy type theory]] as introduced in [[schreiber:dcct|dcct]] and type-theorertically developed in [Shulman 15](cohesive+homotopy+type+theory#Shulman15)).  This makes Agda model a [[modal type theory]] and hence a [[modal homotopy type theory]], such as used, for instance, in [[schreiber:thesis Wellen|Wellen 2017]].

See:

* [`Agda-flat` documentation](https://agda.readthedocs.io/en/v2.6.2.2/language/flat.html)

* [installation instructions](http://www.cl.cam.ac.uk/~amp12/agda/internal-universes/code/agda-flat/install.txt)

## Little-known features {#LittleKnownFeatures}

Listed here are some little-known or undocumented features of Agda that are sometimes useful.  Note that undocumented "features" may change without warning; this list is current as of September 2022, Agda v2.6.2.

* There are a lot of useful documented [keybindings](https://agda.readthedocs.io/en/v2.6.2.2/tools/emacs-mode.html#keybindings) that you may not be aware of.
  * This appears not to be documented in the manual (although it is in the Emacs docstring): When in a hole, the commands `C-c C-,` and `C-c C-.` can be prefixed with `C-u C-u` to normalize the type of the hole (and the term, in the second case) before displaying them.

* The manual doesn't document the customizable variables in the Emacs mode.  Of particular note are:
  * `agda-input-user-translations` allows you to add new bindings to the Unicode input mode
  * `agda2-highlight-level`, when set to `interactive`, uses highlighting to display realtime information about which terms  and subterms in the buffer Agda is currently typechecking.
  * `agda2-program-args` allows you to add command-line arguments to be used every time (e.g. the `-v` options below).  This in in addition to the arguments specified by a particular file in the `OPTIONS` line.

  To change the values of these variables, run `M-x customize-variable RET` and enter the variable name, change the value, and then "Set and Save".

* The command `-v` (verbose output) accepts various additional options that are, according to the developers, "documented by their implementation".  These include:
  * `rewriting.rewrite:50` --- displays information about attempted uses of rewrite rules.
  * `rewriting.match:60` --- displays information about attempted matches during rewriting.
  * `import.chase:2` --- when compiling imported files, displays a notification when each file is completed in addition to when it is started.

  Unfortunately, the output produced by these flags appears in the `*Agda debug*` buffer, which is not visible by default, rather than the standard `AgdaInfo` buffer.  To turn these flags on, you can add (for instance) `-v import.chase:2` to `agda2-program-args` via Customization, as above, or to the `OPTIONS` line of a particular file.

## Minimizing bugs

Since Agda has many experimental features under active development, bugs in these features are not uncommon.  When [reporting a bug](https://github.com/agda/agda/issues/new/choose), it is helpful to "minimize" it to make the shortest possible [MRE](https://en.wikipedia.org/wiki/Minimal_reproducible_example).  Some tips for doing this [from the developers](https://github.com/agda/agda/issues/6067#issuecomment-1236313145) include

* Enable `--type-in-type`, `--no-termination-check`, `--no-positivity-check`, `--no-projection-like`, `--no-fast-reduce`
* Disable unused flags
* Remove unused imports
* Copy definitions from imported modules (other than `Agda.Builtin` modules)
* Delete unused definitions
* Turn functions into postulates
* Inline functions
* Remove clauses from definitions
* Replace patterns by `_` if they are not used
* Replace types by Set
* Delete unused arguments to functions or constructors
* Remove dependencies from types
* Replace (sub)terms by `w/e` where `w/e : ∀ {ℓ} {A : Set ℓ} → A` is a postulate
* Make implicit arguments explicit
* Replace wildcards `_` in terms by their solution


## Related concepts

* [[1lab]]

[[!include proof assistants and formalization projects -- list]]

## References
 {#References}

### General

Agda landing page:

* [wiki.portal.chalmers.se/agda/pmwiki.php](http://wiki.portal.chalmers.se/agda/pmwiki.php)

Documentation:

* [agda.readthedocs.io](https://agda.readthedocs.io/en/v2.6.3)

Online Agda interface:

* [[Ingo Blechschmidt]]: [agdapad.quasicoherent.io](https://agdapad.quasicoherent.io)

Plain Agda originates with:

* [[Ulf Norell]], _Towards a practical programming language based on dependent type theory_, PhD thesis (2007) &lbrack;[pdf](https://www.cse.chalmers.se/~ulfn/papers/thesis.pdf), [[Norell-PracticalDTT.pdf:file]]&rbrack;

* [[Ulf Norell]], *Dependently Typed Programming in Agda*, in: *Advanced Functional Programming* AFP 2008, Lecture Notes in Computer Science **5832** (2009) 230-266 &lbrack;[doi:10.1007/978-3-642-04652-0_5](https://doi.org/10.1007/978-3-642-04652-0_5), [pdf](https://www.cse.chalmers.se/~ulfn/papers/afp08/tutorial.pdf)&rbrack;

Textbook account:

* [[Aaron Stump]], *Verified Functional Programming in Agda*, Association for Computing Machinery and Morgan & Claypool (2016) &lbrack;[doi:10.1145/2841316](https://doi.org/10.1145/2841316), ISBN:978-1-970001-27-3&rbrack;


[[Cubical Agda]] (an implementation of [[cubical type theory]], for [[univalence axiom|univalently]] computing [[homotopy type theory]]) originates with:

* [[Anders Mörtberg]], *Cubical Agda* (2018) &lbrack;[blog post](https://homotopytypetheory.org/2018/12/06/cubical-agda)&rbrack;

* {#VMA19} [[Andrea Vezzosi]], [[Anders Mörtberg]], [[Andreas Abel]], *Cubical Agda: A Dependently Typed Programming Language with Univalence and Higher Inductive Types*, Proceedings of the ACM on Programming Languages **3** ICFP 87  (2019) 1–29 &lbrack;[doi:10.1145/3341691](https://doi.org/10.1145/3341691), [pdf](https://www.cse.chalmers.se/~abela/icfp19.pdf)&rbrack;

### Libraries

Libraries for/with [[homotopy type theory]]/[[univalent foundations of mathematics]]:

* original HoTT library: [github.com/hott/hott-agda](https://github.com/hott/hott-agda)

* [[UniMath project]]: [unimath.github.io/agda-unimath](https://unimath.github.io/agda-unimath)

* [[1lab]]

  > (motivated towards [[univalent categories]])

E.g. on [[group theory]] (cf. *[[Symmetry]]*):

* [[UniMath project]]: [agda-unimath/src/group-theory](https://github.com/UniMath/agda-unimath/tree/master/src/group-theory)


Implementation of [[Cauchy real numbers]] (in [[Errett Bishop|Bishop]]-style [[constructive analysis]]) in [[Agda]] (cf. *[[exact real computer arithmetic]]*):

* [[Martin Lundfall]], *Formalizing real numbers in Agda* (2015) &lbrack;<a href="https://wcl.cs.rpi.edu/pilots/library/papers/TAGGED/4211-Lundfall%20(2015)%20-%20Formalizing%20Real%20Numbers%20in%20Agda.pdf">pdf</a>, [[Lundfall-RealNumbersInAgda.pdf:file]], [github](https://github.com/MrChico/Reals-in-agda)&rbrack;

* [[Zachary Murray]], *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;



### Introductions
 {#Introductions}

#### Quick expositions 
 {#Expositions}

* _['Hello World!' in Adga](http://progopedia.com/example/hello-world/251/)_

* [[Guillaume Brunerie]], _The Agda proof assistant_ (2012) &lbrack;slides:[[Brunerie-AgdaProofAssistant.pdf:file]]&rbrack;

* [[Ulf Norell]], *Programming in Agda*, presentation at *Oregon Programming Languages Summer School* (2014) &lbrack;lecture 1: [video](https://www.youtube.com/watch?v=NrSW7YsneVg), 2: [video](https://www.youtube.com/watch?v=X0JWsoWTWnI), 3: [video](https://www.youtube.com/watch?v=HjpLZr_sirY), 4: [video](https://www.youtube.com/watch?v=Yw2VGwxn_g8)&rbrack;

* [[Scott Fleischman]], *Agda from Nothing*, talk at λC (2016) &lbrack;[video 1](https://www.youtube.com/watch?v=-i-QQ36Nfsk&list=PLCqzQM-xq02Uv4OmcckrFsIyZ20hWEeAx&index=7), [video 2](https://www.youtube.com/watch?v=XprGyVWXwks)&rbrack;

* [[Philip Wadler]], *(Programming Languages) in Agda = Programming (Languages in Agda)*, talk at *Codegram* (Sep 2019) &lbrack;[video](https://www.youtube.com/watch?v=R49VgxNLmsY&t=372s)&rbrack;

* [[Fredrik Nordvall Forsberg]], *The basic syntax of Agda*, talk at CS410 Advanced Functional Programming (2021) &lbrack;[video](https://www.youtube.com/watch?v=yreLHTXwkts)&rbrack;


 
On [[cubical Agda]]:

* [[Andrea Vezzosi]], *Cubical Agda: A Dependently Typed Programming Language with Univalence and Higher Inductive Types* (2019) &lbrack;[video](https://www.youtube.com/watch?v=AZ8wMIar-_c)&rbrack;

#### Tutorials & Lectures

General:

* *Learn you an Agda* (2011) &lbrack;[web](http://learnyouanagda.liamoc.net/pages/introduction.html), [github](https://github.com/liamoc/learn-you-an-agda)&rbrack;

* [[Dan Licata]], Ian Voysey, _[Programming and proving in Agda](http://www.cs.cmu.edu/~drl/teaching/oplss13/)_, course material (2013)

* [[Peter Selinger]], *Lectures on Agda* (2021) &lbrack;[web](https://www.mathstat.dal.ca/~selinger/agda-lectures/)&rbrack;

* [[Ingo Blechschmidt]], *Agda -- a beautiful proof assistant*, course at *Teoria dei Tipi*, Padova (Apr 2023) &lbrack;[webpage](https://agdapad.quasicoherent.io/~Padova)&rbrack;

With emphasis on implementing [[homotopy type theory]] and [[univalent foundations of mathematics]]:

* {#Brunerie} [[Guillaume Brunerie]], _Agda for homotopy type theory_ &lbrack;[github](https://github.com/guillaumebrunerie/HoTT/tree/master/Agda/tutorial)&rbrack;

* [[Martín Hötzel Escardó]], *Introduction to Univalent Foundations of Mathematics with Agda* (2019) &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580), [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/)&rbrack;













category: software

[[!redirects agda]]

[[!redirects Cubical Agda]]
[[!redirects cubical Agda]]
[[!redirects cubical agda]]

[[!redirects Agda-flat]]


