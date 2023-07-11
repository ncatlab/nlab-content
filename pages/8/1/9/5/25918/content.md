# Contents 
* this block creates the table of contents, leave as is
{: toc}


## Idea


In [[music theory]], a pitch-class is the [[equivalence relation|equivalence class]] of all pitches that are separated by some number of octaves. However, the equivalence relation can be generalized to systems in which octave equivalence does not hold, and some other interval is chosen instead. 


## Twelve tone equal temperament 


In Western classical music, all scales are derived as [[set|subsets]] of the chromatic scale of pitch-classes. In musical terminology, the set of pitch-classes is 
\[ 
\big\{
  C, C\sharp, D, D\sharp, E, F, F\sharp, G, G\sharp, A, A\sharp, B
\big\}
\,. 
\]
However, in more contemporary music theory these pitch-class names are replaced by [[integer]] notation, so that $C$ becomes 0, $C\sharp$ becomes 1, ..., and $B$ becomes 11. The integer notation immediately expresses the [[cyclic group|additive group]] structure of the pitch-classes, so that we can manipulate the set of pitch-classes as though it is the group $\mathbb{Z}/12\mathbb{Z}$, or $\mathbb{Z}_{12}$ for short, with addition (modulo 12) as the [[binary function|binary operation]]. An immediate result is that we can define [[map|mappings]] on the pitch-classes in a mathematically intuitive way. For instance, the mapping

\[
\label{SubtractionOfPitchClasses}
  \array{
    \mathllap{INT \;\colon\;}
    \mathbb{Z}_{12} \times \mathbb{Z}_{12} 
      &\longrightarrow& 
    \mathbb{Z}_{12}
    \\
    (x, y) &\mapsto&  y - x 
    \mathrlap{\;(mod 12)} 
  }
\,
\]

gives what is called the **pitch-class interval** between pitch-classes $x$ and $y$. For instance, if $x = 4$ and $y = 7$, then $\mathrm{INT}(4, 7) = 3$, which, in musical terminology, expresses the fact that the pitch-classes $E$ and $G$ are three semitones, i.e. a minor third, apart. 




## As an equivalence relation


The set of pitch-classes can be derived from the relation of octave equivalence on pitch space $\mathbb{Z}$. One usually treats $\mathbb{Z}$ as the set of all pitches, with $0$ as middle-$C$. This way one derives the group $\mathbb{Z}_{12}$ (of pitch-classes) in the usual way, as the residue classes of the integers, so that e.g. the pitch-class $4$ is really the class of integers
\[ 
  [4] 
   \;\coloneqq\; 
  \big\{ 
    4 + 12k \in \mathbb{Z} 
  \;\big\vert\; 
    k \in \mathbb{Z} 
  \big\}. 
\]
One may likewise derive these classes via the map
\[ 
  c \;\colon\; 
    \mathbb{Z} \longrightarrow \mathbb{Z}_{12} 
\]
that sends pitches to their respective pitch-classes, so that the [[fiber]] of $c$ over each $x \in \mathbb{Z}_{12}$ is its equivalence class of pitches.




## As a denotator


According to the theory of forms and denotators due to [Mazzola (2012)](#Mazzola12), we may denote a pitch-class formally using the following notation,
\[ 
  thisPitchClass
    \;\colon\; 
  0_\mathbb{Z} 
    \rightsquigarrow 
  PC 
    \underset{Id}{\longrightarrow} 
  Simple(\mathbb{Z}_{12})(n)
  \,, 
\]
where $PC$ is a form defined by
\[ 
  PC 
    \underset{Id}{\longrightarrow} 
  Simple (\mathbb{Z}_{12})
  \,.
\]




## Generalizations to non-twelve tone equal temperament


One can generalize the notion of pitch-class to groups other than $\mathbb{Z}_{12}$, in particular for any $\mathbb{Z}_n$ for $n \geq 1$. One then derives the notion of an $n$-note scale. In general, neither ordinary octave equivalence nor equal temperament are required of such scales. For instance, the criterion for equivalence of pitches could be an interval larger or smaller than an octave, and pitch-classes may not be equally spaced. Nonetheless, one may still want to treat such scales as groups, in order to manipulate them algebraically. 


## References
 {#References}

* Allen Forte, _The structure of atonal music_, Yale University Press, 1973. 

* David Lewin, _Generalized musical intervals and transformations_, Oxford university press, USA, 2010.

* {#Mazzola12} Guerino Mazzola, _The topos of music: geometric logic of concepts, theory, and performance_, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-8141-8](https://doi.org/10.1007/978-3-0348-8141-8)&rbrack; 

* Robert Morris, _Composition with pitch-classes_, Yale University, 1987.
 