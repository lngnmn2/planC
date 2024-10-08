I am already quite an old guy, at least other people threat me as such. This means that I have tried (and failed) quite a lot of things already, and have got in return something what they call &ldquo;experience&rdquo;. At least I have read some. Here, there.

There is always that archtypical character in all the golden era kung-fu movies &#x2013; a &ldquo;master&rdquo; with a long hair and a long beard, who knows all the kung-fu styles. I am more or less like that &#x2013; I know all the kung-fu styles (of CS) worth knowing.

When one &ldquo;studies&rdquo;, lets say, Indian or Buddhist philosophy (well, this is a *vast* subject) there is a distinct, recurring (again and again) common pattern &#x2013; the early intuitive and less subjective, based on a shared experience teachings (of the ancients) are getting systematically destroyed and transformed into incomprehensible verbiage vomit of &ldquo;modern&rdquo; abstract terminology.

All the &ldquo;famous commentators&rdquo; just introduced more and more &ldquo;primitive&rdquo; abstractions (which they think off as refinements) and turned the teaching, pure and simple, into a scholastic shitfest. Moreover, most of them do not know when to stop, and are keeping producing more and more &ldquo;spiritual&rdquo; verbiage. The most brilliant J. Krishnamurti became a chatterbox.

There is *always*, however, an end of a search, the end of knowledge, when the whole &ldquo;maze&rdquo; has been explored (and nothing more &ldquo;real&rdquo; than the maze itself has been found). The Buddha is the most notable example of the one who stopped searching after he realized [the true Nature of] *What Is*.

The rare *correct* intuitive insights of the Upanishads has been turned by &ldquo;commentators&rdquo; into volumes of abstract doctrines, the teaching of the Buddha has been turned into ritualistic mumbling and reduced to repetitive rituals, just like Brahmanas turned everything into endless sacrifice rituals for their own socail status and profits.

You may be thinking that such things (social movements which the pattern captures) happen only in the distant past, and now we all are rational and even &ldquo;scientific&rdquo; instead of speculative and vaguely abstract. Hardly.

The early teachings of what we call &ldquo;Computer Science&rdquo; has been ruined and transformed (by &ldquo;creative&rdquo; idiots) into incomprehensible abstract bullshit in exactly the same way, turning everything into a verbose syntactic vomit of unnecessary, redundant abstractions (which is the root of all evil).

This is not an exaggeration in the least. By the late 90s, with the emergence of the Haskell 98 report (and the R5RS standard prior to that), as well as the refinement of the ML (and then Ocaml) with modules and functors, *everything* out there has been well-understood and &ldquo;solved&rdquo;.

The abstract interfaces, categorized as Algebraic Types &#x2013; a proper generalization of ADTs, and corresponding small modules, which hide all the (representation and implementation) details, has been placed at the center of what a non-bullshit programming (the science of managing complexity) is really.

It has been realized (at least by some of us) that the &ldquo;composition of individual traits&rdquo;, defined as type-classes or traits (which is a *set union* relation), NOT a strict inheritance hierarchy (which is a *set-subset relation*) is the most fundamental notion. The set-subset (class) hierarchies are too rigid and it is NOT how biology works. Composition is "more&rsquo; universal.

It is not a random coincidence that composition of pure functions (of matching types) in a lazy (call-by-need) language [and in the Lambda Calculus itself] could ONLY be implemented as *nesting* of expressions. Composition *is* nesting. This is the most esoteric notion I have discovered. *Nesting* is *how* hierarchies are emerging.

Some *abstraction barriers* are actually very real &#x2013; individual atoms (ions) and small molecules are an abstraction barrier for *Life Itself*. Everything in what we would call Molecular Biology is clearly separated by abstraction barriers &#x2013; atoms and ions, molecules, aminoacids, etc. It is no surprise that this very notion is at the core of [less] complex systems.

In the modern parlance, representation and implementation of atoms are completely hidden (inaccessible) behind their [abstract] interface, and is irrelevant for Life Itself.

