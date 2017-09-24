
## Classes de caractères

### Basique

|      |                   |                                                               |
|------|-------------------|---------------------------------------------------------------|
| `\d` | `[0-9]`           | Un chiffre `[\p{Nd}]`                                         |
| `\D` | `[^0-9]`          | un caractère qui n'est pas un chiffre                         |
| `\s` | `[ \t\n\r\f\x0B]` | Un caractère blanc (espace, tab, new line...)                 |
| `\S` | `[^\s]`           | Un caractère non blanc                                        |
| `\w` | `[a-zA-Z_0-9]`    | Un caractère de mot. `[\p{Ll}\p{Lu}\p{Lt}\p{Lo}\p{Nd}\p{Pc}]` |
| `\W` | `[^\w]`           | Un caractère qui n'est pas un caractère de mot                |
| `\O` |                   | Un chiffre octal                                              |
| `\c` |                   | Caractère de contrôle                                         |


### POSIX

|              |                                                  |
|--------------|--------------------------------------------------|
| `\p{Alnum}`  | Alphanumeric characters                          |
| `\p{Alpha}`  | Alphabetic characters                            |
| `\p{ASCII}`  | ASCII characters                                 |
| `\p{Blank}`  | Space and tab characters                         |
| `\p{Cntrl}`  | Control characters                               |
| `\p{Digit}`  | Numeric characters                               |
| `\p{Graph}`  | printable and visible (without spaces)           |
| `\p{Lower}`  | Lower-case alphabetic                            |
| `\p{Print}`  | Printable characters (with spaces)               |
| `\p{Punct}`  | Punctuation characters                           |
| `\p{Space}`  | All whitespace characters, including line breaks |
| `\p{Upper}`  | Upper-case alphabetic                            |
| `\p{XDigit}` | Hexadecimal digits                               |

### Unicode

|          |             |                                                                  |
|----------|-------------|------------------------------------------------------------------|
| `\p{Cc}` | control     | an ASCII `0x00..0x1F` or Latin-1` 0x80..0x9F` control character. |
| `\p{Cf}` | format      | invisible formatting indicator.                                  |
| `\p{Cn}` | unassigned  | any code point to which no character has been assigned.          |
| `\p{Co}` | private use | any code point reserved for private use.                         |
| `\p{Cs}` | surrogate   | one half of a surrogate pair in UTF-16 encoding.                 |
| `\p{C}`  | control     | format                                                           |

|          |                  |                                                                                                     |
|----------|------------------|-----------------------------------------------------------------------------------------------------|
| `\p{L1}` | latin-1          |                                                                                                     |
| `\p{LC}` | uppercase letter | lowercase letter                                                                                    |
| `\p{LD}` | uppercase letter | lowercase letter                                                                                    |
| `\p{Ll}` | lowercase letter | a lowercase letter that has an uppercase variant.                                                   |
| `\p{Lm}` | modifier letter  | a special character that is used like a letter.                                                     |
| `\p{Lo}` | other letter     | a letter or ideograph that does not have lowercase and uppercase variants.                          |
| `\p{Lt}` | titlecase letter | a letter that appears at the start of a word when only the first letter of the word is capitalized. |
| `\p{Lu}` | uppercase letter | an uppercase letter that has a lowercase variant.                                                   |
| `\p{L}`  | uppercase letter | lowercase letter                                                                                    |

|          |                        |                                                                                                                               |
|----------|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `\p{Mc}` | combining spacing mark | a character intended to be combined with another character that takes up extra space (vowel signs in many Eastern languages). |
| `\p{Me}` | enclosing mark         | a character that encloses the character is is combined with (circle, square, keycap, etc.).                                   |
| `\p{Mn}` | non spacing mark       | a character intended to be combined with another character without taking up extra space (e.g. accents, umlauts, etc.).       |
| `\p{M}`  | non spacing mark       | enclosing mark                                                                                                                |

|          |                      |                                                                                                                        |
|----------|----------------------|------------------------------------------------------------------------------------------------------------------------|
| `\p{Nd}` | decimal digit number | a digit zero through nine in any script except ideographic scripts.                                                    |
| `\p{Nl}` | letter number        | a number that looks like a letter, such as a Roman numeral.                                                            |
| `\p{No}` | other number         | a superscript or subscript digit, or a number that is not a digit `0..9` (excluding numbers from ideographic scripts). |
| `\p{N}`  | decimal digit number | letter number                                                                                                          |

