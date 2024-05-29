Don't get me wrong. All those tools have their advantages and reasons to exist
like Ruby everything being object being most simple.

## Rust
(Except linux only alloy): GC.
Faster dev cycle due to compilation

## JS
#no_typing

## TS
no $compile_time_macros (bun is an exception)
Slower than compiled languages even thought close or good
enough (example vscode).
But you would not use JS to write a database

## Java(Kotlin)
No type classes, not every case fits OO

## Python
Missing out on: #compiles_to_js
Complex binary packaging when adding GUI breaking your app
GIL unless you use non standard Python implementation which kinda means
rewriting Numpy and all the eco system (?)

## Ruby
Slow

## PHP
Missing out on: #compiles_to_js
Doesn't run fast in browser (possible using Webassembly though)

## Lua
Jitting not supported on all platforms

## Haxe
short lamdas a.map(_ + 1) or a.map_with_key([$1, $2]) like rejected
Ok this might be personal but typing takes time
The bigger issue with Haxe is that while it can target PHP/Java it doesn't have
consistent behavior. Its more like chose a backend and stick to it.
Yet Haxe is insipring and some cool stuff was written with it.
Being fair: PHP/Java might not be the most used backends.
