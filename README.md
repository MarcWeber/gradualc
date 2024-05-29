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
  So you can't use Knex easily without having to take much care
  So use_async should be a library configuration input.
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
- allow quick and dirty minimizing programmers time
- write code based on types.
  Fill in missing code eventually based on types

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


# How to read these *.md files
Use search (github or clone and use editor) to follow them. It's fastest for typing.
Vim/Emacs/vscode/Github(requires login) all have search in all files features or grep

# expected issues
The goal is complex (sry) 