|          |                           |                                                                                    |
|----------|---------------------------|------------------------------------------------------------------------------------|
| `\p{Pc}` | connector punctuation     | a punctuation character such as an underscore that connects words.                 |
| `\p{Pd}` | dash punctuation          | any kind of hyphen or dash.                                                        |
| `\p{Pe}` | end punctuation           | any kind of closing bracket.                                                       |
| `\p{Pf}` | final quote punctuation   | any kind of closing quote.                                                         |
| `\p{Pi}` | initial quote punctuation | any kind of opening quote.                                                         |
| `\p{Po}` | other punctuation         | any kind of punctuation character that is not a dash, bracket, quote or connector. |
| `\p{Ps}` | start punctuation         | any kind of opening bracket.                                                       |
| `\p{P}`  | dash punctuation          | start punctuation                                                                  |

|          |                 |                                                                                     |
|----------|-----------------|-------------------------------------------------------------------------------------|
| `\p{Sc}` | currency symbol | any currency sign.                                                                  |
| `\p{Sk}` | modifier symbol | a combining character (mark) as a full character on its own.                        |
| `\p{Sm}` | math symbol     | any mathematical symbol.                                                            |
| `\p{So}` | other symbol    | various symbols that are not math symbols, currency signs, or combining characters. |
| `\p{S}`  | math symbol     | currency symbol                                                                     |

### Unicode Block