At a higher level, each individual cell, which *all* have been developed from (are *copies* of) a single zygote, is a &ldquo;message-receiving actor&rdquo; (the Erlang guys were definitely onto something!) which gets its &ldquo;messages&rdquo; from its immediate *environment* (locality), thus &ldquo;being configured&rdquo; to specialize (to exhibit a particular behavior &#x2013; to *become* a cell of a particular kind).

The notion of an *environment*, of a *particular locality* (or more abstractly &#x2013; of a *context*) is a universal one. No process can be comprehended (an existed) separately from its environment (locality) which made it possible. It is not a coincidence that the notion of an environment is implicit (and necessary) for the Lambda Calculus or *any* system of logic.

The *bindings* &#x2013; all the previous &ldquo;results&rdquo; (*all the stable intermediate forms*) is what a &ldquo;surrounding&rdquo; *environment* corresponds to, in logic, in math, in molecular biology, in social systems (language-encoded shared knowledge). The notions of a *scope*, and of a free variable (a *symbolic reference* to &ldquo;an outside&rdquo; of the local context) is just an immediate consequence.

There is nothing accidental or &ldquo;random&rdquo; about (within) the Lambda Calculus. It captures the &ldquo;very essence&rdquo; at the most abstract (most general) level.

From *this* the notion of *layered* hierarchical organization (architecture) &ldquo;naturally&rdquo; arises. The &ldquo;architecture of complexity&rdquo; is, indeed, a nested layers [of abstractions] separated clearly by abstraction barriers (interfaces) &#x2013; cells, tissues, [specialized] organs, [distinct] subsystems, systems. All from a single copy of the same cell (with exactly the same copy of whole DNA), being specialized and &ldquo;configured&rdquo; by its environment (surrounding, neighborhood, locality).

At least 3 distinct *traditions* has been emerged from *the Simply-Typed Lambda Calculus* and ISWIM &#x2013; the ones of SML/Ocaml, Scheme and the most notably, of Miranda/Haskell. Erlang and Scala emerged as schisms of their own.

There are a few distinct &ldquo;patterns&rdquo; which are common of all of these traditions &#x2013; a re-discovered (again and again) minimal subset of special forms in a mostly functional language which is good-enough (even optimal) for everything &#x2013; which what we augment the simple-typed lambda calculus. Technically, the intermediate language of the Glasgow Haskell Compiler, which corresponds to the *System F Omega*, is that &ldquo;universal core&rdquo;.

The notion that a small, simple, base-language has to be extended with *new* data-types has been emphasized by Barbara Liskov and her CLU, while the notion of extending a language with new *special forms* (or embedded DSLs) has been at the core of Common Lisp.

When one is looking at these special forms (and embedded in a LISP specialized macro-DSLs) and is trying to draws the arrows between dots, one (if smart enough) would discover more distinct common patterns. These has been *partially* captured by the algorithm charting techniques from the 70s.

Unsurprisingly, if we add *the structural pattern matching* (on Algebraic Data Types), which all the ML tradition languages have, one will see &ldquo;the complete picture&rdquo; &#x2013; a better branching (more arrows going out). All the &ldquo;special forms&rdquo; are reducible to just a few universal patterns of &ldquo;arrows between dots&rdquo; (to which the Category Theory has arrived by another route).

Since the 90s, the smartest people (who gave us CLU, SML and Haskell) told us, that *this* is good-enough for everything and even that *this* is how to manage complexity and how to compute.

If one knows some very basic cell biology, one would see the very same patterns &ldquo;Out There&rdquo;, just as the early LISP guys did (when freshly discovered the actual structure of DNA was a big deal).

Unlike liberal arts &ldquo;educated&rdquo; people used to babble about &ldquo;boundless creativity&rdquo; (the word-marker of an idiot), we do not have endless structures. Actually, we have *sequences, tree-like structures and a lookup tables*, where a *partial* (and a total) function could be thought off (correctly represented as) a lookup table.

DNA transcription machinery do &ldquo;table lookups&rdquo; and produce sequential structures, which spontaneously fold themselves into &ldquo;stable forms&rdquo;.

Just like the early LISP procedures were made out of LIST structures (nested pairs with a &ldquo;CAR&rdquo; and a &ldquo;CDR&rdquo;), all other basic data structures (*alists*, *trees*) were made from just &ldquo;CONSes&rdquo;. This wasn&rsquo;t a mere coincidence, of course.

The next big idea is *Immutability* of all bindings &#x2013; both *symbol bindings* (in an environment, which were originally just bunch of nested *alists*) and *data bindings*. *Clojure* persued the immutability of bindings to its limit with a great success.

Guess what? Immutable *balanced trees* which represent (and implement) everything else (all the proper non-leaking ADTs), including &ldquo;flat&rdquo; sequences (the actual Machine Types such as arrays are grossly overhyped).

Again, an immutable *binding* (the old terminology was inspired by math and is so much better!) of a symbol to a value or of slots of a record type to a corresponding value is the most fundamental building block, just as in math itself. Unsurprisingly, the molecular structures which constitute the basis of Life Itself are &ldquo;supposed to be&rdquo; immutable (or at least stable-enough).

Then it has been realized that just *product-types, sum-types and function types* are enough for everything. Not just that, but they correspond to the most fundamental shapes &#x2013; sequences and lookup tables (alists), and to the logical notions of `AND` `OR` and `->`, which is, of course, not a random coincidence.

So, one begins to see (and so becomes a &ldquo;seer&rdquo;) the big picture of a small number of the universal &ldquo;forms&rdquo; which underlay almost everything (and the reccuring patterns of &ldquo;dots between arrows&rdquo; one level behind them). *All* your abstract types (ADTs) can be just properly *Algebraic* and even immutable.

And suddenly, someone like me discovered that Monads in Haskell (which is, just a type-class for a simple ADT of a Monoidal composition) corresponds to a the notion of a universal abstraction barrier, or of a cell-membrane.

The really smart guys (around Odersky) were generalized the *for-comprehensions* around Monadic composition, and this is where we are today.

Now, how many people have actually comprehended and realized all this? I know of no one else. You would be the first to learn all this from here.

The classic books about the classic languages are the source of the &ldquo;ancient&rdquo;, first intuitive, and then shared experience-based knowledge (because it properly captures some aspects of *What Is*), just, unsurprisingly, like the seers of Upanishads and the early Buddhists.

*L. C. Paulson. ML for the Working Programmer* is one of such classic books. The *&ldquo;Bird & Wadler&rdquo;* is another one. The most important book of the LISP tradition is *&ldquo;On Lisp&rdquo;* by Paul Graham. *&ldquo;The Armstrong thesis&rdquo;* is another revelation of a truly illuminated sage (here I am showing you *the way*).

Notice that 99.6% of the &ldquo;world experts&rdquo; on HN never heard about these books, and `/g/` can barely read. This means that one could be way ahead of the crowd, if one chooses to follow &ldquo;the right path&rdquo; (of *Brian Harvey* and very few other great teachers).

There are, of course, a few more *classic books*.

Okay, there is a message (a tiny set of infallible principles) from the ancient traditions:

One has to program in a pure subset of a mostly functional language, using layers of embedded DLS, which manipulate immutable values defined by ADTs and small (narrow) Abstract Interfaces, including Monadic ones.

There is the message from an aging kung-fu master:

The ability to properly capture and express a set of relevant concepts from your problem domain as an one-to-one correspondence to a set of high-level abstractions in a pure functional language like Haskell (being defined in a loosely-coupled corresponding modules) allows one to have an executable mathematical model &ldquo;for free&rdquo; (as a by-product of Haskell technically being an executable system of pure logic).

This is how *mathematics itself* has been developed over a millennia &#x2013; by properly capturing and generalizing (abstracting) into mathematical abstractions, developing (extending) appropriate DSLs (notations) as needed.

The simple but fundamental data types (of a particular shape) are good-enough for everything (Clojure and Scala3 proved this postulate by example, with SML and Common Lisp before that).

If one really needs all that machine-level crap one can always rewrite *an already working system* into a crappy imperative &ldquo;implementation language&rdquo; of choice.

One more time: the classic languages like SML and the programming style they encourage are actually the best possible ones, and everything modern is a digression from that math-inspired ideal.

Haskell, miraculously, is still math. Just throw away everything amateur and study and write your extensions (to a language) using the standard library, the way it has been done in it.

One will have a factor of 10 less code (has been shown experimentally in the case of Haskell), dramatically reduced complexity (by reducing everything into a familiar and well-understood math), and less time (money) spent &#x2013; it will basically work once it compiles.

Sounds unreal? This is what a proper philosophy actually does for you.
