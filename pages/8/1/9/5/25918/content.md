# Contents 
* this block creates the table of contents, leave as is
{: toc}


## Introduction


In [[music theory]], the term "pitch" is generally used to mean an individual [[frequency]], such as the pitch A4, which has a frequency of 440 Hz. The concept of pitch therefore does not take into account octave equivalence, so A4 (440 Hz) and A5 (880 Hz) are distinct pitches. On the other hand, a *pitch-class* denotes the [[equivalence relation|equivalence class]] of pitches that are octave-equivalent. Therefore A4 and A5 are members of the pitch-class A. 

The need to formulate the notion of pitch-class arose with the rise of atonal music theory in the twentieth century. Due to a radical shift in musical idioms, the concepts from the past that were taken for granted for centuries were no longer adequate for music theory. The concept of pitch-class was one such notion. Rahn, in [Rahn 1980](#Rahn80), summarizes the situation as so:


> Tonal theory has been around so long and so pervasively that many of its concepts are built into our basic musical terminology. To call a particular pitch a $C\sharp$ is to accept at least two theoretical assumptions about structures of pitches. The first is the assumption of *pitch-class equivalence*: that all pitches that are called $C\sharp$, in whatever octave, have enough in common (for purposes of musical structure) that it is useful to give all of them the same name–"$C\sharp$". The second assumption of *diatonic functionality*: a $C\sharp$ cannot function as the fourth degree of an $A\flat$ major scale, even though a $C\sharp$ and a $D\flat$ (which can so function) may both be produced by hitting the same key on a piano. Of these two assumptions, that of diatonic functionality is more elaborate, more sophisticated, further along the tree of theoretical development, and more peculiarly "tonal".
	
> The theory of atonal music can retain the assumption of pitch-class equivalence, but must reject diatonic functionality as being too particularly "tonal". Hence there is a need for a way to notate pitches which does not incorporate diatonic functionality. For decades, theorists have been solving this problem using *integers* to notate pitches. This less specialized notation has allowed us also, as a bonus, to *construct* (rather than assume) the structures of diatonic functionality in tonal music. Tonal theory can in this sense be regarded as a special case of atonal theory, just as atonal theory is a special case (incorporating pitch-class equivalence) of  a more general theory of music. 
 

In music theory, one therefore denotes pitches with integer notation, where 0 usually refers to $C4$, 1 to $C\sharp4$ or $D\flat4$, -12 to $C3$, and so on. One then derives the notion of pitch-class, where two pitches $p$ and $p'$, represented as integers, are equivalent iff there is an $n \in \mathbb{Z}$ such that
\[
p + 12 n = p'.
\] 
This equivalence relation means that the set of pitch-classes is therefore treated as the [[cyclic group]] $\mathbb{Z}_{12}$. 

It is important to note however that just because we use integers to denote pitches and pitch-classes, this does not mean that all properties of integers and cyclic groups make sense as properties of pitches/pitch-classes. For instance, 13 is a prime number, but it doesn't make sense to think of the pitch $C\sharp5$ as a prime pitch. The use of integers to denote pitches and pitch-classes is therefore a convention, which is used for the expediences of music theory. 

Some aspects of the structure of the integers that also correspond to the structure of pitches/pitch-classes are the following:

* **Greater than**. For $a, b \in \mathbb{Z}$ pitches, if $a \lt b$ then the pitch denoted by $a$ sounds lower than the pitch denoted by $b$. Note that this relation does *not* make sense however for pitch-classes $x, y \in \mathbb{Z}_{12}$. 

* **Interval-class**. For $w, x, y, z \in \mathbb{Z}_{12}$ pitch-classes, if $x-w = z-y$, then the pitch-class interval between $w$ and $x$ is equal to the pitch-class interval between $y$ and $z$. For instance, the pitch-class interval between $C$ (0) and $E$ (4) is $4$, as is the pitch-class interval between $F$ (5) and $A$ (9). This means that hearing a $C$ and an $E$ sounding simultaneously will have a similar harmonic "flavor" as hearing an $F$ and an $A$ simultaneously. 
 

## References
 {#References}

* Allen Forte, _The structure of atonal music_, Yale University Press, 1973. 

* David Lewin, _Generalized musical intervals and transformations_, Oxford university press, USA, 2010.

* {#Mazzola12} Guerino Mazzola, _The topos of music: geometric logic of concepts, theory, and performance_, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-8141-8](https://doi.org/10.1007/978-3-0348-8141-8)&rbrack; 

* Robert Morris, _Composition with pitch-classes_, Yale University, 1987.

* {#Rahn80} John Rahn, _Basic atonal theory_, 1980. 
 