|                                              |                                         |
|----------------------------------------------|-----------------------------------------|
| `\p{InAegeanNumbers}`                        | Aegean Numbers                          |
| `\p{InAlphabeticPresentationForms}`          | Alphabetic Presentation Forms           |
| `\p{InArabic}`                               | Arabic                                  |
| `\p{InArabicPresentationForms-A}`            | Arabic Presentation Forms-A             |
| `\p{InArabicPresentationForms-B}`            | Arabic Presentation Forms-B             |
| `\p{InArmenian}`                             | Armenian                                |
| `\p{InArrows}`                               | Arrows                                  |
| `\p{InBasicLatin}`                           | Basic Latin                             |
| `\p{InBengali}`                              | Bengali                                 |
| `\p{InBlockElements}`                        | Block Elements                          |
| `\p{InBopomofo}`                             | Bopomofo                                |
| `\p{InBopomofoExtended}`                     | Bopomofo Extended                       |
| `\p{InBoxDrawing}`                           | Box Drawing                             |
| `\p{InBraillePatterns}`                      | Braille Patterns                        |
| `\p{InBuhid}`                                | Buhid                                   |
| `\p{InByzantineMusicalSymbols}`              | Byzantine Musical Symbols               |
| `\p{InCherokee}`                             | Cherokee                                |
| `\p{InCJKCompatibilityForms}`                | CJK Compatibility Forms                 |
| `\p{InCJKCompatibilityIdeographs}`           | CJK Compatibility                       |
| `\p{InCJKCompatibilityIdeographs}`           | CJK Compatibility Ideographs            |
| `\p{InCJKCompatibilityIdeographsSupplement}` | CJK Compatibility Ideographs Supplement |
| `\p{InCJKRadicalsSupplement}`                | CJK Radicals Supplement                 |
| `\p{InCJKSymbolsandPunctuation}`             | CJK Symbols and Punctuation             |
| `\p{InCJKUnifiedIdeographs}`                 | CJK Unified Ideographs                  |
| `\p{InCJKUnifiedIdeographsExtensionA}`       | CJK Unified Ideographs Extension A      |
| `\p{InCJKUnifiedIdeographsExtensionB}`       | CJK Unified Ideographs Extension B      |
| `\p{InCombiningDiacriticalMarks}`            | Combining Diacritical Marks             |
| `\p{InCombiningHalfMarks}`                   | Combining Half Marks                    |
| `\p{InCombiningMarksforSymbols}`             | Combining Diacritical Marks for Symbols |
| `\p{InControlPictures}`                      | Control Pictures                        |
| `\p{InCurrencySymbols}`                      | Currency Symbols                        |
| `\p{InCypriotSyllabary}`                     | Cypriot Syllabary                       |
| `\p{InCyrillic}`                             | Cyrillic                                |
| `\p{InCyrillicSupplementary}`                | Cyrillic Supplementary                  |
| `\p{InDeseret}`                              | Deseret                                 |
| `\p{InDevanagari}`                           | Devanagari                              |
| `\p{InDingbats}`                             | Dingbats                                |
| `\p{InEnclosedAlphanumerics}`                | Enclosed Alphanumerics                  |
| `\p{InEnclosedCJKLettersandMonths}`          | Enclosed CJK Letters and Months         |
| `\p{InEthiopic}`                             | Ethiopic                                |
| `\p{InGeneralPunctuation}`                   | General Punctuation                     |
| `\p{InGeometricShapes}`                      | Geometric Shapes                        |
| `\p{InGeorgian}`                             | Georgian                                |
| `\p{InGothic}`                               | Gothic                                  |
| `\p{InGreek}`                                | Greek                                   |
| `\p{InGreekandCoptic}`                       | Greek and Coptic                        |
| `\p{InGreekExtended}`                        | Greek Extended                          |
| `\p{InGujarati}`                             | Gujarati                                |
| `\p{InGurmukhi}`                             | Gurmukhi                                |
| `\p{InHalfwidthandFullwidthForms}`           | Halfwidth and Fullwidth Forms           |
| `\p{InHangulCompatibilityJamo}`              | Hangul Compatibility Jamo               |
| `\p{InHangulJamo}`                           | Hangul Jamo                             |
| `\p{InHangulSyllables}`                      | Hangul Syllables                        |
| `\p{InHanunoo}`                              | Hanunoo                                 |
| `\p{InHebrew}`                               | Hebrew                                  |
| `\p{InHighPrivateUseSurrogates}`             | High Private Use Surrogates             |
| `\p{InHighSurrogates}`                       | High Surrogates                         |
| `\p{InHiragana}`                             | Hiragana                                |
| `\p{InIdeographicDescriptionCharacters}`     | Ideographic Description Characters      |
| `\p{InIPAExtensions}`                        | IPA Extensions                          |
| `\p{InKanbun}`                               | Kanbun                                  |
| `\p{InKangxiRadicals}`                       | Kangxi Radicals                         |
| `\p{InKannada}`                              | Kannada                                 |
| `\p{InKatakana}`                             | Katakana                                |
| `\p{InKatakanaPhoneticExtensions}`           | Katakana Phonetic Extensions            |
| `\p{InKhmer}`                                | Khmer                                   |
| `\p{InKhmerSymbols}`                         | Khmer Symbols                           |
| `\p{InLao}`                                  | Lao                                     |
| `\p{InLatin-1Supplement}`                    | Latin-1 Supplement                      |
| `\p{InLatinExtended-A}`                      | Latin Extended-A                        |
| `\p{InLatinExtended-B}`                      | Latin Extended-B                        |
| `\p{InLatinExtendedAdditional}`              | Latin Extended Additional               |
| `\p{InLetterlikeSymbols}`                    | Letterlike Symbols                      |
| `\p{InLimbu}`                                | Limbu                                   |
| `\p{InLinearBIdeograms}`                     | Linear B Ideograms                      |
| `\p{InLinearBSyllabary}`                     | Linear B Syllabary                      |
| `\p{InLowSurrogates}`                        | Low Surrogates                          |
| `\p{InMalayalam}`                            | Malayalam                               |
| `\p{InMathematicalAlphanumericSymbols}`      | Mathematical Alphanumeric Symbols       |
| `\p{InMathematicalOperators}`                | Mathematical Operators                  |
| `\p{InMiscellaneousMathematicalSymbols-A}`   | Miscellaneous Mathematical Symbols-A    |
| `\p{InMiscellaneousMathematicalSymbols-B}`   | Miscellaneous Mathematical Symbols-B    |
| `\p{InMiscellaneousSymbols}`                 | Miscellaneous Symbols                   |
| `\p{InMiscellaneousSymbolsandArrows}`        | Miscellaneous Symbols and Arrows        |
| `\p{InMiscellaneousTechnical}`               | Miscellaneous Technical                 |
| `\p{InMongolian}`                            | Mongolian                               |
| `\p{InMusicalSymbols}`                       | Musical Symbols                         |
| `\p{InMyanmar}`                              | Myanmar                                 |
| `\p{InNumberForms}`                          | Number Forms                            |
| `\p{InOgham}`                                | Ogham                                   |
| `\p{InOldItalic}`                            | Old Italic                              |
| `\p{InOpticalCharacterRecognition}`          | Optical Character Recognition           |
| `\p{InOriya}`                                | Oriya                                   |
| `\p{InOsmanya}`                              | Osmanya                                 |
| `\p{InPhoneticExtensions}`                   | Phonetic Extensions                     |
| `\p{InRunic}`                                | Runic                                   |
| `\p{InShavian}`                              | Shavian                                 |
| `\p{InSinhala}`                              | Sinhala                                 |
| `\p{InSmallFormVariants}`                    | Small Form Variants                     |
| `\p{InSpacingModifierLetters}`               | Spacing Modifier Letters                |
| `\p{InSpecials}`                             | Specials                                |
| `\p{InSuperscriptsandSubscripts}`            | Superscripts and Subscripts             |
| `\p{InSupplementalArrows-A}`                 | Supplemental Arrows-A                   |
| `\p{InSupplementalArrows-B}`                 | Supplemental Arrows-B                   |
| `\p{InSupplementalMathematicalOperators}`    | Supplemental Mathematical Operators     |
| `\p{InSupplementaryPrivateUseArea-A}`        | Supplementary Private Use Area-A        |
| `\p{InSupplementaryPrivateUseArea-B}`        | Supplementary Private Use Area-B        |
| `\p{InSyriac}`                               | Syriac                                  |
| `\p{InTagalog}`                              | Tagalog                                 |
| `\p{InTagbanwa}`                             | Tagbanwa                                |
| `\p{InTags}`                                 | Tags                                    |
| `\p{InTaiLe}`                                | Tai Le                                  |
| `\p{InTaiXuanJingSymbols}`                   | Tai Xuan Jing Symbols                   |
| `\p{InTamil}`                                | Tamil                                   |
| `\p{InTelugu}`                               | Telugu                                  |
| `\p{InThaana}`                               | Thaana                                  |
| `\p{InThai}`                                 | Thai                                    |
| `\p{InTibetan}`                              | Tibetan                                 |
| `\p{InUgaritic}`                             | Ugaritic                                |
| `\p{InUnifiedCanadianAboriginalSyllabics}`   | Unified Canadian Aboriginal Syllabics   |
| `\p{InVariationSelectors}`                   | Variation Selectors                     |
| `\p{InVariationSelectorsSupplement}`         | Variation Selectors Supplement          |
| `\p{InYijingHexagramSymbols}`                | Yijing Hexagram Symbols                 |
| `\p{InYiRadicals}`                           | Yi Radicals                             |
| `\p{InYiSyllables}`                          | Yi Syllables                            |

