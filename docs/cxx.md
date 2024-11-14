- [No idea how big it is](#orgfdf9061)
- [Expectations vs. reality](#org38fc5b5)
- [Nobody ever got fired for choosing C++](#org05f2705)
- [Programming in terms of implementations](#orge1d202c)
- [Separation of concerns, delegation to cope with complexity](#orgf99b40e)
- [Everything should go into the library code](#org68172aa)
- [Modern ideas](#org0ed94d3)



<a id="orgfdf9061"></a>

# No idea how big it is

Just as Stroustrup (originally an incompetent and ignorant narcissistic asshole) used to brag &#x2013; C++ is literally everywhere.

This, however, does not mean that this is a good language, and especially that everything has been done &ldquo;just right&rdquo;. Not even close.

Advanced codebases like LLVM and Clang (with all the libraries), which Apple and Google are using in production, so they &ldquo;invest&rdquo; a lot of costly human resources in it.

The most widely used software would easily be `libstdc++.so` (with `libm.so` and `libc.so`, of course).

Most of the language runtimes, notably the *JVM*, all actually used web browsers, most of the PC games,

The classic languages, however (both the LISP and the ML families), are using C to implement the language runtimes and parts of standard libraries. Neither objects nor &ldquo;++&rdquo; is required.

Almost everything from Google, Microsoft and Facebook, including their internal codebases.


<a id="org38fc5b5"></a>

# Expectations vs. reality

The famous (really) `bisqwit` video about *how C++ is an actual improvement over C*

<https://www.youtube.com/watch?v=kdlIlIIHCz0>

shows us a highly over-simplified and idealized world, in which C++ is just *does the right thing*.

The problem, however, is that everything else &#x2013; an *imperative* mix of OOP and STL and concurrent mutable data access is an utter crap and a major conceptual disaster. It has been shown more than once that these fundamental notions does not mix in principle.

Add to this the fact that most of C++ code rely on a leaky abstractions, shared mutable state and threading under a preemptive multitasking, and realize that it is a miracle that everything &ldquo;works&rdquo; somehow.

The &ldquo;secret&rdquo; is that time (amount of man-hours) and effort spent on coding and debugging is enormously wasteful.


<a id="org05f2705"></a>

# Nobody ever got fired for choosing C++

Because the language is such a crap, literally millions of a top-tier, very expensive man-hours has been spend on compilers and tooling. The whole codebases (LLVM) has been created to systematically manage complexity, idiosyncrasies and nasty corner cases of C++.

The fact that several competing C++ shops are improving and maintaining a shared C++ implementation (LLVM-based `clang, libcxx, libcxxabi` and the tooling) has to tell you how *bad* things actually are. The whole industry is struggling to make something that actually works.

The result, however, is spectacular, similar to the achievements of modern applied biology. The current Chrome browser (which is arguably the most advanced and the most complex widely used C++ codebase) is being compiled (and then shipped) with current stable `clang` and it just works. Android and IOS are being compiled with `clang` too.

My *Gentoo* builds work too.


<a id="orge1d202c"></a>

# Programming in terms of implementations

This is &ldquo;the C curse&rdquo;.

Machine types instead of proper abstractions.


<a id="orgf99b40e"></a>

# Separation of concerns, delegation to cope with complexity

In theory, recompiling the old code with a new compiler against the stable interfaces of libc++ would yield not just efficiency and performance gains but even support of new processor architectures.

Google learned this lesson the hard way and now it uses mainstream Clang.

Not a coincidence that a standard library comes with the compiler

Hardware primitives, support for concurrency (atomics, fences, locks), etc.


<a id="org68172aa"></a>

# Everything should go into the library code

There is a general principle which states that a well-designed language has to be small, even minimal, with a set of orthogonal but complementing features, allowing almost everything to be implemented in the libraries. `Scala3` and the whole of the `ML` family of languages are exactly like this. So was the original `C`.

`C++` introduced (due to ignorance) the fundamental and unsolvable in principle complexity of mixing of *mutation of objects with have a shared state*, so endless complications (over naive simplicity and cleverness of C) followed.


<a id="org0ed94d3"></a>

# Modern ideas

-   if one has to write a full generic type, one is programming at a low-level.
-   type-inference is a must have, period.
-   literal suffixes for numeric types
-   overloaded literals (from Haskell)
-
