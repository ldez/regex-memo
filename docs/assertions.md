
## Assertion (Look-ahead – Look-behind)

|         |                                                  |
|---------|--------------------------------------------------|
| `(?=)`  | Assertion avant positive (positive lookahead)    |
| `(?!)`  | Assertion avant négative (negative lookahead)    |
| `(?<=)` | Assertion arrière positive (positive lookbehind) |
| `(?<!)` | Assertion arrière négative (negative lookbehind) |


### Assertion avant positive (positive lookahead)

|                      |                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------|
| `element(?=pattern)` | Permet de vérifier si un élément est suivi d'un pattern spécifique avant de capturer cet élément.  |
| `(?=pattern)element` | Permet de vérifier si un élément commence par un pattern spécifique avant de capturer cet élément. |

Exemples :

* Expression : `(?=ma)\b\w{5,}\b`
  * Cible : `maison mais maisonnette carotte concombre ta`
  * Résultat : 2 match.
  * Trouve `maison` et `maisonnette`, soit un mot de 5 caractères 'mot' ou plus commençant par `ma`.

* Expression : `(?=255)(\d{1,3}\.){3}\d{1,3}`
  * Trouve les ip commençant par 255.

* Expression :` \b\w+\b(?=, mais)`
  * Cible : `Bah oui, mais bon alors voilà! oui, ok mais et alors?`
  * Résultat : 1 match.
  * Trouve `oui`, le pattern entre parenthèses qui le suit n'est pas capturé.

### Assertion avant négative (negative lookahead)

|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| `element(?!pattern)` | Permet de vérifier si un élément n'est pas suivi d'un pattern spécifique avant de capturer cet élément.   |
| `(?!pattern)element` | Permet de vérifier si un élément ne commence pas par un pattern spécifique avant de capturer cet élément. |

Exemples :

* Expression : `(?!ma)\b\w{3,}\b`
  * Cible : `maison mais maisonnette carotte concombre ta`
  * Résultat : 2 matches.
  * Trouve `carotte` et `concombre`, soit un mot de 3 caractères 'mot' ou plus ne commençant pas par `ma`.

* Expression : `(?!255)(\d{1,3}\.){3}\d{1,3}`
  * Trouve les ip ne commençant pas par 255.

* Expression : `\b\w{3}\b(?!, mais)`
  * Cible : `Bah oui, mais bon alors voilà! oui, ok mais et alors?`
  * Résultat : 3 matches.
  * Trouve `bah`, `bon` et `oui`, mais le premier '`oui` n'a pas été capturé car il est suivi du pattern.

### Assertion arrière positive (positive lookbehind)

|                       |                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------|
| `(?<=pattern)element` | Permet de vérifier si un élément est précédé d'un pattern spécifique avant de capturer cet élément.  |
| `element(?<=pattern)` | Permet de vérifier si un élément se termine par un pattern spécifique avant de capturer cet élément. |

Exemples :

* Expression : `\b\w{4,}\b(?<=n)`
  * Cible : `maison mais maisonnette carotte concombre ta`
  * Trouve `maison`, soit un mot de 4 caractères 'mot' ou plus se terminant par `n`.

* Expression : `(?<=oui, )\b\w{4}\b`
  * Cible : `Bah oui, mais bon alors voilà! oui, ok mais et alors?`
  * Résultat : 1 match.
  * Trouve `mais`, car c'est le seul mot de 4 lettres précédé de `oui, `.

### Assertion arrière négative (negative lookbehind)

|                       |                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `(?<!pattern)element` | Permet de vérifier si un élément n'est pas précédé d'un pattern spécifique avant de capturer cet élément. |
| `element(?<!pattern)` | Permet de vérifier si un élément se termine pas par un pattern spécifique avant de capturer cet élément.  |

Exemples :

* Expression : `\b\w{4,}\b(?<!n)`
  * Cible : `maison mais maisonnette carotte concombre ta`
  * Trouve `mais`, `maisonnette`, `carotte` et `concombre`, soit un mot de 4 caractères 'mot' ou plus se terminant pas par `n`.

* Expression : `(?<!oui, )\b\w{2}\b`
  * Cible : `Bah oui, mais bon alors voilà! oui, ok mais et alors?`
  * Résultat : 1 match.
  * Trouve `et`, car c'est le seul mot de 2 lettres qui n'est pas précédé de `oui, `.

