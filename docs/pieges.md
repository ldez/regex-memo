##  Pièges

### Groupe vs Ensemble

* `[A-Z]+` : corresponds à l'ensemble des caractères entre `A` et `Z` (toutes les lettres en majuscule) = `ABCFGD`, `ZERTGD`, `X`, `DJL`, ...
* `(A-Z)+` : corresponds à la répétition du groupe `A-Z` = `A-Z`, `A-ZA-ZA-Z`, `A-ZA-ZA-ZA-ZA-ZA-Z`, ...

### Négation vs Début de ligne

* `[^IB]` : corresponds à l'ensemble des caractères sauf `I` et `B` : `A`, `C`, `D`, `E`
* `^(IB)` : corresponds à la séquence de caractères `IB` en début de ligne : `IB`

### Point d'interrogation vs Répétition

* `[A?]` : corresponds aux caractères `A` et `?` : `A`, `?`
* `(A?)` : corresponds à un ensemble composé de 0 ou 1 fois à `A` : `A`, vide.

### Point vs Remplace

* `[A.]` : corresponds aux caractères `A` et `.` : `A`, `.`
* `(A.)` : corresponds à une séquence de 2 caractères commençant par `A` suivie de n'importe quel caractère : `AA`, `A:`, `AB`, ...

### Plus vs Répétition

* `[\d+]` : corresponds aux caractères décimal et à `+` : `1`, `+`, `9`, `6`, ...
* `(\d+)` : corresponds à une séquence composé uniquement de caractère décimal : `132456`, `98456`, `654138`, `2`, ...

### Tous vs Séquence

* `[.*]` : corresponds aux caractères `.` et `*` : `.`, `*`
* `(.*)` : corresponds à un ensemble de n'importe quel caractère.

### Backspace vs Extrémité

* `[\b]` : corresponds au caractère 'Backspace'.
* `\b` : corresponds à l'extrémité d'un mot.


