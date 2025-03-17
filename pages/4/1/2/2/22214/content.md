
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

_Machine learning_ is a branch of [[computer science]] which devises algorithms to learn from data so as to perform tasks without being explicitly programmed to do so. Notable approaches include [[neural networks]], support vector machines and Bayesian networks.

## Related concepts

* [[neural network]]

* [[kernel method]]

* [[topological data analysis]]

* [[topological machine learning]]

* [[statistical learning theory]]

* [[singular learning theory]]

* [[information geometry]]

## References

### Classical machine learning

Textbook accounts:

* [[Sumio Watanabe]], _Algebraic geometry and statistical learning theory_, CRC Press (2009) &lbrack;[doi:10.1017/CBO9780511800474]( https://doi.org/10.1017/CBO9780511800474)&rbrack;

* [[Sumio Watanabe]], _Mathematical theory of Bayesian statistics_, Cambridge University Press (2018) &lbrack;[ISBN:9780367734817](https://www.routledge.com/Mathematical-Theory-of-Bayesian-Statistics/Watanabe/p/book/9780367734817), [pdf](http://196.189.45.87/bitstream/123456789/36917/1/Sumio%20Watanabe_2018.pdf)&rbrack;

* [[Shai Shalev-Shwartz]], [[Shai Ben-David]], _Understanding machine learning: from theory to algorithms_, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107298019](https://doi.org/10.1017/CBO9781107298019)&rbrack;

* Ian Goodfellow, Y. Bengio, A. Courville, _Deep learning_, MIT Press (2016) &lbrack;[web](https://www.deeplearningbook.org/), [pdf](https://github.com/janishar/mit-deep-learning-book-pdf), [ISBN:9780262035613](https://mitpress.mit.edu/9780262035613/)&rbrack;

See also:

* Wikipedia, *[Machine learning](https://en.wikipedia.org/wiki/Machine_learning)*
* Juergen Schmidhuber (2015), Scholarpedia, 10(11):32832 [Deep learning](http://www.scholarpedia.org/article/Deep_Learning) (with extensive historical bibliography)

Expository review: 

* [[Stephen Wolfram]], *[What Is ChatGPT Doing… and Why Does It Work?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/)* (Feb 2023)

On transformers and large language models (LLM):

* Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser, Illia Polosukhin, _Attention is all you need_, in  Advances in Neural Information Processing Systems 30 (NIPS 2017) [pdf](https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf)

* [[Michael R. Douglas]], _Large language models_, [arXiv:2307.05782](https://arxiv.org/abs/2307.05782)


With regards to [[kernel methods]]:

* Thomas Hofmann, [[Bernhard Schölkopf]], Alexander J. Smola, *Kernel methods in machine learning*, Annals of Statistics 2008, Vol. 36, No. 3, 1171-1220 ([arXiv:math/0701907](https://arxiv.org/abs/math/0701907))

* [[Julien Mairal]], [[Jean-Philippe Vert]], *Machine Learning with Kernel Methods*, 2017 ([pdf](http://members.cbio.mines-paristech.fr/~jvert/svn/kernelcourse/slides/master2017/master2017.pdf), [[MarailVertKernelMethods.pdf:file]])

* Hông Vân Lê, _Supervised learning with probabilistic morphisms and kernel mean embeddings_, [arXiv:2305.06348](https://arxiv.org/abs/2305.06348) 

Proposal for applications of [[category theory]] to machine learning:

* Dan Shiebler, [[Bruno Gavranović]], Paul Wilson, _Category Theory in Machine Learning_ ([arXiv:2106.07032](https://arxiv.org/abs/2106.07032))
* [[Yiannis Vlassopoulos]], _Modelling language semantics and probability densities of text continuations_, QNLP 2022 [youtube](https://www.youtube.com/watch?v=c3IOe3JPfq8)

The following framework claims to relate to [[homotopy type theory]] 

* Ben Goertzel, _Reflective metagraph [[rewriting system|rewriting]] as a foundation for an AGI "Language of Thought"_, [arXiv:2112.08272](https://arxiv.org/abs/2112.08272)

On a definition of artificial *general* intelligence

* S. Legg, M. Hutter, _Universal intelligence: a definition of machine intelligence_, Minds & Machines 17, 391--444 (2007) [doi](https://doi.org/10.1007/s11023-007-9079-x)

* M. Hutter, _Universal artificial intelligence: sequential decisions based on algorithmic
probability_, Springer 2005; book presentation [pdf](http://www.hutter1.net/ai/suaibook.pdf)

* Shane Legg, _Machine super intelligence_, PhD thesis, 2008 [pdf](https://sonar.ch/documents/317954/files/2008INFO002.pdf)


### Quantum machine learning
 {#ReferencesQuantumMachineLearning}

In view of [[quantum computation]] (ie. quantum machine learning):

* Diego Ristè, Marcus P. da Silva, Colm A. Ryan, Andrew W. Cross, Antonio D. Córcoles, John A. Smolin, Jay M. Gambetta, Jerry M. Chow & Blake R. Johnson,
 
  *Demonstration of quantum advantage in machine learning*, npj Quantum Information volume 3, Article number: 16 (2017) ([doi:10.1038/s41534-017-0017-3](https://doi.org/10.1038/s41534-017-0017-3))

* [[Jacob Biamonte]], Peter Wittek, Nicola Pancotti, Patrick Rebentrost, Nathan Wiebe, [[Seth Lloyd]], *Quantum Machine Learning*, Nature **549**  (2017) 195–202 ([doi:10.1038/nature23474](https://doi.org/10.1038/nature23474))

  EurekaAlert, *Quantum Machine Learning* [14-Sep-2017](https://www.eurekalert.org/pub_releases/2017-09/iiop-qml091417.php)

* Iris Cong, Soonwon Choi, Mikhail D. Lukin, *Quantum convolutional neural networks*, Nature Physics volume 15, pages 1273–1278 (2019)  ([doi:10.1038/s41567-019-0648-8](https://doi.org/10.1038/s41567-019-0648-8))
  > (on [[quantum neural networks]])

* Yunchao Liu, Srinivasan Arunachalam, Kristan Temme, *A rigorous and robust quantum speed-up in supervised machine learning* ([arXiv:2010.02174](https://arxiv.org/abs/2010.02174))

* [[Melanie Swan]], [[Renato P dos Santos]], [[Frank Witte]], Between Science and Economics, Volume 2: *Quantum Computing Physics, Blockchains, and Deep Learning Smart Networks*, World Scientific 2020 ([doi:10.1142/q0243](https://doi.org/10.1142/q0243))

* Stefano Mangini, Francesco Tacchino, Dario Gerace, Daniele Bajoni, Chiara Macchiavello, *Quantum computing models for artificial neural networks*, EPL (Europhysics Letters) 134(1), 10002 (2021) ([arXiv:2102.03879](https://arxiv.org/abs/2102.03879))

review:

* Kamila Zaman, [[Alberto Marchisio]], Muhammad Abdullah Hanif, [[Muhammad Shafique]], *A Survey on Quantum Machine Learning: Current Trends, Challenges, Opportunities, and the Road Ahead* &lbrack;[arXiv:2310.10315](https://arxiv.org/abs/2310.10315)&rbrack;

and with emphasis on [classically controlled](quantum+computation#ClassicalControlQuantumData) [[NISQ]]-computes:

* [[John Preskill]], Section 6.5 of: *Quantum Computing in the NISQ era and beyond*, Quantum  2018-08-06, volume 2, page 79 ([arXiv:1801.00862](https://arxiv.org/abs/1801.00862), [doi:10.22331/q-2018-08-06-79](https://doi.org/10.22331/q-2018-08-06-79))

* Kosuke Mitarai, Makoto Negoro, Masahiro Kitagawa, Keisuke Fujii, *Quantum Circuit Learning*, Phys. Rev. A 98, 032309 (2018) ([arXiv:1803.00745](https://arxiv.org/abs/1803.00745))

* {#BenedettiLloydSackFiorentini19} Marcello Benedetti, Erika Lloyd, Stefan Sack, Mattia Fiorentini, *Parameterized quantum circuits as machine learning models*, Quantum Science and Technology 4, 043001 (2019) ([arXiv:1906.07682](https://arxiv.org/abs/1906.07682))

* Marco Radic, *Quantum-enhanced Machine Learning in the NISQ era*, 2019 ([pdf](https://elib.uni-stuttgart.de/bitstream/11682/10642/1/main-english.pdf), [[RadicQMLWithNISQ.pdf:file]])

* Dario Gerace, *Quantum Machine Learning on NISQ hardware*,, talk at *INT online program on "Scientific Quantum Computing and Simulation on Near-Term Devices"*  2020 ([pdf](https://www.int.washington.edu/talks/WorkShops/int_20_3/People/Gerace_D/Gerace.pdf), [[GeraceQMLonNISQ.pdf:file]])

* {#MariBromleyIzaacSchuldKilloran20} Andrea Mari, Thomas R. Bromley, Josh Izaac, Maria Schuld, Nathan Killoran,  *Transfer learning in hybrid classical-quantum neural networks*, Quantum 4, 340 (2020) ([arXiv:1912.08278](https://arxiv.org/abs/1912.08278))

* Lucas Munds, *[Quantum Machine Learning: A Roadmap for NISQ Era and Beyond](https://lmunds.medium.com/quantum-machine-learning-a-roadmap-for-nisq-era-and-beyond-f50fdf89c1ce)*, Oct 17, 2020  

* Tirthajyoti Sarkar, *[TensorFlow Quantum: Marrying machine learning with quantum computing](https://towardsdatascience.com/tensorflow-quantum-marrying-machine-learning-with-quantum-computing-84533757e07f)*, Mar 11, 2020

* QunaSys, Tech Blog, *Quantum machine learning of quantum data with NISQ devices* ([Feb 15 2021](https://qunasys.medium.com/quantum-machine-learning-of-quantum-data-with-nisq-devices-13ef42943d0a))

* [TensorFlow.org](https://www.tensorflow.org/) (Google), *[Quantum Machine Learning](https://www.tensorflow.org/quantum/concepts#quantum_machine_learning)*

Critical discussion:

* Pablo Bermejo, Paolo Braccia, Manuel S. Rudolph, Zoë Holmes, Lukasz Cincio, M. Cerezo: *Quantum Convolutional Neural Networks are (Effectively) Classically Simulable* &lbrack;[arXiv:2408.12739](https://arxiv.org/abs/2408.12739)&rbrack;
  > "We present this as a challenge to the community and argue that until the viability of QCNNs for \[not classically simulable\] datasets can be demonstrated there is no reason to believe QCNNs will be useful. \[...\] Hence we boldly claim: *There is currently no evidence that QCNNs will work on classically non-trivial tasks, and their place in the upper echelon of promising QML architectures should be seriously revised.*"

### Applications

There are or will be innumerable applications. Here are some:

To [[mathematical structures]] in [[algebraic geometry]], [[representation theory]], [[number theory]] and [[combinatorics]]:

* [[Yang-Hui He]], *Machine-Learning Mathematical Structures*, International Journal of Data Science in the Mathematical Sciences &lbrack;[arXiv:2101.06317](https://arxiv.org/abs/2101.06317), [doi:10.1142/S2810939222500010](https://doi.org/10.1142/S2810939222500010)&rbrack;

reviewed in:

* [[Yang-Hui He]], *Machine-Learning Mathematical Structures*, talk at *[M-Theory and Mathematics 2023](https://ncatlab.org/nlab/show/M-Theory+and+Mathematics#2023)*, NYU Abu Dhabi (Jan 2023) &lbrack;[web](/nlab/show/M-Theory+and+Mathematics#He2023)&rbrack;


To the [[conformal bootstrap]]:

* Gergely Kántor, Vasilis Niarchos, [[Constantinos Papageorgakis]], *Solving conformal field theories with artificial intelligence* ([arXiv:2108.08859](https://arxiv.org/abs/2108.08859))

(...)





[[!include coupling proof assistants with machine learning -- references]]








[[!redirects machine-learning]]


[[!redirects quantum machine learning]]

[[!redirects artificial intelligence]]



