# My personalized Kyria's Keymap

## Resources

- [How to flash firmware with qmk](https://docs.splitkb.com/hc/en-us/articles/6330981035676-Aurora-Build-Guide-20-Flashing-Firmware)
- [Online keymap builder](https://config.qmk.fm/#/frooastboard/walnut/LAYOUT_all)

## How to

- Compile this software: `qmk compile -kb splitkb/kyria/ -km my_keymap_name`
- Flash compiled software: `qmk flash -bl dfu path/to_my/firmware_file.hex`

## Description

The default keymap contains 5 layers which allows it to include all keys found on an ANSI layout TKL keyboard plus media keys.
Hardware features of the Kyria such as OLEDs, rotary encoders and underglow are also supported.

The five different layers are the following:

1. Base layer (QWERTY, Colemak-DH or Dvorak)
2. Navigation layer
3. Symbols/Numbers layer
4. Function layer
5. Adjust layer

![Step-by-step animation of the transformation of an ortholinear TKL to a Kyria](https://i.imgur.com/uVDCOek.gif)

<details>
After making transformations to the classic ANSI US QWERTY TKL 60% to arrive to the layout of the Kyria, as illustrated in the animation above, the result looks like this:

## Base layer(s)

```
Base Layer: -

,-------------------------------------------.                              ,-------------------------------------------.
|  Tab   |   -  |   -  |   -  |   -  |   -  |                              |   -  |   -  |   -  |   -  |   -  |  Bksp  |
|--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
|Ctrl/Esc|   -  |   -  |   -  |   -  |   -  |                              |   -  |   -  |   -  |   -  |   -  |Ctrl/ - |
|--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
| LShift |   -  |   -  |   -  |   -  |   -  | [ {  |CapsLk|  |F-Keys|  ] } |   -  |   -  |   -  |   -  |   -  | RShift |
`----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                       |Adjust| LGUI | LAlt | Space| Nav  |  | Sym  | Enter| AltGr| RGUI | Menu |
                       `----------------------------------'  `----------------------------------'
```

Three different well-known keyboard layouts are provided to fill in the placeholder `-` keys: QWERTY, Colemak-DH, and Dvorak. The default layer can be changed at runtime, more info on that in the section on the [adjust layer](#adjust-layer).

For the rest of this write-up, the base layer will be assumed to be Dvorak and will be used as a reference to describe physical keys, e.g. “<kbd>B</kbd> key” vs, the much more verbose, “lower inner index key”.

```
Base Layer: Dvorak

,-------------------------------------------.                              ,-------------------------------------------.
|  Tab   | ' "  | , <  | . >  |   P  |   Y  |                              |   F  |   G  |   C  |   R  |   L  |  Bksp  |
|--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
|Ctrl/Esc|   A  |   O  |   E  |   U  |   I  |                              |   D  |   H  |   T  |   N  |   S  |Ctrl/- _|
|--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
| LShift |  ; : |   Q  |   J  |   K  |   X  | [ {  |CapsLk|  |F-keys|  ] } |   B  |   M  |  W   |   V  |   Z  | RShift |
`----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                       |Adjust| LGUI | LAlt | Space| Nav  |  | Sym  | Enter| AltGr| RGUI | Menu |
                       `----------------------------------'  `----------------------------------'
Base Layer: QWERTY

,-------------------------------------------.                              ,-------------------------------------------.
|  Tab   |   Q  |   W  |   E  |   R  |   T  |                              |   Y  |   U  |   I  |   O  |   P  |  Bksp  |
|--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
|Ctrl/Esc|   A  |   S  |   D  |   F  |   G  |                              |   H  |   J  |   K  |   L  | ;  : |Ctrl/' "|
|--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
| LShift |   Z  |   X  |   C  |   V  |   B  | [ {  |CapsLk|  |F-keys|  ] } |   N  |   M  | ,  < | . >  | /  ? | RShift |
`----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                       |Adjust| LGUI | LAlt | Space| Nav  |  | Sym  | Enter| AltGr| RGUI | Menu |
                       `----------------------------------'  `----------------------------------'
```

</details>

## Navigation layer

```
Nav Layer: Media, navigation
 ,-------------------------------------------.                              ,-------------------------------------------.
 |        |M Prev|M Play|M Next|VolMut| BRI+ |                              |BrwsrS| PgUp | Home |  End | PgUP | Delete |
 |--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
 |        |  GUI |  Alt | Ctrl | Shift| BRI- |                              |BrwsrF|  ←   |   ↓  |  ↑   |  →   | Insert |
 |--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
 |        | Calc |      |MouseW|MouseL|MouseR|Mouse4|Mouse5|  |      |      |BrwsrB|MouseL|MouseD|MouseU|MouseR|  PrtSc |
 `----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                        |      |      |      |      | [Nav]|  |      |      |      |      |      |
                        `----------------------------------'  `----------------------------------'
```

This is where you'll find all the keys that are generally between the main block of a classic keyboard and the numpad in addition to media controls and modifiers on easy access on the home row for fast and comfortable chording with navigation keys.

## Symbols layer

```
Sym Layer: Numbers, symbols

 ,-------------------------------------------.                              ,-------------------------------------------.
 |    `   |  !   |  @   |  #   |  $   |  %   |                              |   ^  |  &   |  *   |  (   |  )   |   =    |
 |--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
 |    ~   |  1   |  2   |  3   |  4   |  5   |                              |   6  |  7   |  8   |  9   |  0   |   _    |
 |--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
 |        |  ?   |   |  |   \  |  [   |  {   |   (  |      |  |      |  )   |   }  |  ]   |   /  |      |      |   +    |
 `----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                        |      |      |      |      |      |  | [Sym]|      |      |      |      |
                        `----------------------------------'  `----------------------------------'
```

## Function layer

```
Function Layer: Function keys

,-------------------------------------------.                              ,-------------------------------------------.
|        |  F9  | F10  | F11  | F12  |      |                              |      |      |      |      |      |        |
|--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
|        |  F5  |  F6  |  F7  |  F8  |      |                              |      | Shift| Ctrl |  Alt |  GUI |        |
|--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
|        |  F1  |  F2  |  F3  |  F4  |      |      |      |  |[Fkey]|      |      |      |      |      |      |        |
`----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                       |      |      |      |      |      |  |      |      |      |      |      |
                       `----------------------------------'  `----------------------------------'
```

## Adjust layer

```
Adjust Layer: Default layer settings, RGB

 ,-------------------------------------------.                              ,-------------------------------------------.
 |        |BL_TOG|      |QWERTY| HSNT |      |                              | PLAIN|BREATH|RAINBW| SWIRL| SNAKE|KNGHTRID|
 |--------+------+------+------+------+------|                              |------+------+------+------+------+--------|
 |        |BLBRTH| BL+  |Dvorak|      |      |                              | TOG  | SAI  | HUI  | VAI  | MOD  |  XMAS  |
 |--------+------+------+------+------+------+-------------.  ,-------------+------+------+------+------+------+--------|
 |        |BL_CYC| BL-  |Colmak|      |      |      |      |  |      |      | TEST | SAD  | HUD  | VAD  | RMOD |GRADIENT|
 `----------------------+------+------+------+------+------|  |------+------+------+------+------+----------------------'
                        | [Adj]|      |      |      |      |  |      |      |      |      |      |
                        `----------------------------------'  `----------------------------------'
```

Default layer settings on the left and various RGB underglow controls on the right.

NOTE: The default layer settings set by those keys are _NOT_ stored in EEPROM and thus do not persist through boots. If you wish to change the default layer in a non-volatile manner, either change the order of the layers in the firmware, for example like so if you want to set Dvorak as the new default:

```c
enum layers {
    _DVORAK = 0,
    _QWERTY,
    _COLEMAK_DH,
    _HSNT,
    _NAV,
    _SYM,
    _FUNCTION,
    _ADJUST
};
```

or re-define the `QWERTY`, `COLEMAK` and `DVORAK` keys to point to custom keycodes starting on `SAFE_RANGE` and calling the `set_single_persistent_default_layer` function inside of `process_record_user`.

## Hardware Features

### Rotary Encoder

The left rotary encoder is programmed to control the volume whereas the right encoder sends <kbd>PgUp</kbd> or <kbd>PgDn</kbd> on every turn.

### OLEDs

The OLEDs display the current layer at the top of the active layers stack, logo and lock status (caps lock, num lock, scroll lock).
