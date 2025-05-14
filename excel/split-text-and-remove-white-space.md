# Split A Text String And Remove Whitespace

The contents of a cell can be split into multiple cells using the `TEXTSPLIT` formula in Excel.
You must identify the character upon which the text will be split.
Only one formula is needed even if the formula adds content to many new cells.

## Example

Given a cell with the content _CA - Contra Costa - Walnut Creek_, using `TEXTSPLIT` and splitting on the `-` character will produce separate cells with the contents of _CA_, _Contra Costa_, and _Walnut Creek_.
In the table below, only column `B` would need the formula.

|                 A                |  B  |        C       |        D       |
|:--------------------------------:|:---:|:--------------:|:--------------:|
| CA - Contra Costa - Walnut Creek | CA  |  Contra Costa  |  Walnut Creek  |
|                                  |     |                |                |

The formula in cell B would be: `=TEXTSPLIT(A1,"-")`

## Removing Whitespace

Some data may contain unwanted whitespace characters creating padding or inconsistent data.
To remove unnecessary whitespace, first use the `TRIM` formula.

```vb
=TRIM(TEXTSPLIT(A1,"-"))
```
