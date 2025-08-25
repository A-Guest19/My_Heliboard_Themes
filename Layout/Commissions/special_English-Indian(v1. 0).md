# Special English (Indian) Layout

Samsung-esque Custom Layout for [thisisartman](https://github.com/thisisartman)

## Contents:
- Requirements & Other
- Main Layout (simple-style)
- Symbols (simple-style)
- Functional Keys (JSON-style)
- Number Row (JSON-style)
- Numpad (JSON-style)
- NTS

<blockquote><details>
  <summary>v1.0</summary>
                 
<blockquote><details>
  <summary>Requirements & Other</summary>
             
- Always show number row on
- Emoji key on
- Key hints on
</details></blockquote>

<blockquote><details>
<summary>Codes</summary>

### Main Layout
```
1 
2 
3 
4 
5 
6 
7 
8 
9 
0 

q
w
e
r
t
y
u
i
o
p

a
s
d
f
g
h
j
k
l

z
x
c
v
b
n
m
```
### Symbols
```
1
2
3
4
5
6
7
8
9
0

%
/
|
=
[
]
<
>
{
}

@
#
₹
_
&
-
+
(
)

*
"
'
:
;
!
?
```
### Functional Keys
```
[
  [
    { "label": "language_switch", "width": 1 },
    { "label": "copy", "width": 1 },
    { "label": "cut", "width": 1 },
    { "label": "paste", "width": 1 },
    { "label": "undo", "width": 1 },
    { "label": "redo", "width": 1 },
  ],
  [
    { "type": "placeholder" },
  ],
  [
    { "type": "placeholder" },
  ],
  [
    { "label": "shift", "width": 0.15 },
    { "type": "placeholder" },
    { "label": "delete", "width": 0.15 }
  ],
  [
    { "label": "symbol_alpha", "width": 0.15 },
    { "$": "variation_selector",
      "default":  { "label": "comma" },
      "email":    { "label": "@", "groupId": 1, "type": "function" },
      "uri":      { "label": "/", "groupId": 1, "type": "function" }
    },
    { "$": "keyboard_state_selector", "languageKeyEnabled": { "$": "keyboard_state_selector", "alphabet": { "label": "language_switch" }}},
    { "$": "keyboard_state_selector", "emojiKeyEnabled": { "$": "keyboard_state_selector", "alphabet": { "label": "emoji" }}},
    { "$": "keyboard_state_selector", "symbols": { "label": "numpad" }},
    { "label": "space" },
    { "label": "period", "labelFlags": 1073741824 },
    { "label": "action", "width": 0.15 }
  ]
]
```
### Number Row
```
[
    [
      { "type": "placeholder" },
    ],
    [
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "1" },
        "default": { "label": "1", "popup": { "relevant": [{ "label": "¹" }, { "label": "½" }, { "label": "⅓" }, { "label": "¼" }, { "label": "⅛" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "2" },
        "default": { "label": "2", "popup": { "relevant": [{ "label": "²" }, { "label": "⅔" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "3" },
        "default": { "label": "3", "popup": { "relevant": [{ "label": "³" }, { "label": "¾" }, { "label": "⅜" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "4" },
        "default": { "label": "4", "popup": { "relevant": [{ "label": "⁴" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "5" },
        "default": { "label": "5", "popup": { "relevant": [{ "label": "⁵" }, { "label": "⅝" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "6" },
        "default": { "label": "6", "popup": { "relevant": [{ "label": "⁶" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "7" },
        "default": { "label": "7", "popup": { "relevant": [{ "label": "⁷" }, { "label": "⅞" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "8" },
        "default": { "label": "8", "popup": { "relevant": [{ "label": "⁸" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "9" },
        "default": { "label": "9", "popup": { "relevant": [{ "label": "⁹" }] } }
      },
      { "$": "shift_state_selector",
        "manualOrLocked": { "label": "0" },
        "default": { "label": "0", "popup": { "relevant": [{ "label": "⁰" }, { "label": "ⁿ" }, { "label": "∅" }] } }
      }
    ],
    [
      { "label": "copy" }
    ],
  ]
```
### Numpad
```
[
  [
    { "label": "+", "type":  "function", "labelFlags": 512 },
    { "label": "1", "type": "numeric" },
    { "label": "2", "type": "numeric" },
    { "label": "3", "type": "numeric" },
    { "label": "%", "type":  "function", "labelFlags": 512 }
  ],
  [
    { "label": "(", "type":  "function", "labelFlags": 512 },
    { "label": "4", "type": "numeric" },
    { "label": "5", "type": "numeric" },
    { "label": "6", "type": "numeric" },
    { "label": "space", "type":  "function" }
  ],
  [
    { "label": ")", "type":  "function", "labelFlags": 512 },
    { "label": "7", "type": "numeric" },
    { "label": "8", "type": "numeric" },
    { "label": "9", "type": "numeric" },
    { "label": "delete" }
  ],
  [
    { "label": "alpha" },
    { "label": "comma", "width":  0.1 },
    { "label": "symbol", "width":  0.12 },
    { "label": "0", "type": "numeric" },
    { "label": "=", "type": "function", "width":  0.12, },
    { "label": "period", "width":  0.1 },
    { "label": "action" }
  ]
]
```
</details></blockquote>

</details></blockquote>

### NTS
NTS: special means extensive tweaking
