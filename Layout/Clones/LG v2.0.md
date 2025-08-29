# LG v2.0



LG style keyboard resembling the ~2016 v6.5.7 edition.


## Contents:
- What's New!
- Requirements & Other
- Main Layout (JSON-style)
- Symbols (Simple-style)
- More Symbols (Simple-style)
- Functional Keys (JSON-style)
- Numbers (JSON-style)
- Number Row (JSON-style)
- Phone (JSON-style)
- Phone symbols (JSON-style)
- NTS

<blockquote><details>
  <summary>Click Here for v2.0</summary>

<blockquote><details>
  <summary>What's New!</summary>

  - Updated main layout to JSON (in preparation for customized popups)
  - Added Functional Keys layout (JSON-style)
  - Added Numbers layout (JSON-style)
  - Added Phone layout (JSON-style)
  - Added Phone symbols layout (JSON-style)
  - Added period popups clone
  - Settings key now appears on alphabet and disappears on symbols & more symbols layouts
  - Emoji key now appears on symbols layout and disappears on alphabet layout
  - Number row keys are now the same color as functional keys
  - Period key now changes to TLDs
  - When entering a website name, "/" key appears
  - When entering email, "@" key appears
</details>

  
</blockquote>
                 
<blockquote><details>
  <summary>Requirements & Other</summary>
  
**Requirements:**
             
- Always show number row on
- Show TLD popup keys on
- Show emoji key off

**Recommended:**
- Change input method with space key on
- Long press symbols key for numpad

