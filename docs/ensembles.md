## Ensembles

|              | Expressions     | Résultat                                             |
|--------------|-----------------|------------------------------------------------------|
| simple class | `[abc]`         | `a`, `b`, or `c`                                     |
| negation     | `[^abc]`        | Any character except `a`, `b`, or `c`                |
| range        | `[a-zA-Z]`      | `a` through `z`, or `A` through `Z`, inclusive       |
| union        | `[a-d[m-p]]`    | `a` through `d`, or `m` through `p`: `[a-dm-p]`      |
| intersection | `[a-z&&[def]]`  | `d`, `e`, or `f`                                     |
| subtraction  | `[a-z&&[^bc]]`  | `a` through `z`, except for `b` and `c`: `[ad-z]`    |
| subtraction  | `[a-z&&[^m-p]]` | `a` through `z`, and not `m` through `p`: `[a-lq-z]` |
