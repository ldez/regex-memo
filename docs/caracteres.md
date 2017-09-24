## Caractères

|       |                                                   |
|-------|---------------------------------------------------|
| `\\`  | Le caractère anti-slash                           |
| `\\a` | Le caractère sonnette `\u0007`                    |
| `\\b` | Backspace `\u0008`                                |
| `\\e` | Le caractère d'échappement `\u001B`               |
| `\f`  | Formfeed `\u000C`                                 |
| `\n`  | Le caractère de nouvelle ligne `\u000A`           |
| `\r`  | Le caractère de retour en début de ligne `\u000D` |
| `\t`  | Le caractère de tabulation `\u0009`               |
| `\\v` | Vertical tabulation `\u000B`                      |

|          |                                                                  |
|----------|------------------------------------------------------------------|
| `\\cx`   | Le caractère de contrôle ASCII correspondant à `x`               |
| `\0`     | `null`                                                           |
| `\0n`    | Le caractère de code ASCII octal _n_ avec (0≤`n`≤7)              |
| `\0nn`   | Le caractère de code ASCII octal _nn_ avec (0≤`n`≤)              |
| `\0mnn`  | Le caractère de code ASCII octal _mnn_ avec (0≤`m`≤3 et 0≤`n`≤7) |
| `\0hh`   | Le caractère de code ASCII hexadecimal `0xhh`                    |
| `\0hhhh` | Le caractère de code ASCII hexadecimal `0xhhhh`                  |
| `\\xnn`  | Le caractère de code ASCII hexa `xxxx`                           |
| `\uxxxx` | Le caractère de code Unicode hexa `xxxx`                         |
