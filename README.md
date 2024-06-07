# gradualc
An attempt to build a gradual compiler allowing you to gradually add competing
features which should play as well as possible with each other and with
external tools to avoid software rewrites

# High level goals (summary)

Be must useful, assist the programmer and get out of the way.

- allow advanced features and turning into specialist depending on target
  (JS/ Rust like / Python Like / Nix or Haskell like lazy / OO like to
  substitute Dart/Flutter / SQL Like for data querying)
  Example: plv8 can run SQL queries but doesn't return Promise !
  See #pain_point_knex_plv8
- minimizing overhead by having one tool
- minimizing dev cycles by being able to choose best fit for your case
  (interpreted vs compiled vs jitted vs partially interpreted vs interpreted)
  Think about it vscode vs Eclipse :-P
  vscode is good enough for many things, but compiled might be faster if you
  really have to work on much data
- allow embedding external abstract syntax trees (json/SQL/shell like)
  thus make it easy to run code in different context (SQL, backend, ..)
  Eg lookup useSSQ at rakkasjs to get an idea how to embed server side code within client code.
  In this case it happens to be the same language.
- acknowledge programming languages are tool to get a job done.
  Thus quick & Dirty / DSL for your case might make sense. In the end you as
  programmer are repsonsible for the result.
- #write_code_based_on_types.
  Fill in missing code eventually based on types
- compromise less compiled vs getting job done
  See #react_ssr_faster_with_compiled_languages

Why?
Try man zshall or bash and and learn how to use dictionaries or get a substring
and about exceptions of | while or whatever
Same for powenshell. Same for bat/bash abstraction languages. Same for ..

A language is made up of
    - core syntax
    - core libraries (date/IO/..)
    - packaging system
    - additional library
    - editor support (language server)
    - books to teach

Does it make sense to write a machine learning library using Dart just because
the frontend was written in Dart and you want same backend language ?

# DETAILS

See [FEATURES](./FEATURES.md)

See [being an alternative to](./BEING_ALTERNATIVE_TO.md) 
Think of it as potentially replacing if everything works out and the result is fast enough.

See [some important consequences](./SOME_IMPORTANT_CONSEQUENCES.md)

SEE [features and their contradictions](./FEATURES_CONTRADICTIONS.md)

# Some programming language and what they are missing out on
See [some programming languages and what they are missing out on](./SOME_PROGRAMMING_LANGUAGES_AND_WHAT_THEY_ARE_MISSING_OUT_ON.md)

[learnings from the past](./LEARNINGS_FROM_THE_PAST.md)

# IMPACT
This project might impact probably way beyond 20 million people:
https://www.linkedin.com/pulse/how-many-software-developers-world-codeninjainc
https://en.wikipedia.org/wiki/GitHub

# mixed language examples
vite using esbuild which is written in GO
All website using Webassembly
bun using Zig for speed adding JS runtime on top
...

# How to read these *.md files
Use search (github or clone and use editor) to follow them. It's fastest for typing.
Vim/Emacs/vscode/Github(requires login) all have search in all files features or grep

# expected issues
The goal is complex (sry) 

# Why this project exists
[pain-points-leading-to-this-project](./PAIN_POINT_LEADING_TO_THIS_PROJECT.md)
If the pain pointns go away, the reason for this project might vanish.
