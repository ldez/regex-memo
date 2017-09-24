## Méta-caractères

### Standard
|           |                                                                                  |
|-----------|----------------------------------------------------------------------------------|
| `.`       | Remplace n'importe quel caractère, sauf la fin de ligne.                         |
| `?`       | 0 ou une fois l'expression précédente.                                           |
| `*`       | Opérateur de Kleene : 0, 1 ou plusieurs fois l'expression précédente.            |
| `+`       | 1 ou plusieurs fois l'expression précédente.                                     |
| `[]`      | Classes de caractères                                                            |
| `{}`      | Quantificateur.                                                                  |
| `^`       | Négation.                                                                        |
| `|`       | Opérateur 'ou'.                                                                  |
| `-`       | Plage de caractères contigus.                                                    |
| `\`       | Le caractère qui suit n'est plus considéré comme un méta-caractère.              |
| `\Q … \E` | Le(s) caractère(s) qui suivent ne seront plus considéré comme un méta-caractère. |

### Spécificateurs de frontière

|      |                                                                               |
|------|-------------------------------------------------------------------------------|
| `^`  | Début de ligne. (en mode multiligne )                                         |
| `$`  | Fin de ligne. (en mode multiligne )                                           |
| `\b` | Extrémité de mot.                                                             |
| `\B` | Extrémité de non mot.                                                         |
| `\A` | Le début de la séquence à analyser.                                           |
| `\G` | L'analyse du motif qui suit \G suit exactement l'analyse précédente du motif. |
| `\z` | La fin de la séquence à analyser.                                             |
| `\Z` | La fin de la séquence à analyser, moins le caractère final.                   |
| `\<` | Le début d'un mot                                                             |
| `\>` | La fin d'un mot                                                               |

