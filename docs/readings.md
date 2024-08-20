- [The Architecture Of Complexity](#org13ca162)
- [Discrete-time signal processing (Alan V. Oppenheim)](#org27de9c2)
- [Time series](#org227d4c0)
- [Barbara Liskov (both CLU and Java books)](#orga798c01)

The major task is to extract knowledge and transfer it into `org-roam2` &ldquo;cards&rdquo;, as a sort of *&ldquo;knowledge base&rdquo;*.

Clear, concise, mathematically rigorous definitions of abstract concepts.


<a id="org13ca162"></a>

# The Architecture Of Complexity

This is, perhaps, the most important paper (for actually smart people).

The date is **1962**, so this is just 2 years after John McCarthy published his LISP paper for the first time.

All the fine people supposedly have read this, B. Liskov, Guy L. Steele, Gerald Sussman, P. Norvig, SPJ.

It has been written by a theoretician. Theoreticians, in general, does not care about precision and rigor, so every single assertion could be independently verified by anyone, but they sometimes have so-called &ldquo;insights&rdquo; and properly capture important generalities.

This short paper basically says that you have to design your program as a set of *layered embedded DSLs*, so it **will be** as robust as possible and **will be** developed *faster*, if one uses &ldquo;bottom-up process&rdquo; (*after* &ldquo;top-down&rdquo; problem domain decomposition) in prototyping.

The notion of &ldquo;stable intermediate forms&rdquo; is, indeed, *universal*. So is the notion of *partitioning* and of a *hierarchy of layers*, which is what a complex system decomposes into (atoms, molecules, aminoacids, proteins are obviously form distinct layers and have actual &ldquo;abstraction barriers&rdquo; at each level).

Another universal and fundamental notion in this short paper is of a *heuristic-based back-tracking search as a universal strategy of problem-solving*. He did not use these terms, but he talks abot &ldquo;trial-and-error search process&rdquo; and &ldquo;*selectivity* based on heuristics and rules of thumb&rdquo;.

This is exactly what happens in human societies. Instead of so-called &ldquo;free will&rdquo; individuals are just bouncing around within their social, economic and genetic *constraints*, trying this and that and &ldquo;seeing what sticks&rdquo;.

But the &ldquo;stable intermediate forms&rdquo; (which are *reused* (!) and your own data-types, functions, modules) and the layered architecture (of embedded DSLs) was a *revelation*.

LISP guys got it. They even got *homoiconicity* from cell biology. Everything &#x2013; enzymes, which are just particularly folded proteins, and the &ldquo;data&rdquo; (other proteins) &#x2013; has been made from *sequences* of the same 20 aminoacids.

The only thing that &ldquo;missed&rdquo; is the subtle notion from Haskell, where the monadic code *form actual membranes* with &ldquo;pumps&rdquo; and &ldquo;portals&rdquo;, and the I/O code (and other effects) tent to stay &ldquo;at the edges&rdquo;.

*Every Monad defines and implicit abstraction barrier* (using Kleisli arrows, which we call `return` or &ldquo;lifting&rdquo; in general), but his is another story, this time by me.

[The Architecture Of Complexity (Herbert A. Simon, 1962)](https://faculty.sites.iastate.edu/tesfatsi/archive/tesfatsi/ArchitectureOfComplexity.HSimon1962.pdf)


<a id="org27de9c2"></a>

# Discrete-time signal processing (Alan V. Oppenheim)

The most dense books, but the fundamental concepts and proven techniques has to be extracted from them. The author is one of the pioneers in this field.

This, by the way, is the essence of learning &#x2013; to extract the right understanding from poorly or messy written books.


<a id="org227d4c0"></a>

# Time series

Very difficult to find a definitive, concise well-written non-bullshit book.

My general heuristic is to look for something from the *MIT Press* first.


<a id="orga798c01"></a>

# Barbara Liskov (both CLU and Java books)

&ldquo;Abstraction barriers&rdquo; via abstract data types (in CLU) and Abstract Interfaces (in Java) is the true essence of programming as a discipline of managing complexity. Period.

She stated everything clear and concise, within just a few pages &#x2013; the art of writing which has been forever lost.

Yes, just a few pages is all you need.
