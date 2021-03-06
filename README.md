# What it is

A bottom-up implementation of Datalog in javascript with [heavy code commentary](http://joyrexus.github.io/datalog.js/). It's short and simple and horribly inefficient. The aim is merely to demonstrate what Datalog is and how it works in principle.


## Wait, what is Datalog?

[Datalog](http://en.wikipedia.org/wiki/Datalog) is a logical query language. It exists somewhere between relational algebra (the formal theory behind SQL) and Prolog, but is closer in motivation to the former than the later. It was invented to apply some of the principles of logic programming to database theory. Its primary addition to the semantics of databases is recursive queries.


## Implementation

Right now every query simply builds up a complete database of facts first, by taking each applicable rule, matching it against the known facts and then adding the solutions (if any) to the existing facts. This is repeated as long as new facts can be added this way and then the database is complete. Now we only need to check if our query unifies with any fact. Sounds not exactly smart? It isn't. But it's simple and easy to understand.


## See also

* [LogPy](https://github.com/logpy/logpy) - logic programming in python.

* [Learn Datalog Today](http://www.learndatalogtoday.org/) - an interactive tutorial designed to teach you the [Datomic](http://datomic.com/) dialect of Datalog. [This video tutorial](https://www.youtube.com/embed/bAilFQdaiHk)    covers similar ground.

* [Relational Logic in JS](http://logic.stanford.edu/dataintegration/chapters/appendix.html) - Genesereth's JavaScript implementation of the core algorithms for relational logic from his book [Data Integration: the relational logic appoach](http://logic.stanford.edu/dataintegration/).

* [The Reasoned Schemer](http://mitpress.mit.edu/books/reasoned-schemer) - The
  goal of the book is to help the functional programmer think logically and 
  the logic programmer think functionally. The authors believe that logic   
  programming is a natural extension of functional programming, and they 
  demonstrate this by extending the Scheme with logical constructs — thereby 
  combining the benefits of both styles. The extension encapsulates most of 
  the ideas in Prolog.

* [SICP, sect 4.4](http://mitpress.mit.edu/sicp/full-text/book/book-Z-H-29.html#%_sec_4.4) - SICP's logic programming chapter.

* [PAIP, chapts 11-12]() - Peter Norvig's [Paradigms of Artificial
  Intelligence Programming](http://norvig.com/paip-preface.html) 
  presents the key ideas behind Prolog in chapters 11 and 12, and
  uses these ideas in subsequent chapters, particularly 20 and 21.
  (Prolog is a declarative logic programming language like Datalog
  with [different features and limitations](http://en.wikipedia.org/wiki/Datalog#Features.2C_limitations_and_extensions).)
  In chapter 11 Norvig walks through the construction of a Prolog 
  interpreter/compiler in Common Lisp. Source code available 
  [here](http://norvig.com/paip/README.html).


