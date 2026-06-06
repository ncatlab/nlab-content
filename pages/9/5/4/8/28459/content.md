
## Chord orbifolds in music theory
 {#ChordOrbifoldsInMusicTheory}

### Idea

In [[music theory]], the configuration space of unordered musical *chords*, [[global quotient orbifold|quotentied]] by *acoustic equivalences* like *octave repetition* and *voice permutation*, may be thought of $[$[Tymoczko 2006](#Tymoczko2006), [Calender, Quinn & Tymoczko 2008](#CalenderQuinnTymoczko2008)\] as an [[orbifold]] (specifically a [[toroidal orbifold]]) whose singular strata correspond to distinct *voices*, as follows:


**Pitch-Class Space as a Circle.** In Western music, *pitch* may be modeled continuously as a [[real number]] $p\in\mathbb{R}$, where [[integers]] represent semitones (e.g., piano keys). However, human hearing exhibits *octave equivalence*: a "C" played in one octave sounds functionally equivalent to a "C" played in the next octave, 12 semitones away. Therefore considering pitches modulo octave equivalent yields the *pitch-class* [[quotient space]], topologically a [[circle]]:
 
\[
  \label{PitchClassSpace}
  \mathbb{R}/12\mathbb{Z}
    \cong 
  S^{1}
  \mathrlap{\,.}
\]


**Ordered Chords Space as a Torus.** An ordered $n$-note chord  is an [[n-tuple|$n$-tuple]] of such pitch classes. The space of all such ordered $n$-note chords is therefore the [[Cartesian product]] of $n$ circles, which is the [[n-torus|$n$-torus]]:

\[
  \label{OrderedChordSpace}
  T^{n}
    =
  \big(S^1\big)^{\times_n}
  \mathrlap{\,.}
\]

**Unordered Chord Space as an Orbifold.** But music theory typically treats chords as unordered [[sets]]. For example, the chord $\{C, E, G\}$ is functionally the same chord as $\{E, G, C\}$. To formalize this [[permutation]] [[invariance]], one is to consider the further quotient of the torus $T^{n}$ (eq:OrderedChordSpace) by the [[permutation]] [[group action|action]] of the [[symmetric group]] $Sym_{n}$. But since this action is not [[free action|free]] (it has [[fixed points]]), the proper incarnation of this is as the *[[global quotient orbifold]]*

\[
  \label{UnorderedChordSpace}
  T^n \sslash Sym_n
  \,.
\]

The [[orbifold singularity|singular]] [[strata]] of this [[orbifold]] correspond to the chords where voices merge (cross).

**Further Symmetries.** There are further [[symmetries]] that may be quotiented out: 


* *Transposition*: Shifting all notes up or down by a constant interval $c$. This acts as a continuous translation along the main diagonal of $T^{n}$. Factoring out transposition yields a space locally isomorphic to $\mathbb{R}^{n-1}$.

* *Inversion*: Reflecting pitch space ($p\mapsto-p$), which corresponds to turning chords upside down.

The [[global quotient orbifold]] of the $n$-torus by permutation, transposition, and inversion simultaneously results in a farily complex orbifold. For example, the space of 3-note chords modulo transposition and inversion is a [[Möbius strip]] with a [[boundary]] of [[singular points]].

\linebreak

Of course, there is mathematical idealization involved in this, which may not necessarily always be reflected in musical practice (cf. [Tymoczko 2007](#Tymoczko2007))

### Applications

These orbifolds are used to study *voice leading* --- the transition from one chord to another over time. A piece of music can be modeled as a continuous path winding through this orbifold. Efficient voice leading (where voices move by the smallest possible intervals) translates to finding [[geodesics]] on this [[Riemannian orbifold]], where [[orbifold singularity|singular]] boundaries act like acoustic "mirrors"; paths that bounce off the singularities represent musical voices crossing or temporarily merging into a unison.



### References

The original articles:

* {#Tymoczko2006} [[Dmitri Tymoczko]]: *The Geometry of Musical Chords*, Science **313** 5783 (2006) 72--74 \[<a href="https://doi.org/10.1126/science.1126287">doi:10.1126/science.1126287</a>, [pdf](https://dmitri.mycpanel.princeton.edu/voiceleading.pdf)\]

* {#CalenderQuinnTymoczko2008} Clifton Callender, Ian Quinn, [[Dmitri Tymoczko]]: *Generalized Voice-Leading Spaces*, Science **320** 5874 (2008) 346--348 \[<a href="https://doi.org/10.1126/science.1153021">doi:10.1126/science.1153021</a>, [pdf](https://dmitri.mycpanel.princeton.edu/files/publications/science2.pdf)\]

Further discussion: 

* {#Tymoczko2007} [[Dmitri Tymoczko]]: *Response to Comment on "The Geometry of Musical Chords"*, Science **315** 5810 (2007) 330 \[<a href="https://doi.org/10.1126/science.1134163">doi:10.1126/science.1134163</a>\]

Exposition:

* [[Dmitri Tymoczko]]: *[Mathematical Moments: Putting Music on the Map](https://www.ams.org/publicoutreach/mathmoments/mm57-music-podcast)*, AMS News & Outreach (July 2006) \[<a href="https://www.ams.org/samplings/mathmoments/podcast-mom-music.mp3">mp3</a>\]

* Mattia G. Bergomi: *Musical modeling through graphs and orbifolds* (2014) \[<a href="http://repmus.ircam.fr/_media/moreno/MMIM_Bergomi_Tonnetz.pdf">pdf</a>\]

* Jon Latané: *[Topologica: Jazz, Orbifolds, and Your Event-Sourced, Flux-Driven Dream Code](https://medium.com/fully-automated-luxury-robot-music/topologica-jazz-orbifolds-and-your-event-sourced-flux-driven-dream-code-f8e24443a941)*, blog post (2017)
