# #pain_point_knex_plv8

For instance if you learn knex you can run SQL queries eg on Postgresql.
plv8 plugin allows to run SQL from JS within database context as macro.
However it doesn't return promises.
Knex isn't universal, you great care have to be taken with eventualy future
breakage which is unmaintainable code.

Zig allows to write same code with and without promises. But you eventually
some libraries are missing yet and you don't want to switch for whatever reason

# #pain_point_java_is_no_typescript

    fetch('weather?city='+city) as Promise<{city:string, temperature: number

How would this look like in Java ? You have to compormise:
Either define classes (wasting compiler time, disk space, ..) or go untyped.
People on libera chat told me to be idiomatic.
I think the best solution is the easiest to read write and maintain which get's the job done.
So I want TypeScript typing within Java for such use cases!

# #flutter_reinventing_ai

Flutter was cerated to create new UI write once run everywhere. Now people
start reimplementing the world including AI libraries to have one language.

# #shell_is_not_a_programming_language
I tried topgit patch once, but felt lost cause so much 'the bashish' way.

# #react_ssr_faster_with_compiled_languages
Do you want to learn ocaml in order to get speed ?
And speed matters for sales customer retention etc
https://sancho.dev/blog/server-side-rendering-react-in-ocaml
