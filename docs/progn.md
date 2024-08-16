- [Why?](#org0da8936)
- [How to program?](#org518ad82)
- [Social aspects](#org64ee4b1)
- [Imperative crap](#org9cb1925)
- [Understanding the &ldquo;whys&rdquo;](#org0a85646)
  - [Machines languages](#org745a212)
  - [C](#org157ce79)
  - [The C-like syntax](#orgfeccbc3)
  - [Calling conventions](#org23eca9f)
  - [C++](#orgd1dccfb)
  - [Java](#org5bb9042)
  - [Ada](#orgd471401)
  - [Rust](#orgb5aa0b8)
- [Psychological aspects](#org0f3b5c4)
- [The &ldquo;right understanding&rdquo;](#orgc37de34)
- [The most important thing](#orgfd382d5)
- [Bullshit, bullshit everywhere](#org77e452a)
  - [TTD](#org98eb99a)
  - [Agile](#orgf665938)
  - [&ldquo;Safe&rdquo; languages](#org3629827)

Just like *Arnold* built his body, in vain, and *Tyson* built his body and skills, also in vain, we are laboriously building our &ldquo;less wrong&rdquo; and presumably as accurate as possible &ldquo;inner representations of *What Is*&rdquo; within our brains. In vain, all the same.

This is just the same kind of a biological process based on systematic repetition and the resulting *temporary* transformations of the relevant cell clusters, only to disintegrate later, in accordance with the Buddha&rsquo;s teaching.

This does not mean, however, that we (and them) should not have done it.


<a id="org0da8936"></a>

# Why?

Why am I writing this and keeping it inside a project? Because we have to be at the same level of understanding, so our communication will be clear and meaningful.

To actually have that *&ldquo;active recall&rdquo;* meme (hi, Cal), one has to develop his own proper (which actually corresponds to some aspects of *What Is*) *intuitive* (in principle, without all the minute details) understanding of how things are *Out There* and *why*.

One more time &#x2013; you don&rsquo;t have to memorize all the mostly irrelevant details (and be very proud of yourself, just like most of C++ or Java *coders* are), but have to learn *the underlying principles*, which explains out the *whys*, along with proper generalizations and common reccuring patterns (&ldquo;standard idioms&rdquo;) which underlay *all* programming languages.

This, by the way, is how one deeply and truly understands mathematics &#x2013; by tracing all the properly captured and *properly generalized* mathematical abstractions back to the particular aspects of underlying reality, from which they have been captured.

The same universal (to the Mind of an external observer) principle is required for any proper understanding, including CS and programming. This is how the Buddha himself abstained his realizations &#x2013; reducing everything back to *What Is*.


<a id="org518ad82"></a>

# How to program?

Well, you *learn things as they [really] are* and then *just do the right thing*. These &ldquo;laws&rdquo; are as old as the Buddha.

The problem is, as usual, that the reality has been completely (and many times) distorted by mountains, literally whole Himalayas, of meaningless verbiage, written and spoken.

Every single degen nowadays is either an AI researcher or a &ldquo;software developer&rdquo;, and every single one writes some crappy pop-sci books for low IQ audiences (hi, Cal).

Books are broken beyond repair. We won&rsquo;t have more Steppenwolves or Zen and Arts.


<a id="org64ee4b1"></a>

# Social aspects

Just like it is with all other social movements (abstract social constructs, mass-hysterias and organized religions) most of things you see and hear is an utter *bullshit*.

Young autistic people usually hit this wall very early &#x2013; *&ldquo;all these people cannot be wrong, so may be it is me who is wrong&rdquo;* &#x2013; and damage their own self-esteem for nothing.

Yes, all these people are wrong most of the time. We have seen this *literally everywhere*.

Every single stroke of a brush, every single color, every stone within Egyptian temples and pyramids were made &ldquo;according to absolutely proper and infallible reasons&rdquo;. They did everything according to the current social norms and the current social consensus.

Guess what? It is all bullshit (well, just nice traditional *art forms*).

Do you thing &ldquo;programming&rdquo; is different? Why would it be?


<a id="org9cb1925"></a>

# Imperative crap

There are two kinds of programmers &#x2013; with background in mathematics, and mathematically ignorant. The former gave us the whole *LISP* and *ML* traditions (with the *CLU, Emacs* and *Scheme* &ldquo;sects&rdquo;), while the later sold us their imperative crap (think of an *army training grounds* versus *a math department*).

Before programming has been established as a &ldquo;learn by doing&rdquo; (one has to actually *practice it*, like boxing, not just watch or read) and &ldquo;just do it [yourself]&rdquo; discipline, *theoreticians* gave us *ALGOL* for an *imperative, procedural (structured)* programming.

The goal was sound and noble &#x2013; to develop a general purpose *higher-level* (higher than and more general that a particular machine architecture) programming language (to express algorithms).

The only problem was that this family of languages has no working implementations used by anyone.

Another ultimate *virus* (which seemingly infected *both* Stroustrup and Gosling) was *SIMULA-68* &#x2013; another language based on an idiotic &ldquo;Platonist&rsquo;s&rdquo; view of the world, where everything is an hierarchy of &ldquo;objects&rdquo;, just like it is in an army), ignoring *Smalltalk* and *CLOS* (which did everything &ldquo;just right&rdquo;).

When you see or hear the word &ldquo;simulation&rdquo; being used, watch out for a liberal arts &ldquo;education&rdquo; memes and general stupidity. Simulations have exactly the same relations with reality as cartoons or stories, (even more distant, being at a completely different level from *What Is*.


<a id="org0a85646"></a>

# Understanding the &ldquo;whys&rdquo;

We used to program particular machines (architectures) in a corresponding &ldquo;machine language&rdquo;, using a form of *human-readable* syntax called an &ldquo;assembly language&rdquo;.

We have to understand the machine (CPU and memory) architecture before we can write a program.

The CPU registers, their sizes, the &ldquo;stack&rdquo;, the memory &ldquo;layout&rdquo; (visible to a program) and the memory access (alignment, etc).

From these early days up till now we still have the notions of a &ldquo;machine word&rdquo;, lets say, (the width of a &ldquo;pointer&rdquo; (an address) and *therefore* of a value on the &ldquo;stack&rdquo;, which has to be able wide-enough to store &ldquo;absolute&rdquo; addresses).

The fundamental (for a machine) notions of &ldquo;call by value&rdquo; (creating a copy) and "call by reference (an copying an address of the value) are still out there.

The traditional memory &ldquo;layout&rdquo; of *the code segment, the data segment, heap and stack* is still around. Modern OSes just &ldquo;emulate&rdquo; it.

Understanding &ldquo;what is&rdquo; and &ldquo;why it is the way it is&rdquo; is *the proper understanding*, from which everything follows.


<a id="org745a212"></a>

## Machines languages

A CPU is an *interpreter* (an instance of a *Universal Machine*) for a particular &ldquo;instruction set&rdquo;, implemented in a hardware.

Generally, each instruction has its particular *numeric code*, and an associated human readable (mnemonic or textual) form.

The programmers of the past just wrote sequences of &ldquo;commands&rdquo; to a CPU, using machine instructions that the particular CPU &ldquo;understands&rdquo; (is able to interpret).

All the hardware details (of widths, number representations, encodings) has to be learned beforehand.


<a id="org157ce79"></a>

## C

*C* was a struck of a genius &#x2013; it is a thin layer of seemingly proper abstractions (ADTs) on top of [potentially] *any* machine architecture, so thin that we could literally *see through it* the workings of a machine. *This* is why *C* was a &ldquo;revelation&rdquo; at the time.

There is, however, some crucial things to understand.

The types were not *mathematical sets (which corresponds to abstract number systems)* but subsets &ldquo;bounded&rdquo; by hardware, just like it is within hardware itself.

The general notion of an *ordered sequence* (terminated by a distinct *stop-marker*) has been borrowed from molecular biology (and early LISPs).

It was intentionally a &ldquo;small language&rdquo; (compared to PL/1) with a *lightweight syntax*, and just a few &ldquo;chosen&rdquo; syntactic forms.

The later standards partially enforced the &ldquo;declare before use&rdquo; principle.

And this was basically it. No notion of proper *Algebraic Types*, no proper support for *higher-order functions*, crappy *enums*, no proper macros (just &ldquo;primitive&rdquo; pre-processor directives), no generics &#x2013; just a &ldquo;higher-level language &#x2013; some *proper generalizations* over an assembly languages&rdquo;.

Notice that *back then* there were noting like multi-byte encodings, &ldquo;threads&rdquo;, even of a &ldquo;shared state&rdquo; (shared libraries has been developed much later). There were no notion of &ldquo;multi-processor multitasking&rdquo;.

The means of encapsulation of the state was a &ldquo;process&rdquo; (a whole statically-linked and properly isolated binary being partially loaded into memory).


<a id="orgfeccbc3"></a>

## The C-like syntax

All the crappy &ldquo;cavalierman&rdquo; imperative languages share some form of a C-like syntax &#x2013; C++, Java, and fucking Javascript.

Sane *academic imperative languages*, such as *Ada*, tend to the original (verbose and detailed) ALGOL syntax. The designers of *Ada* even made this into a proper principle &#x2013; no syntactic ambiguity is allowed (with a clear distinction between *statements* and *expressions*), at the cost of some additional verbosity.

It is funny that *Ada*, being a &ldquo;military language&rdquo;, is actually an *academic* language (DOD and DARPA just paid for it), while stuff which has been sold to us as &ldquo;profound&rdquo; (C++, Java) has been created by literal incompetent and unqualified &ldquo;cavaliermen&rdquo;.

Yes, the &ldquo;familiar constructs&rdquo; and &ldquo;the feel of it&rdquo; is what sells, but there are other considerations and evolved (discovered) patterns. The fact that *Python* is eating out the world is the proof (by example) that a clean and highly polished syntax maters *a lot*.

People who publicly issue statements like &ldquo;the syntax does not matter&rdquo; are plain incompetent idiots. Java would be **way less hated by smart people** if its designers would give some considerations to the syntax.

Modern C++ is righteously hated partially due to an inconsistent and incomprehensible syntactic vomit - a sign of a low-effort crap (adding shit later in a rush).


<a id="org23eca9f"></a>

## Calling conventions

Every machine supports &ldquo;procedural programming paradigm&rdquo; and has a built-in notion of a procedure.

How exactly the parameters are passed (which registers are being used) is defined my a specification for a particular CPU architecture.

What is allocated on the stack and what is allocated on the heap is defined by so-called *ABI*, which is defined by an OS implementers and the tradition.

The world is running on so-called *C ABI*, but there is not so much due to *C* in it. It is so happen that when objects were actually implemented (in C++ runtime), the address of the &ldquo;self&rdquo; has to be passed as a &ldquo;0th parameter&rdquo;, and thus placed on the stack before all the actual argument values.

Thus all the modern imperative languages &ldquo;follow&rdquo; the calling conventions from the past for compatibility (with an OS/CPU combo) reasons.

Understanding the &ldquo;memory model&rdquo; (the stack, the heap and the procedure calling conventions) is still essential, to see the &ldquo;whys&rdquo; behind what Java, lets say, (or C++) do.


<a id="orgd1dccfb"></a>

## C++

The &ldquo;C with classes&rdquo; (and structs with methods) was really nice and indeed a &ldquo;++&rdquo; to C.

Then something went wrong. Nowadays people would blame &ldquo;the C legacy&rdquo;, while, in fact, it is reluctance to restrict the possible behavior of pointers and references, in exactly the same way that &ldquo;Simple Typing&rdquo; restricted the original Lambda Calculus to get rid of paradoxes.

Modern C++ is a *dogmatic talmudism*, if you remember the old-speak. It takes huge amount of resources to make it just work (Google Chrome, JVM).

Fuck it. Use Rust or Ada (unfortunately, both lack high quality libraries for almost everything. Rust has a lot of amateur low-effort crappy crates).

Not having proper [parameterized] Algebraic Types and Type-Classes or Traits is a sign of a crappy imperative language built by *unqualified*. Adding them later *ad-hook* resulted in abominations like Java Generics or the STL.


<a id="org5bb9042"></a>

## Java

I would not call names on James Gosling, but we have to admit that he was *ignorant* of every single development in the LISP, ML and Functional programming traditions, and ignored and perhaps even fired *the* Guy Steele &#x2013; an expert in programming language syntax and semantics &#x2013; so now we have to say everything two times (&ldquo;get the papers, get the papers&rdquo;).

It was well-understood back in *the late 80s and the early 90s* that strong typing is *&ldquo;the must&rdquo;* and that the most of the types can be systematically and soundly *inferred*, *at least on the other side of an assignment* statement.

We have to admit that the two fundamental ideas &#x2013; to eliminate the &ldquo;naked pointers&rdquo; (and to *implicitly use references*), and to compile to an intermediate bytecode, which, in turn, can be easily mapped to almost any CPU instruction set (a machine architecture) &#x2013; were great. He is definitely a very good *engineer* and a mediocre and *unqualified* programming language designer.


<a id="orgd471401"></a>

## Ada


<a id="orgb5aa0b8"></a>

## Rust

Rust did *a lot* of the fundamental things (for an imperative language) just right.

We could even call it a *&ldquo;mostly imperative language&rdquo;* (my term), just like *Scheme* or *Ocaml* or *Scala3* are, definitely, *mostly functional languages*.

At even a higher level, composition of *traits* (instead of rigid &ldquo;inheritance&rdquo; hierarchies), extension methods, clear distinction between interfaces an implementations is an obvious &ldquo;right thing&rdquo; to do.

Lifting the *lifetimes* into the type-system and restricting and *formalizing* the behavior of *references* (at most one mutable reference at a time, which is an implicit property for *refs* in functional languages) is Rust&rsquo;s distinct, unique innovation.


<a id="org0f3b5c4"></a>

# Psychological aspects

Just like any other complex social systems (markets, lets say) everything is actually &ldquo;driven by *psychology*&rdquo; and human emotions (*neuro-modulators*), not &ldquo;pure rationality&rdquo;, logic and reason.

Just like the markets in actual reality are NOT *&ldquo;efficient&rdquo;*, the languages (and designs) which most people are using are not &ldquo;rational&rdquo;, leave alone &ldquo;optimal&rdquo;.

People do what they *feel like doing*, not what is rational to do.

This is why we have C++ and utter fucking abominations like *PHP, Java* or *Javascript* at the very top rows of statistical reports.


<a id="orgc37de34"></a>

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


<a id="orgfd382d5"></a>

# The most important thing

The most important thing is to develop and rely on *your own intuitive understanding*, based on your own &ldquo;realizations&rdquo; from experience (by doing!) not on what some narcissistic asshole is saying on the internet, youtube or some imageboard full of incompetent amateurs.

This is *the only way*. The way of the Buddha himself (who explicitly proclaimed that everything is based on &ldquo;the right understanding&rdquo; [of /What Is/]).


<a id="org77e452a"></a>

# Bullshit, bullshit everywhere

> &ldquo;Bullshit, bullshit, bullshit&rdquo;. &#x2013; K-PAX

A 400+ pages books to maximize margins. Hours-long talks on YouTube about subjects which could be explained on a half of a page. Torrents of a meaningless vomit-like verbiage everywhere.

There is always some deep underlying principles behind each meme, which make it work (somehow better than without it). It is these principles which have to be realized and understood. Everything else is bullshit.


<a id="org98eb99a"></a>

## TTD

*Focus on high-level abstract interfaces from the start*. This is the principle that *actually* makes TTD (done right) useful.

One has to *prototype /with /tests and stubs* &#x2013; functions has to return dummy values but the actual interfaces and the tests has to be real.

This *practice* develops the habit of focusing on what is actually important, and think about *abstraction barriers* and data flows.

Then comes data structures (a representation). Data dominates, the program almost writes itself when the right Algebraic Data Types has been chosen.

So, set up your declarative testing DSLs (a-la `Scalatest`) first.


<a id="orgf665938"></a>

## Agile

Nothing can be a substitute for design effort. *&ldquo;The sooner you jump into coding, the longer will it take&rdquo;*. Agile is NOT a substitute for a proper *top-down design* (a problem domain decomposition).

The principle behind non-bullshit &ldquo;agile&rdquo; is a *quick, spiral-shaped process of complete (Always Be Compiled, &ldquo;all tests passed&rdquo;) iterations, so your program is always in a /consistent*, stable state.

Again, this is actually a *spiral*, not a loop, even it looks like from a particular (perpendicular) point of view. The *completeness* of an &ldquo;iteration&rdquo; is the they. Keeping them small just a follows.

It makes *inevitable (in a search process of &ldquo;trial-and-error&rdquo;) &ldquo;back-tracking and restarts&rdquo;* frequent and less painful.


<a id="org3629827"></a>

## &ldquo;Safe&rdquo; languages

This is the &ldquo;last 10% of the code takes *another 90%* of the time&rdquo; principle.

Absence of certain classes of subtle bugs pays off in the overall time of developmet.

Programs is &ldquo;type-safe and memory-safe languages&rdquo; take way less time to stabilize (once it compiles it works without &ldquo;surprises&rdquo;) and are easier and faster to *change* maintain.
