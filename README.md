# Modern ClojureScript

Modern ClojureScript (`modern-cljs`) is a series of tutorials that guide you in 
creating and running [ClojureScript][1] (CLJS) projects.

CLJS is a compiler for the Clojure programming language that targets
JavaScript. It emits JavaScript code which runs in web browsers or
other client-side or server-side JavaScript interpreters.

## Required background

These tutorials require that you have some prior programming experience. 
They assume you've gotten your hands dirty by trying a little Clojure,
even if you're not proficient in it yet. It will also be quite helpful if
you have some experience programming for the Web using HTML, JavaScript and the
browser DOM.

If you don't know anything about Clojure (or about Lisp), I
recommend you learn a little bit before starting these tutorials.

There are plenty of outstanding resources on Clojure that are freely available
on the Internet, and you can't overestimate the benefit of reading
a book on Clojure (or another Lisp dialect) to your value as a programmer,
a thinker, and a human being.

Here are some book recommendations:

* [Clojure Programming][29]: written by three of the heroes of Clojure,
  it contains everything you need to know about Clojure and its ecosystem.
* [Programming Clojure][30]: written by another legendary Clojure developer,
  it's the easiest path to learning Clojure.
* [The Joy of Clojure][31]: the title speaks by itself. A must read!
* [ClojureScript Up and Running][32]: at the moment, it's the only
  published book on ClojureScript. Even though it's not old, the
  book is a bit outdated since ClojureScript is evolving quickly. It's brief
  and useful, especially if you want to integrate with external
  JavaScript libraries.
* [SICP - Structure and Interpretation of Computer Programs][27]: this
  is the best programming book I've read in my very long career. It uses
  [Scheme/Racket][48] (a Lisp dialect) rather than Clojure and is available
  [online][43], in [print][43], or in a [lecture series](51).
* [On Lisp][28]: if you want to learn about macros, this is the place to start. 
  It uses [Common Lisp][49] (a Lisp dialect) rather than Clojure.
* [The Annotated Clojure Reference Manual][33]: by Rich Hickey, the creator
  of Clojure, it's an often overlooked Clojure book :).


## Required tools

Many people worry about which operating system and editor/IDE are best
for developing in Clojure and ClojureScript. I personally
use both Mac OS X and Ubuntu, and I use Emacs as an editor. 

Because I'm an old-timer, *nix and Emacs are the OS and editor I know best. 
That being said, in this series of tutorials you're not going to find any
suggestions or reference to operating systems or editors. Use whatever tools
you already have and know. I have too much respect for people developing
IDE/plugins for Clojure/CLJS to say that one is better than another, and
you don't want to combine learning a new programming language with trying
to learn a new programming environment.

You will need to have [git][45] installed and you'll need some familiarity
with the [basics of git][46].

Everything else you'll need besides git and a code editor is covered in the
tutorials!

## Why the name Modern ClojureScript?

You might wonder why this tutorial series is named `modern-cljs`
when ClojureScript is only a couple of years old. What 
in the world is ancient ClojureScript? You got me there! I started this series
while trying to port a few examples from the
[Modern JavaScript: Develop and Design][34] book to ClojureScript, and now it's
too late to change.

The name is becoming more appropriate each day as ClojureScript
continues to evolve quickly. I'd like to think it was a brilliant choice, but
it was just a happy accident. 

# The Tutorials

## Introduction

This series of tutorials guides you in creating and running simple CLJS
projects. The bulk of the series follows the progressive enhancement of
a single project.

While working through the tutorials I *strongly* suggest you start at
tutorial 1 and type in all the code for each tutorial yourself.
In my experience this is the the best approach if you're not already
very fluent with the programming language.

That being said, if you want to jump to the end and see what the final project
resulting from following the tutorials looks like, and assuming you
have already installed [leiningen 2][2], you can run the project from the last
tutorial by following these steps:

1. Get the tutorial repository by running
   `git clone https://github.com/magomimmo/modern-cljs.git`
2. `cd modern-cljs`
3. run `lein cljx once` # used from tutorial-16 forward
4. run `lein ring server-headless`
5. open a new terminal and cd in the modern-cljs main directory
6. run `lein cljsbuild once`
7. run `lein trampoline cljsbuild repl-listen`
8. open [login-dbg.html][3] and/or [shopping-dbg.html][4] in your browser
9. you can play with the repl you started in step 7 which is now connected
   to the browser

Don't be concerned if steps 3-9 don't make sense to you just yet,
they'll be covered in the tutorials.

> NOTE: If you want to skip ahead or back and access the code of any single
> tutorial without typing it or pasting it in, you can do as follows:
>
> * run `git clone https://github.com/magomimmo/modern-cljs.git`
> * `cd modern-cljs`
> * run `git checkout tutorial-n` # n is 01 for tutorial 1, 02 tutorial-02, etc.

## [Tutorial 1 - The Basics][5]

Create and configure a very basic CLJS project.

## [Tutorial 2 - Browser CLJS REPL (bREPL)][6]

Set up a browser connected CLJS REPL (bRepl) using an external http-server.

## [Tutorial 3 - Ring and Compojure][7]

Replace the external http-server with [Ring][8], a Clojure HTTP server and
middleware, and [Compojure][50], a routing library for Ring.

## [Tutorial 4 - Modern ClojureScript][9]

Have some fun with CLJS form validation by porting the JavaScript login form
example from [Modern Javascript: Development and design][10] to CLJS.

## [Tutorial 5 - Introducing Domina][12]

Use the [Domina library][13] to make our login form validation more Clojure-ish.

## [Tutorial 6 - The Easy Made Complex, and the Simple Made Easy][14]

