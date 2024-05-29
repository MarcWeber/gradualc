# gradualc
An attempt to build a gradual compiler allowing you to gradually add features
which should play well with other languages.

# High level goals

Getting rid of lock ins. If you have a project idea in mind you have to choose
and settle on a language like PHP. Once you outgrow it (need app). You either
have twice the work or need to switch language (major time effort).
MicroPython -> switch to CPP.
I am tired of learning new tools :-)

Try to the future in the sense of providing a dev system which can turn into a
specialist as needed while playing well with existing solutions allowing you to
reuse your existing knowledge.

Unite world of developers rather than splitting them over and over again.
Because a dev eco system is compiler, package manager, tooling, libraries, ...
So learning 3 languages requires 3 times the effort and debugging an reviewing
and distribution

See ./BEING_ALTERNATIVE_TO.md 
Think of it as potentially replacing if everything works out and the result is fast enough.

See ./SOME_IMPORTANT_CONSEQUENCES.md

# FEATURES
It's ok if goals are controversal thus cannot be added at the same time without compromise.
This actually means that within your code you get isles of code matching the
chosen features. Might still be better than using multiple languages

See ./FEATURES.md

# contradicting features
If you try to combine contradicting features like interpreted vs compiled you
run into many challenges.

SEE ./FEATURES_CONTRADICTIONS.md

# Some programming language and what they are missing out on
See ./SOME_PROGRAMMING_LANGUAGES_AND_WHAT_THEY_ARE_MISSING_OUT_ON.md

./LEARNINGS_FROM_THE_PAST.md

# How to read these *.md files
Use search (github or clone and use editor) to follow them. It's fastest for typing.
Vim/Emacs/vscode/Github(requires login) all have search in all files features or grep
