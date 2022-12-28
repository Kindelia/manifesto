The Kindelia Manifesto
======================

What is the true nature of computation? A hundred years ago, humanity answered that very question, twice. In 1936, Alan
invented the Turing Machine, which, highly inspired by the mechanical trend of the 20th century, distilled the common
components of early computers into a single universal machine that, despite its simplicity, was capable of performing
every computation conceivable. From simple numerical calculations to entire operating systems, this small machine could
compute anything. Thanks to its elegance and simplicity, the Turing Machine became the most popular model of
computation, and served as the main inspiration behind every modern processor and programming language. C, Fortran,
Java and Python, are languages based on a procedural mindset, which is highly inspired by Turing's invention.

Yet, the Turing Machine wasn't the only model of computation that humanity invented. Albeit a less known history, also
in 1936, and in a completely independent way, Alonzo Church invented the Lambda Calculus, which distilled the common
components - not of machines, but of different branches of math - into a single universal language that was capable of
modeling every mathematical theory. What was surprising, though, is that this language, unexpectedly, could also perform
computations. The same algorithms that could be computed by Turing Machines procedurally, could also be computed by the
Lambda Calculus, through symbolic manipulations. The idea of using the Lambda Calculus for computations inspired the
creation of an entire new branch of programming, which we call the functional paradigm. Haskell, Clojure, Elixir and Agda,
are languages based on the functional mindset, which is highly inspired by Church's invention.

If both, Turing Machines (and procedural languages) and the Lambda Calculus (and functional languages), are capable of doing
computations, then which mindset is the "right one"? When it comes to raw capabilities, neither. Still on the 20th century, it
was proven that, when it comes to computability, Turing Machines and the Lambda Calculus are equivalent. Every problem
that one can solve, can also be solved by the other. That insight is known as the Church-Turing thesis, which
essentially states that computers are capable of emulating each-other. If that was completely true, then the choice
wouldn't matter. After all, if, for example, every programming language is capable of solving the same set of problems,
then what is the point in making a choice?

Yet, while the Church-Turing hypothesis makes a statement about computability, it says nothing about computation. In
other words, a model can be inherently less efficient than other. Historically, procedural languages such as C and
Fortran have consistently outperformed the fastest functional languages, such as Haskell and Ocaml. Yet, languages
like Haskell and Agda provide abstractions that make entire classes of bugs unrepresentable. Historically, the
functional paradigm has been more secure. Of course, these factors can vary greatly, but the point is that this notion
of equivalence is limited, and there are impactful differences.

In 1983, Stephen Wolfram introduced the Rule 110, an elementary cellular automaton that has been shown to be as capable
as both. Wolfram argues that this model is of fundamental importance for math and physics, and that a new kind of science should emerge from
its study. These claims were met with harsh skepticism; after all, if all models are equivalent, what is the point?
Yet, we've just established that, while equal in capacity, different models result in different practical outcomes.
Perhaps there isn't a new branch of science to emerge from the study of alternative models of computation, but what
about the design of processors and programming languages?

A model of computation has a significant impact on the way we design our languages, and several of their drawbacks can
be traced down to limitations of the underlying model. For example, the parallel primitives of the procedural paradigm,
mutexes and atomics, provide a contrived, complex solution to multi-threaded synchronization. As a result, parallelism
is generally considered hard, and programmers still write sequential code by default. Similarly, security isn't natural
to the procedural paradigm. Global state, mutable arrays and loops generate an explosion of possible execution paths,
edge cases and off-by-one errors that make absolute security all but impossible. Even highly audited code, such as
OpenSSL, is often compromised by out-of-bounds exploits. The functional paradigm handles both issues much better: there
is an enourmous amount of inherent parallelism on functional programs, and logic-based type systems make entire classes
of bugs unrepresentable. But if that is the case, then why are functional programs still mostly single-threaded, and
bug-ridden? And why isn't the functional paradigm more prevalent?

A strong factor, we argue, is performance issues. As much as the Turing Machine, and, thus, the procedural paradigm as a
whole, is inadequate for parallelism and security, the Lambda Calculus, and the functional paradigm as a whole, is
inadequate for efficient computations. The fundamental operation of the Lambda Calculus, substitution, may trigger an
unbounded amount of copies of an unboundedly large argument. Because of that, it can not be performed in a bounded
amount of steps, and, thus, there isn't a physical mapping of substitution to real-world physical processes. In other
words, substitution isn't an atomic operation, which prevents us from creating efficient functional processors and
runtimes. Attempts to solve the issue only pushed it into other directions, such as the need of shared references, which
inhibit parallelism, or garbage collection, which isn't atomic. The failure of the functional paradigm to achieve
satisfactory efficiency impacted its popularity, which, in turn, lead to tools like formal proofs to never catch up.

This raises the question: is there a model of computation, which, like the Turing Machine, has a reasonable physical
implementation, and yet, like the Lambda Calculus, has a robust logical interpretation? In 1997, Yves Lafont proposed a new
alternative, the Interaction Combinators, on which substitution is broken down into 2 fundamental laws: commutation,
which creates and copies information, and annihilation, which observes and destroys information. In a sense, this may
resemble SKI combinators, but that isn't a good analogy, since SKI combinators still include non-atomic operations: K
may erase an unboundedly large structure, and S may copy an unboundedly large structure. The charm, and elegance, of the
Interaction Combinators is that its reduction laws are truly atomic: each operation can be completed in a constant
amount of steps, and has a clear physical mapping. Not only that, they're inherently parallel, in the same sense that
the Lambda Calculus has been claimed to be, in theory, but without the issues that let it to be, in practice.

Interestingly, every aspect that is considered good in other models of computation, is present on Interaction
Combinators, while negative aspects are completely absent. Moreover, both the Lambda Calculus and the Turing Machine can
be efficiently emulated by the Interaction Combinators, while the opposite isn't true. This suggests that, while the 3
systems are equivalent in terms of computability, the Interaction Combinators are more capable in terms of computation.
Under certain point of view, one could argue that both the Turing Machine and the Lambda Calculus are slight distortions
of this fundamental model, caused by human creativity, due to our historical intuitions regarding machines and
mathematics. Perhaps machines and substitutions aren't as fundamental as we think, and some alien civilization has
developed all its mathematical theories and computers based on annihilation and commutation, with no references to the
Lambda Calculus, or the Turing Machine.

We, at the Kindelia Foundation, hold the view that Interaction Combinators are a more fundamental model of computation,
and, consequently, that computers, processors and programming languages inspired by them would offer tangible benefits
compared to the ones we built based on Turing Machines and the Lambda Calculus. The Kindelia Foundation was created to
research this new model of computation, and, through the different mindset it brings, catch insights that will let us
produce groundbreaking technology that will push humanity towards the next level of computational maturity.
