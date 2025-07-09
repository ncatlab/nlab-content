
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

*Kenzo* is a piece of [[computer program|software]] for computations in [[constructive mathematics|constructive]] [[algebraic topology]] ([[computational topology]]).

## Related entries

* [[list of mathematics software]]




## Some notes

Some notes on coding in [Kenzo](https://www-fourier.ujf-grenoble.fr/~sergerar/Kenzo/).

### Space constructors

    (setq m23 (moore 2 3)) ==> "Moore space (Z/2Z,3)"

    (setq kz1 (k-z 1))     ==> "Eilenberg-Maclane space K(Z,1)"

    (crts-prdc space1 space2): Cartesian product space

    (loop-space space1): Loop space 

### Predicates

     (typep space1 'kan)

     (typep space1 'simplicial-group)

     (typep space1 'ab-simplicial-group)

### Invariants

     + (homology)
     + (basis) eg. Basis for a simplicial set..

\begin{example}
$\pi_4$ and $\pi_5$ for `Moore(Z/2,3)`

To compute the 4th [[homotopy group]] of `Moore(Z/2,3)`, follow the overview of the DOC and do

      #+begin_src common-lisp
      (require 'kenzo)
      (setf m23 (moore 2 3))
      (setf ch3 (chm1-class m23 3))
      (setf f3 (z2-whitehead m23 ch3))
      (setf x4 (fibration-total f3))
      (homology x4 3 5) ;; this gives Z/2Z, which is the \pi_{4} for Moore(Z/2Z,3).
      #+end_src

To compute its 5th homotopy group:

     #+begin_src common-lisp
     (setf ch4 (chml-class x4 4))
     (setf f4 (z2-whitehead x4 ch4))
     (setf x5 (fibration-total f4))
     (homology x5 4 6) ;; this gives Z/4Z, which is the \pi_{5} for Moore(Z/2Z,3)
     #+end_src

\end{example}


### Computations?

     (cprd) coproduct.. eg for a K(Z,1)

     (aprd) product.. eg for a K(Z,1)


## Chapter by chapter

### 1. Chain complexes

#### 1.3. Representation of a chain complex

\begin{example}
**morphism from a chain complex to another, of degree $k$**

A chain complex is implemented as an instance of a CLOS class. 

See page 8 for the definition of the class 

     =CHAIN-COMPLEX=: =(DEFCLASS CHAIN-COMPLEX () [..])= 

This class has 8 slots

`=cmpr=`, `=basis=`, `=bsgn=`, `=dffr=`, `=idnm=`, `=orgn=`, `=grmd=`, `=efhm=`. 

the accessors of the slots are the functions speficied after `=:reader=` in the defclass code.

To build a chain complex, use `=build-chcm=`. For example:

       #+begin_src common-lisp
       ;; warning hasn't compiled
       (setf diabolo-cmpr #'s-cmpr)
       (setf diabolo-basis #'(lambda (dmn)
                               (case dmn
                                 (0 '(s0 s1 s2 s3 s4 s5))
                                 (1 '(s01 s02 s12 s23 s34 s35 s45))
                                 (2 '(s345))
                                 (otherwise nil ))))
       (setf diabolo-bspn 's0) ;; base point

       (setf diabolo-pure-dffr
             #'(lambda (dmn gnr)
                 (unless (<= 0 dmn 2)
                   (error "Non-correct dimension for diabolo-dp."))
                 (case dmn
                      (0 (cmbn -1)) ; Note the null combination of degree -1
                      (1 (case gnr
                           (s01 (cmbn 0 -1 's0 1 's1))
                           (s02 (cmbn 0 -1 's0 1 's2))
                           (s12 (cmbn 0 -1 's1 1 's2))
                           (s23 (cmbn 0 -1 's2 1 's3))
                           (s34 (cmbn 0 -1 's3 1 's4))
                           (s35 (cmbn 0 -1 's3 1 's5))
                           (s45 (cmbn 0 -1 's4 1 's5))))
                      (2 (case gnr
                           (s345 (cmbn 1 1 's34 -1 's35 1 's45))))
                      (otherwise (error "Bad generator for complex diabolo")))
                 ))
       (setf diabolo-strt :GNRT)
       (setf diabolo-orgn '(diabolo-for-example))

       ;; Then construct it!
       (setf diabolo (build-chcm :cmpr diabolo-cmpr :basis diabolo-basis
                                 :bsgn diabolo-bspn :intr-dffr diabolo-pure-dffr
                                 :strt diabolo-strt :orgn diabolo-orgn))
       #+end_src

\end{example}

Simple functions handling chain complexes: `=cat-init=`, `=chcm=`, `=cmpr=`, `=basis=`, `=dffr=`, `=z-chcm=`.

An important trivial case Z[0]. Do it as exercise! .. Answer on page 14. You can call it by `=(z-chcm)=` (predefined).

\begin{example}
**The circle.**

       #+begin_src common-lisp
       ;; warning hasn't compiled
       (defun CIRCLE ()
         (the chain-complex
              (build-chcm
               :cmpr #'(lambda (gnrt1 gnrt2) (the cmpr :equal))
               :basis #'(lambda (dmns)
                          (the list
                               (case dmns (0 '(*)) (1 '(s1))
                                          (otherwise +empty-list+))))
               :bsgn '*
               :intr-dffr #'zero-intr-dffr
               :strt :cmbn
               :orgn '(circle))))
       #+end_src

\end{example}

#### 1.4. Morphisms

See the final example provided in the end of this section.

### 2. Objects with effective homology


### 21. Computing homotopy groups

By constructing the [[Whitehead tower]] of a space $X$, the computation of the [[homotopy groups]] of $X$ is reduced to computing the [[ordinary homology|homology]] groups of some pieces in the tower.

#### 21.2 The functions for computing homotopy groups

     #+begin_quote
     In this version of Kenzo, only the case where the first non-null
     homology group is Z or Z/2Z can be processed; ..
     #+end_quote

## Examples

### $S^{2}$

The [[2-sphere]] $S^2$:

     #+begin_src common-lisp :eval never
     ;; This looks like a 2-sphere to me
     (setf short-s2?
           (build-finite-ss
            '(v0 v1 v2
              1 e01 (v1 v0) e02 (v2 v0) e12 (v2 v1)
              2 t (e12 e02 e01) t_ (e12 e02 e01))))
     #+end_src

### $\mathbb{R}P^{2}$

The [[real projective plane]] $\mathbb{R}P^2$:

     #+begin_src common-lisp :eval never
     ;; This is a small construction of RP^2.. taken from lecture note.
     ;; Constructive Homological Algebra and Applications-Julio Rubio and Francis Sergeraert-arXiv:1208.3816
     (setf short-P2R
           (build-finite-ss '(v 1 e (v v) 2 t ( e v e ))))
     #+end_src




## References

* [Kenzo Homepage](https://www-fourier.ujf-grenoble.fr/~sergerar/Kenzo/)

* [[Julio Rubio]], [[Francis Sergeraert]], Yvon Siret: *KENZO -- a Symbolic Software for Effective Homology Computation* (1999) &lbrack;[pdf](https://www-fourier.ujf-grenoble.fr/~sergerar/Kenzo/Kenzo-doc.pdf)&rbrack;

* Jonathan Heras, Vico Pascual, Ana Romero, [[Julio Rubio]], *Integrating multiple sources to answer questions in Algebraic Topology*, Lectures Notes in Artificial Intelligence **6167** (2010) &lbrack;[arXiv:1005.0749](https://arxiv.org/abs/1005.0749)&rbrack;

Based on :

* [[Julio Rubio]], [[Francis Sergeraert]], *Constructive Algebraic Topology*, Bulletin des Sciences Mathématiques
**126** 5 (2002) 389-412 &lbrack;[arXiv:math/0111243](https://arxiv.org/abs/math/0111243), <a href="https://doi.org/10.1016/S0007-4497(02)01119-3">doi:10.1016/S0007-4497(02)01119-3</a>&rbrack;

Exposition:

* [[Julio Rubio]], *Formalization of Mathematics: why Algebraic Topology?*, MAP Spring School 2012 &lbrack;[pdf](http://www-sop.inria.fr/manifestations/MapSpringSchool/contents/JulioRubio.pdf)&rbrack;

A rewrite of Kenzo in [[Haskell]]:

* [[Mitchell Riley]]: [github.com/mvr/at](https://github.com/mvr/at)



category: reference
