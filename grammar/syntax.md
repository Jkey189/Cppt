# <mark style="background: #F8C7CC;">Пояснения:</mark>
- `...*`, `(...)*` - повторение (`n` раз, где `n` $\in N \cup 0$)
- `[...]` - необязательный элемент


# <mark style="background: #F5DD90;">Грамматика</mark>
`<программа>` $\rightarrow$
- `<декларация>*` |

`<декларация>` $\rightarrow$
- `<инструкция>` |
- `<функция>`

`<функция>` $\rightarrow$ `<func>` `<тип>` `<идентификатор>` `(` `[ <параметры> ]` `)` `<блок>`

`<параметры>` $\rightarrow$ `<параметр>` `( , <параметр> )*`

`<параметр>` $\rightarrow$ `<тип>` `<идендификатор>`


`<блок>` $\rightarrow$ `{` `<инструкция>` `( ; <инструкция> )*` `}`

`<инструкция>` $\rightarrow$
- `<блок>` |
- `<ввод>` |
- `<вывод>` |
- `<условная_инструкция>` |
- `<цикл>` |
- `<выбор>` |
- `<функция>` |
- `break` `;` |
- `continue` `;` |
- `<инициализация>` |
- `<присваивание>` |
- `return` `<выражение>` `;` |
- `<выражение>` `;` |
- `;`

`<ввод>` $\rightarrow$ `<cin>` `>>` `<идентификатор>` `( >> <идентификатор> )*` `;`

`<вывод>` $\rightarrow$ `<cout>` `<<` `<выражение>` `( << <выражение> )*` `;`

`<условная_инструкция>` $\rightarrow$ `if` `(` `<выражение>` `)` `<блок>` `[ else <блок> ]`

`<цикл>` $\rightarrow$
- `while` `(` `<выражение>` `)` `<блок>` |
- `for` `(` `<инициализация>` `;` `<выражение>` `;` `<шаг>` `)` `<блок>`

`<инициализация>` $\rightarrow$ `<тип>` `<идентификатор>` `[ = <идентификатор> | <целочисленный_литерал> | <вещественной_литерал> | <строковый_литерал> | <символьный_литерал> ]` `;`

`<присваивание>` $\rightarrow$ `<идентификатор>` `[ [ <индекс> ] ]*` `=` `<выражение>` `;`

`<шаг>` $\rightarrow$ `<выражение>`

`<выбор>` $\rightarrow$ `switch` `(` `<выражение>` `)` `{` `( case <литерал> : <блок> )*` `[default: <блок>]` `}`

`<литерал>` $\rightarrow$
- `<комментарий_литерал>` |
- `<целочисленный_литерал>` |
- `<вещественной_литерал>` |
- `<строковый_литерал>` |
- `<символьный_литерал>`

`<комментарий_литерал>` $\rightarrow$ `/*` `<ASCII_table>` `*/`

`<целочисленный_литерал>` $\rightarrow$ `[0-9]*`

`<вевщественный_литерал>` $\rightarrow$ `[0-9]*` `.` `[0-9]*`

`<строковый_литерал>` $\rightarrow$ `"` `[a-zA-Z0-9,./!@#$%^&*()_-+=]` `"`

`<символьныф_литерал>` $\rightarrow$ `'` `[a-zA-Z0-9,./!@#$%^&*()_-+=]` `'`

`<выражение>` $\rightarrow$ `<запятая>`

`<запятая>` $\rightarrow$ `<выражение_лог_или>` `( ( , ) <выражение_лог_или> )*`

`<выражение_лог_или>` $\rightarrow$ `<выражение_лог_и>` `( ( && ) <выражение_лог_и> )*`

`<выражение_лог_и>` $\rightarrow$ `<выражение_равн_неравн>` `( ( || ) <выражение_равн_неравн> )*`

`<выражение_равн_неравн>` $\rightarrow$ `<выражение_сравн>` `( ( == | != ) <выражение_сравн> )*`

`<выражение_сравн>` $\rightarrow$ `<выражение_плюс_минус>` `( ( > | < ) <выражение_плюс_минус> )*`

`<выражение_плюс_минус>` $\rightarrow$ `<выражение_умнож_дел>` `( ( + | - ) <выражение_умнож_дел> )*`

`<выражение_умнож_дел>` $\rightarrow$ `<унарное_выражение>` `( ( * | / ) <унарное_выражение> )*`

`<унарное_выражение>` $\rightarrow$ `[ ! | - ]` `<атомное_выражение>`

`<атомное_выражение>` $\rightarrow$
- `<литерал>` |
- `<идентификатор>` `[ [ <индекс> ] ]*` |
- `(` `<выражение>` `)`

`<индекс>` $\rightarrow$
- `<целочисленный_литерал>` |
- `<идентификатор>`

`<тип>` $\rightarrow$
- `int` |
- `float` |
- `char` |
- `bool` |
- `void` |
- `string` |
- `array` `<` `<тип>` `>`

`<идентификатор>` $\rightarrow$ `[a-zA-Z_]` `[a-zA-Z0-9_]*`

