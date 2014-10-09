Project
===

Problem definition
--

Your task is to write a program solving one of problems listed below:

1. *SAT solver* - more info [here](http://en.wikipedia.org/wiki/Boolean_satisfiability_problem)
2. Simple key-value store using B+ trees
3. Regular expression matcher/replacer
4. Unix utility: grep (no need for fancy regexp support)
5. LISP interpreter
6. Something like problems above. You may choose your own (but the lab-leader must agree on, indeed)

_“Sounds like problems for introductory programming courses, so what's the trick”_ you may think.

Let's make it more challenging:

- Program should take its input from a file and print output to another file, specified on the command line. Input and output files should be human-readable/writable. There are no other requirements on the format except that.
- Program must be written in a programming language implemented by yourself, i.e. you must first design and implement a programming language interpreter or compiler and a runtime for it and then implement a solution of one of the above problems in it. You may design your own language or you may implement a (subset of) existing one - it is up to you.
- Compiler itself is not graded, don't spend too much time with it and feel free to use existing bytecode compilers (javac etc.)
- You may work in teams, max team size is 2 people.
- You may use any language you want to implement your programming language runtime.

Submission
---

To submit your project, send an email to Marcel Hlopko with your project attached as a zip archive.

The subject of submission email must starts with `[MI-RUN][Project Submission]` (exactly like this, including brackets!!!) - this helps us to automatically process your emails. Otherwise, your email may (and will!!!) get lost in hundreds of other emails we receive.

The attached archive filename should be in form of `mi-run-<username>.zip` (`mi-run-<username1>-<username2>.zip` respectively) where `<username>` is CVUT user name of the author (authors separated by dash, respectively).

The .zip archive should contain ONE (root) directory named `mi-run-<username>`.

Structure of this directory is free-style, however it should contain:
- All the sources
- BASH script, makefile, rakefile or similar to compile your project WITHOUT running an IDE (WITHOUT RUNNING WINDOWS!!!). A Makefile for GNU Make, build.xml for Apache ant, pom.xml for Maven, Rakefile for Rake, CMake or similar is just fine (please, try to use something commonly used - it saves us a lot of time).
- Short README.txt describing:
  - How to compile it
  - Format of input and output files
  - Example code snippets demonstrating the features of your language
- Source code of the program solving the problem you chosen
- Some sample input files

Deadline
---

We do not set a deadline for submissions, feel free to submit your project in summer 2015. But you have so submit your project by 23:59 12.12.2014, if you want to be sure you will be graded in the winter 2014/2015. If you don't, we cannot guarantee you'll be able to go to exam before December 2015. Do not expect us to make you a personal examination term the very next day after submission just because you are in hurry for your masters defense. Usually we are able to arrange one examination per month. At most.

Hints
---

- Discuss. With your colleagues, teachers, do not hesitate to ask. Labs are not obligatory, but we advice you to follow. We encourage you to start working on the semestral work as soon as possible and take your work to labs and ask concrete questions. However, asking elementary questions and attempts to arrange consultations to solve elementary problems after the end of the semester will be frowned upon, if not completely ignored.
- Do not spend much time on parsing/compiling. Use some kind of compiler-compiler tool: yacc/bison, javacc, antlr, smaCC, petitparser… Or use existing bytecode (i.e. write a virtual machine which can interpret Java bytecode or other). Parsing is not part of grade.
- Think twice about the semantics of the language you're going to implement. When done, think again.
- Once implemented, check if the actual semantics is the same as the one you intended implemented. You may be surprised. Rather earlier than during exam.
- A good way is to start with parser and simple AST interpreter, then implement a compiler + BC interpreter, then GC. A good test suite would help, a lot.
- Use multiple languages, if it makes sense. A sensible choice might be to use Ruby/JavaScript to implement a parser and compiler and then C to implement actual execution runtime.

Exam
===

There will be no exam in common sense. Your final grade will be based on the outcome of your project after a short discussion, so you will have a chance to justify your design decisions.

The reason is that programming language design and implementation is like a writing a book or painting a picture. Even if you follow all the best practices how to write/paint, it is not guaranteed that the result will be an excellent book or painting. Therefore there is no set of requirements you have to fulfill. Don't be lazy, do your best. If unsure, don't hesitate to ask your lab leader. AST interpreter of procedural language won't be enough.

The exam will take place the week before Xmas, We need some time to go through your code, so submit before 12.12.2014. If you don't do so, we don't guarantee there will be another exam before December 2014. Seriously. Be sure to start soon, ask questions and be smart :)

FAQ
===

For those who still insist on a list of requirements to know what is the minimal set of feature required in order to pass an exam, then:

- _Do I have to implement GC?_ *Yes*
- _Do I have to implement bytecode interpreter?_ *Yes*
- _Do I have to implement bytecode compiler?_ *Yes*
- _Do I have to implement just-in-time compiler?_ *Yes*
- _Do I have to implement scheduler and threads?_ *Yes*
- _What optimization do I have to implement?_ *All known, dead code elimination, constant folding, abstract interpretation, trace-based compilation, custom compilation, inlining, everything!*
- _Do I have to implement XYZ?_ *Yes, of course!*

Do you feel better? :-)

