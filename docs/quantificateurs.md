
## Quantificateurs

| Quantifiers      |                                     |
|------------------|-------------------------------------|
| `0`              | une ou plusieurs occurrences.       |
| `*`              | zéro, une ou plusieurs occurrences. |
| `?`              | zéro ou une occurrence.             |
| `{n}`            | exactement n occurrences.           |
| `{n,}`           | au moins n occurrences.             |
| `{n,m}`          | de n à m (inclus) occurrences.      |
| `(?>pattern)`    | groupe atomique.                    |

Les quantificateurs précédents sont qualifiés de 3 façons différentes :

* **avides** : le matcheur lit toute la chaîne avant d'essayer la première concordance.
  Si l'appariement échoue, le matcheur recule d'un caractère, puis recommence... et ainsi de suite.
  La recherche du motif .*abc dans la chaîne `abcxxxxxxabcxxxxabc` trouve une occurrence de 0 à 19.

* **réticent** noté par `?` : la premère réussite est la bonne !
La recherche du motif `.*?abc` dans la chaîne `abcxxxxxxabcxxxxabc` trouve trois occurrences, une de 0 à 3, une de 3 à 12 et une 12 de à 19.

* **possessif_** noté par `+` : pareil que avide, mais si ça échoue, on ne recommence pas !
  La recherche du motif `.*+abc` dans la chaîne `abcxxxxxxabcxxxxabc` ne trouve pas de concordance : en effet, `.*+` mange tout jusqu'à la fin de la chaîne, et donc ce n'est pas suivi de `abc`

| Quantifiers |           |            | Meaning                                       |
|-------------|-----------|------------|-----------------------------------------------|
| Greedy      | Reluctant | Possessive |                                               |
| `X?`        | `X??`     | `X?+`      | `X`, once or not at all                       |
| `X*`        | `X*?`     | `X*+`      | `X`, zero or more times                       |
| `X+`        | `X+?`     | `X++`      | `X`, one or more times                        |
| `X{n}`      | `X{n}?`   | `X{n}+`    | `X`, exactly _n_ times                        |
| `X{n,}`     | `X{n,}?`  | `X{n,}+`   | `X`, at least _n_ times                       |
| `X{n,m}`    | `X{n,m}?` | `X{n,m}+`  | `X`, at least _n_ but not more than _m_ times |