Goes With: [this LG Light Theme](https://github.com/A-Guest19/My_Heliboard_Themes/blob/main/Themes/Clones/LG%20Light%20v2.0.md#lg-light-theme-v20) & [this LG Dark Theme](https://github.com/A-Guest19/My_Heliboard_Themes/blob/main/Themes/Clones/LG%20Dark%20v2.0.md#lg-dark-theme-v20)

</details></blockquote>

<blockquote><details>
<summary>Codes</summary>

### Main Layout
```
[
    [
        { "label": "q", "popup": { "relevant": [ { "label": "+" } ] } },
        { "label": "w", "popup": { "relevant": [ { "label": "×" } ] } },
        { "label": "e", "popup": { "relevant": [  { "label": "÷" }, ] } },
        { "label": "r", "popup": { "relevant": [ { "label": "=" } ] } },
        { "label": "t", "popup": { "relevant": [ { "label": "%" } ] } },
        { "label": "y", "popup": { "relevant": [ { "label": "/" } ] } },
        { "label": "u", "popup": { "relevant": [ { "label": "\"" } ] } },
        { "label": "i", "popup": { "relevant": [ { "label": "*" } ] } },
        { "label": "o", "popup": { "relevant": [ { "label": "[" } ] } },
        { "label": "p", "popup": { "relevant": [ { "label": "]" } ] } }
    ],
    [
        { "label": "a", "popup": { "relevant": [ { "label": "@" } ] } },
        { "label": "s", "popup": { "relevant": [ { "label": "$" } ] } },
        { "label": "d", "popup": { "relevant": [ { "label": "!" } ] } },
        { "label": "f", "popup": { "relevant": [ { "label": "#" } ] } },
        { "label": "g", "popup": { "relevant": [ { "label": ":" } ] } },
        { "label": "h", "popup": { "relevant": [ { "label": ";" } ] } },
        { "label": "j", "popup": { "relevant": [ { "label": "&" } ] } },
        { "label": "k", "popup": { "relevant": [ { "label": "(" } ] } },
        { "label": "l", "popup": { "relevant": [ { "label": ")" } ] } }
    ],
    [
        { "label": "z", "popup": { "relevant": [ { "label": "-" } ] } },
        { "label": "x", "popup": { "relevant": [ { "label": "_" } ] } },
        { "label": "c", "popup": { "relevant": [ { "label": ' } ] } },
        { "label": "v", "popup": { "relevant": [ { "label": '' } ] } },
        { "label": "b", "popup": { "relevant": [ { "label": "," } ] } },
        { "label": "n", "popup": { "relevant": [ { "label": "." } ] } },
        { "label": "m", "popup": { "relevant": [ { "label": "?" } ] } }
    ]
]
```
### Symbols
```
+
×
÷
=
%
/
\
*
€
£

@
$
!
#
:
;
&
(
)

-
_
'
"
,
.
?
```
### More Symbols
```
￦
¥
°
¿
¡
^
[
]
<
>

~
`
§
μ
¬
Г
´
·
{
}

©
|
¤
Ω
θ
ฯ
```
### Functional Keys
```
[
  [
    { "label": "shift", "width": 0.13 },
    { "type": "placeholder" },
    { "label": "delete", "width": 0.13 }
  ],
  [
    { "label": "symbol_alpha", "type": "function", "width": 0.13 },
    
    { "$": "keyboard_state_selector", "languageKeyEnabled": 
        { "$": "keyboard_state_selector", "alphabet":
            { "label": "language_switch" }
        }
    },
    
    { "$": "keyboard_state_selector", "alphabet": { "$": "variation_selector", "email": { "label": "@", "type": "function" }, "uri": { "label": "/", "type": "function" } } },
         
    { "$": "keyboard_state_selector", "symbols": 
        { "label": "emoji" }
    },
    
    { "$": "keyboard_state_selector", "alphabet": 
        { "label": "settings", "type": "function", "popup":
            { "relevant": [ 
                { "label": "voice" },
                { "label": "clipboard" },
             ] },
       }
   },
    { "label": "space" },
    { "$": "variation_selector", "default": 
        { "label": ".", "type": "function", "labelFlags": 1073741824, "popup": { "relevant": [
        { "label": "!autoColumnOrder!8" }, { "label": "," }, { "label": "." }, { "label": "!" }, { "label": "?" }, { "label": '' }, { "label": ' }, { "label": "&" }, { "label": "@" }, { "label": "-" }, { "label": "+" }, { "label": ")" }, { "label": "(" }, { "label": ";" }, { "label": ":" }, { "label": "\\" }, { "label": "/" }, ] } }, 
        "email": { "label": ".com", "type": "function", "width": 0.13 }, 
        "uri": { "label": ".com", "type": "function", "width": 0.12, "popup": { "relevant": [ { "label": ".net"}, { "label": ".org"}, { "label" : ".com"}] } }, 
        },
    { "$": "variation_selector", "default": { "label": "action", "width": 0.13 }, }
  ]
]
```
### Numbers
```
[
  [
    { "label": "1", "type": "numeric" },
    { "label": "2", "type": "numeric" },
    { "label": "3", "type": "numeric" },
    { "label": "delete", "width": 0.26 }
  ],
  [
    { "label": "4", "type": "numeric" },
    { "label": "5", "type": "numeric" },
    { "label": "6", "type": "numeric" },
    { "label": " |!code/-1",  "type": "function", "width": 0.26 }
  ],
  [
    { "label": "7", "type": "numeric" },
    { "label": "8", "type": "numeric" },
    { "label": "9", "type": "numeric" },
    { "label": " |!code/-1", "type": "function", "width": 0.26 }
  ],
  [
    { "label": " |!code/-1", "type": "numeric" },
    { "label": "0", "type": "numeric" },
    { "label": ".", "type": "numeric" },
    { "label": "enter", "width": 0.26 }
  ]
]
```
### Number Row
```
[
  [
    { 
      "label": "1", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "¹" }, 
          { "label": "½" }, 
          { "label": "⅓" }, 
          { "label": "¼" }, 
          { "label": "⅛" }
        ] 
      } 
    },
    { 
      "label": "2", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "²" }, 
          { "label": "⅔" }
        ] 
      } 
    },
    { 
      "label": "3", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "³" }, 
          { "label": "¾" }, 
          { "label": "⅜" }
        ] 
      } 
    },
    { 
      "label": "4", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁴" }
        ] 
      } 
    },
    { 
      "label": "5", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁵" }, 
          { "label": "⅝" }
        ] 
      } 
    },
    { 
      "label": "6", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁶" }
        ] 
      } 
    },
    { 
      "label": "7", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁷" }, 
          { "label": "⅞" }
        ] 
      } 
    },
    { 
      "label": "8", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁸" }
        ] 
      } 
    },
    { 
      "label": "9", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁹" }
        ] 
      } 
    },
    { 
      "label": "0", 
      "type": "function", 
      "popup": { 
        "relevant": [
          { "label": "⁰" }, 
          { "label": "ⁿ" }, 
          { "label": "∅" }
        ] 
      } 
    }
  ]
]
```
### Numpad
```
N/A
```
### Numpad (landscape)
```
N/A
```
### Phone
```
[
  [
    { "label": "1", "type": "numeric" },
    { "label": "2", "type": "numeric", "popup": { "main": { "label": "ABC" } } },
    { "label": "3", "type": "numeric", "popup": { "main": { "label": "DEF" } } },
    { "label": "delete", "type": "function", "width": 0.26 }
  ],
  [
    { "label": "4", "type": "numeric", "popup": { "main": { "label": "GHI" } } },
    { "label": "5", "type": "numeric", "popup": { "main": { "label": "JKL" } } },
    { "label": "6", "type": "numeric", "popup": { "main": { "label": "MNO" } } },
    { "label": ".-(|!code/key_switch_alpha_symbol", "type": "function", "width": 0.26 }
  ],
  [
    { "label": "7", "type": "numeric", "popup": { "main": { "label": "PQRS" } } },
    { "label": "8", "type": "numeric", "popup": { "main": { "label": "TUV" } } },
    { "label": "9", "type": "numeric", "popup": { "main": { "label": "WXYZ" } } },
    { "label": "settings", "width": 0.26, "type": "function", "popup": { "relevant": [ { "label": "clipboard" } ] } }
  ],
  [
    { "label": " |!code/-1", "type": "numeric" },
    { "label": "0 +|0", "type": "numeric", "popup": { "relevant": [ { "label": "!noPanelAutoPopupKey!" }, { "label": "+" } ] } },
    { "label": "\\#",  "type": "numeric" },
    { "label": "action", "width": 0.26 }
  ]
]
```
### Phone symbols
```
[
  [
    { "label": "(", "type": "numeric" },
    { "label": "/", "type": "numeric" },
    { "label": ")", "type": "numeric" },
    { "label": "delete", "type": "function", "width": 0.26 }
  ],
  [
    { "label": "-", "type": "numeric" },
    { "label": ",", "type": "numeric" },
    { "label": ".", "type": "numeric" },
    { "label": "123|!code/key_switch_alpha_symbol", "type": "function", "width": 0.26 }
  ],
  [
    { "label": "N", "type": "numeric" },
    { "label": "P", "type": "numeric" },
    { "label": "W", "type": "numeric" },
    { "label": "delete", "width": 0.26 }
  ],
  [
    { "label": " |!code/-1", "type": "numeric", },
    { "label": "+", "type": "numeric" },
    { "label": "space", "type": "numeric" },
    { "label": "action", "width": 0.26 }
  ]
]
```
### Emoji bottom row
```
N/A
```
### Clipboard bottom row
```
N/A
```
</details></blockquote>

</details></blockquote>

### NTS
NTS: N/A