Investigate and find two different ways to solve an issue from the last
tutorial.

##  [Tutorial 7 - Compilation Modes][15]

Explore CLJS/CLS compilation modes by using the `lein-cljsbuild` plugin of
`leiningen`, and discover a problem and solve it using a feature of the
`lein-cljsbuild` plugin.

## [Tutorial 8 - Introducing Domina Events][16]

Use Domina events for a more Clojure-ish approach to handing DOM events.

## [Tutorial 9 - DOM Manipulation][17]

Programmatically manipulate DOM elements in response to DOM events.

## [Tutorial 10 - Introducing AJAX][18]

Use AJAX to let the CLJS client-side code communicate with the server.

## [Tutorial 11 - A Deeper Understanding of Domina Events][19]

Apply Domina events to the login form example from the [4th Tutorial][9].

## [Tutorial 12 - HTML on Top, Clojure on the Bottom][20]

Explore the highest (HTML5) and deepest (Clojure on the server) layers of the
login form example from the [previous tutorial][20].

## [Tutorial 13 - Don't Repeat Yourself][21]

Respect the Don't Repeat Yourself (DRY) principle by sharing validators between
the client-side CLJS and the server-side Clojure.

## [Tutorial 14 - Better Safe Than Sorry (Part 1)][22]

Set the stage for unit testing by learning about the `Enlive`
template sytem and starting the shopping calculator example. Use code
refactoring to satisfy the DRY principle and to solve a cyclic namespaces
dependency problem.

## [Tutorial 15 - Better Safe Than Sorry (Part 2)][23]

Add validators to the `shoppingForm`, and do some unit testing.

## [Tutorial 16 - Better Safe Than Sorry (Part 3)][24]

Make our unit tests portable between Clojure and CLJS by using the
`clojurescript.test` lib and the `cljx` lein plugin.

## [Tuturial 17 - REPLing with Enlive][25]

Integrate the form validators from the server-side Shopping Calculator into
the Web UI, so the user is notified with the right error messages when 
typing invalid values into the form.

## [Tutorial 18 - Housekeeping!][26]

A digression to cover two topics on CLJS developer productivity, setting up
a more comfortable browser REPL based on nREPL, and a more
comfortable project structure using the `profiles` features of
[Leiningen][2].

## [Tutorial 19 - Livin' On the Edge][35]

Learn how to contribute something we need to someone
else's library, and how to publish a snapshot releases on
[clojars][36] to use the enhancement in our own project.

## [Tutorial 20 - Learning by Contributing (Part 1)][37]

Look at the [Enfocus][38] library with the
objective of sharing as much code as possible with 
[Enlive][39]. Start an open source collaboration by proposing a few
improvements to the Enfocus directory structure and the adoption of
the [clojurescript.test][40] library for implementing unit tests.

## [Tutorial 21 - Learning by Contributing (Part 2)][41]

Package [Enfocus](38) into a `jar`, instrument it
with the [Piggieback](52) library, publish it on [clojars](36), and use it
as a dependency in a very simple project to see that the changes we made don't
affect the Enfocus codebase, which still works as expected.

## [Tutorial 22 - Learning by Contributing (Part 3)][42]

Improve [Enfocus](38) by applying separation of concerns and
implementing a few unit tests. In the process, discover some 
bugs and correct them by first interacting with Enfocus in the REPL.

# License

Copyright © Mimmo Cosenza, 2012-2013. Released under the Eclipse Public
License, the same license as Clojure.

[1]: https://github.com/clojure/clojurescript.git
[2]: https://github.com/technomancy/leiningen
[3]: http://localhost:3000/login-dbg.html
[4]: http://localhost:3000/shopping-dbg.html
[5]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-01.md
[6]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-02.md
[7]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-03.md
[8]: https://github.com/ring-clojure/ring
[9]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-04.md
[10]: http://www.larryullman.com/books/modern-javascript-develop-and-design/
[11]: http://www.larryullman.com/
[12]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-05.md
[13]: https://github.com/levand/domina
[14]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-06.md
[15]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-07.md
[16]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-08.md
[17]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-09.md
[18]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-10.md
[19]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-11.md
[20]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-12.md
[21]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-13.md
[22]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-14.md
[23]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-15.md
[24]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-16.md
[25]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-17.md
[26]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-18.md
[27]: http://mitpress.mit.edu/sicp/
[28]: http://www.paulgraham.com/onlisp.html
[29]: http://www.clojurebook.com/
[30]: http://pragprog.com/book/shcloj2/programming-clojure
[31]: http://joyofclojure.com/
[32]: http://shop.oreilly.com/product/0636920025139.do
[33]: https://twitter.com/richhickey
[34]: http://www.larryullman.com/books/modern-javascript-develop-and-design/
[35]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-19.md
[36]: https://clojars.org/
[37]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-20.md
[38]: https://github.com/ckirkendall/enfocus
[39]: https://github.com/cgrand/enlive
[40]: https://github.com/cemerick/clojurescript.test
[41]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-21.md
[42]: https://github.com/magomimmo/modern-cljs/blob/master/doc/tutorial-22.md
[43]: http://mitpress.mit.edu/sicp/full-text/book/book.html
[44]: http://www.amazon.com/Structure-Interpretation-Computer-Programs-Engineering/dp/0262510871/
[45]: http://git-scm.com/
[46]: http://git-scm.com/documentation
[48]: http://racket-lang.org/
[49]: http://en.wikipedia.org/wiki/Common_Lisp
[50]: https://github.com/weavejester/compojure
[51]: http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-001-structure-and-interpretation-of-computer-programs-spring-2005/index.htm
[52]: https://github.com/cemerick/piggieback


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/magomimmo/modern-cljs/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

