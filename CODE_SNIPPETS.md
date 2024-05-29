# #infer_select_fields
See #allow_minimizing_coding_time

This is a perfect example how compiling or interpreting the same code
challenges existing thinking. The idea is to not have to write the select fields
while optimizing a SQL query minimzing the fields to access at compile (or
interpreted) time.

The problem is without looking at x.last and x.name you don't know what fields
to query

    id = 2
    x = sql: FROM users WHERE id = $id
    print(x.name)
    print(x.last)

    when interpreted x is something like:
    expression once type of x is finalized and known
    can be constructed

    Then when send print(x.name) to interpreter expression turns into

    x = <expression once type of x is known>; print(x.name) -> x must contain key name

    Then using finalize(x) means it knows the type is final and could be evaluated ..

This example clearly shows that such interpreted code might run many times
slower than the compiled version and requires the typing system to be included
in the runtime.