### Java spécifiques

|                                  |                                          |
|----------------------------------|------------------------------------------|
| `\p{javaDefined}`                | `Character.isDefined(ch)`                |
| `\p{javaDigit}`                  | `Character.isDigit(ch)`                  |
| `\p{javaIdentifierIgnorable}`    | `Character.isIdentifierIgnorable(ch)`    |
| `\p{javaISOControl}`             | `Character.isISOControl(ch)`             |
| `\p{javaJavaIdentifierPart}`     | `Character.isJavaIdentifierPart(ch)`     |
| `\p{javaJavaIdentifierStart}`    | `Character.isJavaIdentifierStart(ch)`    |
| `\p{javaLetterOrDigit}`          | `Character.isLetterOrDigit(ch)`          |
| `\p{javaLetter}`                 | `Character.isLetter(ch)`                 |
| `\p{javaLowerCase}`              | `Character.isLowerCase(ch)`              |
| `\p{javaMirrored}`               | `Character.isMirrored(ch)`               |
| `\p{javaSpaceChar}`              | `Character.isSpaceChar(ch)`              |
| `\p{javaTitleCase}`              | `Character.isTitleCase(ch)`              |
| `\p{javaUnicodeIdentifierPart}`  | `Character.isUnicodeIdentifierPart(ch)`  |
| `\p{javaUnicodeIdentifierStart}` | `Character.isUnicodeIdentifierStart(ch)` |
| `\p{javaUpperCase}`              | `Character.isUpperCase(ch)`              |
| `\p{javaWhitespace}`             | `Character.isWhitespace(ch)`             |

