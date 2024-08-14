- [How to program?](#orga554b5e)
- [Social aspects](#org8d341c9)
- [Imperative crap](#orgd48830f)
- [Understanding the &ldquo;whys&rdquo;](#org805eae4)
  - [Machines languages](#org4aa95d0)
  - [C](#orga7ee246)
  - [The C-like syntax](#orgbc563f2)
  - [Calling conventions](#org1b9c99a)
  - [C++](#org5b2d796)
  - [Java](#orgbb8de41)
  - [Rust](#org050c49e)
- [Psychological aspects](#org0e7d983)
- [The &ldquo;right understanding&rdquo;](#orge2c8d5d)
- [The most important thing](#org6fed591)

Why am I writing this and keeping it inside a project? Because we have to be at the same level of understanding, so our communication will be meaningful.

To actually have that &ldquo;active recall&rdquo; meme (hi, Cal), one has to develop his own proper (which actually corresponds to some aspects of *What Is*) *intuitive* (in principle, without all the details) understanding of how things are Out There and *why*.

One more time &#x2013; you don&rsquo;t have to memorize all the mostly irrelevant details (and be very proud of it as most of C++ or Java *coders* do), but have to learn *the underlying principles*, which explains out the *whys*, along with proper generalizations and common reccuring patterns (&ldquo;standard idioms&rdquo;) which underly *all* languages.

This, by the way, is how one actually understands mathematics &#x2013; by tracing all the properly captured and *properly generalized* mathematical abstractions to the particular aspects of underlying reality, from which they have been captured.

The same universal (to the Mind of an external observer) principle is required for any proper understanding, including CS and programming.


<a id="orga554b5e"></a>

# How to program?

Well, you *learn things as they [really] are* and then *just do the right thing*. These &ldquo;laws&rdquo; are as old as the Buddha.


<a id="org8d341c9"></a>

# Social aspects

Just like it is with all other social movements (abstract social constructs, mass-hysterias) most of thing you see and hear are *bullshit*.

Young autistic people usually hit this wall very early &#x2013; *all these people cannot me wrong, so may be it is me who is wrong* &#x2013; and damage their self-esteem for nothing.

Yes, all these people are wrong. We have seen this *literally every time*.

Every single stroke of a brush, every single color, every stone within Egyptian temples and pyramids were &ldquo;absolutely proper and infallible&rdquo;. They did everything according to the social norms and the social consensus. Guess what? It is all bullshit (well, just nice traditional *art forms*).

Do you thing &ldquo;programming&rdquo; is different? Why would it be?


<a id="orgd48830f"></a>

# Imperative crap

There are two kinds of programmers &#x2013; with background in mathematics, and mathematically ignorant. The former gave us *LISP* and *ML* traditions (with the *CLU* and *Scheme* &ldquo;sects&rdquo;), while the later sold us their imperative crap (think of an *army training grounds* versus *a math department*).

Before programming has been established as a &ldquo;learn by doing&rdquo; (one has to actually practice it, not just watch and read) and &ldquo;just do it [yourself]&rdquo; discipline, *theoreticians* gave us *ALGOL* for *imperative, procedural (structured)* programming.

The goal was sound and noble &#x2013; to develop a general purpose *higher-level* (higher than and more general that a particular machine architecture) programming language.

The only problem was that this family of languages has no implementations used by anyone.


<a id="org805eae4"></a>

# Understanding the &ldquo;whys&rdquo;

We used to program particular machines (architectures) in a &ldquo;machine language&rdquo;, using form of *human-readable* syntax called an &ldquo;assembly language&rdquo;).

We have to understand the machine CPU and memory architecture before we can write a program.

The CPU register, their sizes, the &ldquo;stack&rdquo;, the memory &ldquo;layout&rdquo; and access.

From these early days till now we still have the notions of a &ldquo;machine word&rdquo;, lets say, (the width of a &ldquo;pointer&rdquo; (an address) and *therefore* of a value on the &ldquo;stack&rdquo;, which has to be able to store addresses).

The fundamental (for a machine) notions of &ldquo;call by value&rdquo; (a copy) and "call by reference (an address) are still out there.

The traditional memory &ldquo;layout&rdquo; of *the code segment, the data segment, heap and stack* is still around. Modern OSes just &ldquo;emulate&rdquo; it.

Understanding &ldquo;what is&rdquo; and &ldquo;why it is the way it is&rdquo; is *the proper understanding*, from which everything follows.


<a id="org4aa95d0"></a>

## Machines languages

A CPU is an *interpreter* (an instance of a *Universal Machine*) for a particular &ldquo;instruction set&rdquo;, implemented in a hardware.

Generally, each instruction has its particular *numeric code*, and an associated human readable (mnemonic or textual) form.

The programmers of the past just wrote sequences of &ldquo;commands&rdquo; to a CPU, using machine instructions that the particular CPU &ldquo;understands&rdquo; (is able to interpret).

All the hardware details (of widths, number representations, encodings) has to be learned beforehand.


<a id="orga7ee246"></a>

## C

*C* was a struck of a genius &#x2013; it is a thin layer of seemingly proper abstractions (ADTs) on top of [potentially] *any* machine architecture, so thin that we could literally *see through it* the workings of a machine. *This* is why *C* was a &ldquo;revelation&rdquo; at the time.

There is, however, some crucial things to understand.

The types were not *mathematical sets (which corresponds to abstract number systems)* but subsets &ldquo;bounded&rdquo; by hardware, just like it is within hardware itself.

The general notion of an *ordered sequence* (terminated by a distinct *stop-marker*) has been borrowed from genetics (and early LISPs).

It was intentionally a &ldquo;small language&rdquo; (compared to PL/1) with a *lightweight syntax*, and just a few &ldquo;chosen&rdquo; syntactic forms.

The later standards partially enforced the &ldquo;declare before use&rdquo; principle.

And this was basically it. No notion of proper *Algebraic Types*, no proper support for *higher-order functions*, crappy *enums*, no proper macros (just &ldquo;primitive&rdquo; pre-processor directives), no generics &#x2013; just a &ldquo;higher-level language &#x2013; some *proper generalizations* over an assembly languages&rdquo;.

Notice that *back then* there were noting like multi-byte encodings, &ldquo;threads&rdquo;, even of a &ldquo;shared state&rdquo; (shared libraries has been developed much later). There were no notion of &ldquo;multitasking&rdquo;.

The means of encapsulation of the state was a &ldquo;process&rdquo; (a whole statically-linked and properly isolated binary).


<a id="orgbc563f2"></a>

## The C-like syntax

All the crappy &ldquo;cavalierman&rdquo; imperative languages share some form of a C-like syntax &#x2013; C++, Java, and fucking Javascript.

Sane *academic imperative languages*, such as *Ada*, tend to the original (verbose and detailed) ALGOL syntax. The designers of *Ada* even made this into a proper principle &#x2013; no syntactic ambiguity is allowed (with a clear distinction between *statements* and *expressions*), at the cost of some additional verbosity.

It is funny that *Ada*, being a &ldquo;military language&rdquo;, is actually an *academic* language (DARPA just paid for it), while stuff which sold to us as &ldquo;profound&rdquo; (C++, Java) has been created by literal incompetent and unqualified &ldquo;cavaliermen&rdquo;.


<a id="org1b9c99a"></a>

## Calling conventions

Every machine supports &ldquo;procedural programming paradigm&rdquo; and has a built-in notion of a procedure.

How exactly the parameters are passed (which registers are being used) is defined my a specification for a particular CPU architecture.

What is allocated on the stack and what is allocated on the heap is defined by so-called *ABI*, which is defined by an OS implementers and the tradition.

The world is running on so-called *C ABI*, but there is not so much due to *C* in it. It is so happen that when objects were actually implemented (in C++ runtime), the address of the &ldquo;self&rdquo; has to be passed as a &ldquo;0th parameter&rdquo;, and thus placed on the stack before all the actual argument values.

Thus all the modern imperative languages &ldquo;follow&rdquo; the calling conventions from the past for compatibility (with an OS/CPU combo) reasons.

Understanding the &ldquo;memory model&rdquo; (the stack, the heap and the procedure calling conventions) is still essential, to see the &ldquo;whys&rdquo; behind what Java, lets say, (or C++) do.


<a id="org5b2d796"></a>

## C++


<a id="orgbb8de41"></a>

## Java


<a id="org050c49e"></a>

## Rust

Rust did *a lot* of the fundamental things (for an imperative language) just right.

We could even call it a *&ldquo;mostly imperative language&rdquo;* (my term), just like *Scheme* or *Ocaml* or *Scala3* are, definitely, *mostly functional languages*.

At even a higher level, composition of *traits* (instead of rigid &ldquo;inheritance&rdquo; hierarchies), extension methods, clear distinction between interfaces an implementations is an obvious &ldquo;right thing&rdquo; to do.

Lifting the *lifetimes* into the type-system and restricting and *formalizing* the behavior of *references* (at most one mutable reference at a time, which is an implicit property for *refs* in functional languages) is Rust&rsquo;s distinct, unique innovation.


<a id="org0e7d983"></a>

# Psychological aspects

Just like any other complex social systems (markets, lets say) everything is actually &ldquo;driven by *psychology*&rdquo; and human emotions (*neuro-modulators*), not &ldquo;pure rationality&rdquo;, logic and reason.

Just like the markets in actual reality are NOT *&ldquo;efficient&rdquo;*, the languages (and designs) which most people are using are not &ldquo;rational&rdquo;, leave alone &ldquo;optimal&rdquo;.

People do what they *feel like doing*, not what is rational to do.

This is why we have C++ and utter fucking abominations like *PHP, Java* or *Javascript* at the very top rows of statistical reports.


<a id="orge2c8d5d"></a>

# The &ldquo;right understanding&rdquo;

Issuing some random imperative &ldquo;commands&rdquo; to a computer (close to a machine level) is NOT the right way to program (that *Forrest Gump* sergeant scene!).

Imperative programming is for sergeants, indeed.

At a &ldquo;math department&rdquo; we want to program by doing [applied] mathematics, with sets, relations, algebraic types and, of course, functions.

Everything has to be a value of some type (including functions), syntactically, everything is an *expression* (which evaluates to a value, including *self-evaluating* &ldquo;literals&rdquo;), every *binding* (both of a symbol or a data-binding) has to be *immutable*, and there is no &ldquo;state&rdquo; anywhere, just structured data (&ldquo;in-a-wire&rdquo; representation).

Uniformity cannot be &ldquo;invented&rdquo;, it is only being discorevered, *emerges* when we do everything &ldquo;just right&rdquo;.

The best &ldquo;mostly functional&rdquo; languages, such as SML, Scheme, Ocaml or Clojure, had all these principles applied.

Haskell is, technically, an executable system of logic (a *declarative* system of notation, which is evaluated by &ldquo;pure substitution&rdquo;).

Ideally, we should to program in Haskell, Scala3 or Rust, depending on what the constraints (including the availability of layered, DSL-based libraries) are.

But knowing (mastering) the underlying universal principles, one could program in *any* language, except, perhaps, PHP and Javascript, due to basic hygiene reasons.


<a id="org6fed591"></a>

# The most important thing

The most important thing is to develop and rely on *your own intuitive understanding*, based on your own &ldquo;realizations&rdquo; from experience (by doing!) not on what some narcissistic asshole is saying on the internet, youtube or some imageboard full of incompetent amateurs.

This is *the only way*. The way of the Buddha himself (who explicitly proclaimed that everything is based on &ldquo;the right understanding&rdquo; [of /What Is/]).
