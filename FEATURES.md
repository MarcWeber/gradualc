## #compile_time_macros
Generate code at compilation time

## #runtime_macros_code
Difference jitting? Or hinted jitting?
This code (...) should be run fast. Optimize before running at runtime.
It's like having a compiler at runtime

If you run code on large datasets (eg database) jitting might be helpful.

## #maybe_one_binary

## #lazyness
See Haskell why it's cool in some cases

## #async
Eg JS is famous example

## #strict

## #compiled

## #interpreted

## #jitted
    make interpreted parts faster

## #rust_like_ownership

## #reference_counted

## #garbage_collected

## #excellent_type_inference_like_haskell
Sry, having to copy paste types just eats up your time. CPU is fast. And might be faster tomorrow.
This all might be leading to something like dynamic bidirectional typing because the interpreter
requires this skill, too.
See #infer_select_fields

## #compiles_to_js
    because JS runtime starts with browser and has been highly optimzed its great for small interactivity

## #backend_code
strong enough to be usable as backend

## #frontend_code
strong enough to be usable as frontend (browser, embedded, app)

## #easy_backend_calling
See useSSQ (rakkasjs)
See #ast_first_class_citizen

## #typescript_like_subtyping
a = something
Typescript allows to say out of all possible values
(true/false/null/undefined/object/symbol,function/..)
This is a object of type Array with exactly 2 items with must be string and
number: [string, number]. This applies for stirng: 'apple' | 'pinapple' means
either stirng but notihng else.

This idea of subtyping can be applied to other langugaes like Java as well.
If you wait for the network using dynamic structures might be faster than classes.
Eg in Java there is no way to type this easily without having to create extra classes
which turns very verbose (and slows down compilation) once you nested structures
See #ast_first_class_citizen

    x = await fetch('http://weather-api.com/?city=X') as Promise<{city: string, temp: number}>

## #be_shell_and_usable_programming_language
Each shell command has its own syntax. None of the existing languages except
shells completions understand the application specific syntax of arguments.
If you want to merge shell and languages languages must be strong enough to shell code and be usable.

## #ast_first_class_citizen
See #run_code_in_different_context
See #be_shell_and_usable_programming_language

sql within server side code
server side code within client code. See #easy_backend_calling
Python within Nim

Long term this basically means that this gradualc system requires to understand
other languages or individual applications

JSON documents

## #incremental_compilation_linking_publishing
Zig has same goal
Publishing Example: copy binary to server or ESP32

## #target_small_code
Allow a compile setting to minimize code.

## #target_fast_compilation
Close to #target_small_code
Try to have fast dev cycles

## #hinting_for_jitting
I read once that JS has jitting but once you call a function with different type
you loose the benefits. So how about helping interpreter what should be run
fast in special cases you care about ?

## #deriving_code_from_types
Example:
    type X = {name: string}
    // automatically derive code to proof format is correct
    // add assertion or unsafe_ignore
    x = JSON.parse(fs.readFile("zoo"))

## #less_compromise_on_safety_vs_speed
requires: #proof_system

No compromise on safety vs speed (eg proof [0] exsists and drop the check
same for head and many more cases)

So the basic idea is either have assertions (#target_small_code) thus runtime
errors for head [], 1/0, overflows etc.

Or as alternative assume the caller does (has the assertion or a proof)

Example 1: eval result type
    # x is a string once evaled in browser turns into () => number
    fun = (x) => {
        y  = eval(x)
        return y()
    }
    print(fun("() => 2"))

Example 2: division by zero
    // b is not zero
    (a,b) => a/b

Example 3: index access
    // proof a contains index b
    (a,b) => a[b]

Example 4: zip
    a = ready_lazy_list_from_file(foo)
    b = [ 2,  3]
    c = [ 10, 40, 50]
    z = lazy_zip(a, b, c)
    print(z[1])

    The funny thing about zipping is if you can proof which is the smallest
    list you only have to check for tail of the smallest list.

    Now proofing all items are same length doesn't work in lazy context.
    Cause you might be getting out only 2 items in which case its enough to
    proof lists are long enough


## #proof_system
Big topic, no idea yet how to start this cause it also slows down

## #run_code_in_different_context
Run code in different context. Examples: Shell, SQL, #easy_backend_calling
code (traditional API),  run untrusted code in safer sandbox, ..

## #smart_code_templates
Eg fill in match { .. } arms (rust) or similar
template which also populates dependency file when adding a function (eg
package.json)

## #have_minimal_langage

## #allow_minimizing_coding_time
There are two ways competing strtategies:
Simple set of base lanugage.
Complex language which can be fitted towards a goal.
The latter saves time. And time is important.
So let user choose ..

## #one_way_of_doing_things
Well its not always easy to understand which is right.
But TS syntax for mapping types why not allow the same in code ?

    This is typelevel code in TypeScript meaning for each key of an object
    (hash) only keep values if they match a function type and value should be the key.
    { [K in keyof T]: T[K] extends ((...args: any[]) => Promise<any>) ? K : never }

    This is the same as (JS like pseudo code)
    {}.map_with_key((k,v) => typeof v == function ? k : skip)

## #eventually_allow_formalised_reasoning
Well this might turn complex due to many options.
Thus formalized reasoning to proof some safety guarantees might make sense but
might be a lot of work
