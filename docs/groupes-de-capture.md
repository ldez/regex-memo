
## Groupes de capture

|                |                                                               |
|----------------|---------------------------------------------------------------|
| `\i`           | `i` est entier représentant le numéro du groupe.              |
| `(?: pattern)` | groupe pur, ne pouvant être capturé.                          |
| `$i`           | désigne le `i` ème groupe reconnu (utilisable par le Matcher) |
| `$`&#96;       | Before matched string                                         |
| `$'`           | After matched string                                          |
| `$+`           | Last matched string                                           |
| `$&`           | Entire matched string                                         |

Le motif en entier, même sans parenthèses, est le groupe de rang 0.

`(a((bc)(d)))` définit 4 groupes :

| Groupe         | Numéro |
|----------------|--------|
| `(a((bc)(d)))` | 0      |
| `(a((bc)(d)))` | 1      |
| `((bc)(d))`    | 2      |
| `(bc)`         | 3      |
| `(d)`          | 4      |

L'expression `(\w\w)\1` permet de reconnaître des mots tels que `titi`, `toto`, `tutu`, `zozo` ...

Un groupe peut être utilisé avant son occurrence dans l'expression régulière :
`(\2deux|(un))+` permet de reconnaître des chaînes reconnues par l'expression un `(((un)+(deux){0,1})*)`.
Lors de l'analyse, au premier passage `\2` n'a pas de valeur, il y a donc échec, mais au deuxième passage, il peut avoir été affecté de "un", et l'analyse continue.
