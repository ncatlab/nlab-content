A [[field]] $k$ is __algebraically closed__ if every non-constant [[polynomial]] (with one variable and coefficients from $k$) has a root in $k$.  It follows that every polynomial of degree $n$ can be factored uniquely as
$$ p = c \prod_{i = 1}^n (\mathrm{x} - a_i) ,$$
where $c$ and the $a_i$ are elements of $k$.

The __fundamental theorem of algebra__ is, classically, the statement that the [[complex number]]s form an algebraically closed field $\mathbb{C}$.  Arguably, this theorem is not entirely algebraic; the algebraic portion is that $R[\mathrm{i}]$ is algebraically closed whenever $R$ is a [[real-closed field]].  Unusually, this algebraic portion is *not* (as stated) valid in [[constructive mathematics]], while the result the [[real numbers]] form a real closed field $\mathbb{R}$ is constructively valid with the proper definitions.

An __algebraic closure__ of an arbitrary field $k$ is an algebraically closed field $\bar{k}$ equipped with a field homomorphism (necessarily an [[injection]]) $i: k \to \bar{k}$ such that $\bar{k}$ is an [[algebraic extension]] of $k$ (which means that every element of $\bar{k}$ is the root of some non-zero polynomial with coefficients only from $k$).  For example, $\mathbb{C}$ is an algebraic closure of $\mathbb{R}$.  The [[axiom of choice]] proves the existence of $\bar{k}$ for any field $k$, as well as its uniqueness up to [[isomorphism]] over $k$.  However, note that $\bar{k}$ need not be unique up to *unique* isomorphism, so it\'s not really appropriate to speak of [[the]] algebraic closure of $k$.  For example, complex conjugation is a nontrivial [[automorphism]] of $\mathbb{C}$ over $\mathbb{R}$.

Without choice, the existence and uniqueness of algebraic closures may fail; see
*  _[Algebraic closure of Q](http://cs.nyu.edu/pipermail/fom/2006-May/010531.html)_, a thread on FOM started by [[Timothy Chow]]; be sure to check for improperly replied posts with the same subject in that and the next two months
*  possibly _[Algebraic closure without choice](http://doi.wiley.com/10.1002/malq.19920380136)_, a paper by somebody that I can\'t read
*  _[The fundamental theorem of algebra: a constructive development without choice](http://math.fau.edu/Richman/HTML/DOCS.HTM)_ by [[Fred Richman]]


[[!redirects algebraic closure]]