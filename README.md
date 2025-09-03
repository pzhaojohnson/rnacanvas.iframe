Here's a [live example](https://codepen.io/xmsdtxld-the-lessful/pen/GgpwEKK) on CodePen.

# Quickstart

For example, to draw the following structure...

```
AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC
(((((((....)))))))...(((((((((((.....(((((.......)))))..))))))))))).....
```

...one would set the `src` attribute of an `<iframe>` element to the following.

```javascript
// JavaScript code to construct the `src` attribute
var src = 'https://code.rnacanvas.app?'
  + 'sequence=AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC'
  + '&dot_bracket=(((((((....)))))))...(((((((((((.....(((((.......)))))..))))))))))).....';
```

The resulting `<iframe>` element would look like:

```html
<iframe
  src="https://code.rnacanvas.app?sequence=AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC&dot_bracket=(((((((....)))))))...(((((((((((.....(((((.......)))))..)))))))))))....."

  width="800"
  height="600"
></iframe>
```

<b>The above</b> `<iframe>` <b>HTML code can be directly copy-and-pasted into a website (such as</b> [CodePen](https://codepen.io/pen/)<b>).</b>

In this case, the `<iframe>` element is given a width of `800` pixels and a height of `600` pixels.

The `sequence` and `dot_bracket` URL parameters of the RNAcanvas [URL interface](https://pzhaojohnson.github.io/rnacanvas.url-interface/)
are made use of in this example.

### Hiding the peripheral UI

To hide things like the lower-left Toolbar and top-left `Open`, `Save` and `Export` buttons,
set the `peripheral_ui` URL parameter to `none`.

```javascript
// JavaScript code to construct the `src` attribute
var src = 'https://code.rnacanvas.app?'
  + 'sequence=AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC'
  + '&dot_bracket=(((((((....)))))))...(((((((((((.....(((((.......)))))..))))))))))).....'

  // set to "none"
  + '&peripheral_ui=none';
```

### Showing a minimal peripheral UI

To show a minimalistic peripheral UI,
set the `peripheral_ui` URL parameter to `minimal`.

```javascript
// JavaScript code to construct the `src` attribute
var src = 'https://code.rnacanvas.app?'
  + 'sequence=AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC'
  + '&dot_bracket=(((((((....)))))))...(((((((((((.....(((((.......)))))..))))))))))).....'

  // set to "minimal"
  + '&peripheral_ui=minimal';
```

This will result in only a top-right `Edit` button being shown,
which when clicked will reopen the drawing in a new tab of RNAcanvas
possessing the full peripheral UI.

### Hiding / styling the border

By default, `<iframe>` elements usually have an indented gray border.

To hide this, one can set the `border` CSS property to `none`.

```html
<iframe
  src="https://code.rnacanvas.app?sequence=AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC&dot_bracket=(((((((....)))))))...(((((((((((.....(((((.......)))))..)))))))))))....."

  width="800"
  height="600"

  style="border: none;"
></iframe>
```

Alternatively, the border can be styled as with any HTML element.

```html
<iframe
  src="https://code.rnacanvas.app?sequence=AGAGUAGCAUUCUGCUUUAGACUGUUAACUUUAUGAACCACGCGUGUCACGUGGGGAGAGUUAACAGCGCCC&dot_bracket=(((((((....)))))))...(((((((((((.....(((((.......)))))..)))))))))))....."

  width="800"
  height="600"

  style="border: 1px solid #bbb;"
></iframe>
```

# Coloring bases according to data

Bases can be given colored outlines according to data
(e.g., base-pair probability data, positional entropy data).

See the [Coloring bases according data](https://pzhaojohnson.github.io/rnacanvas.url-interface/) section
of the RNAcanvas URL interface documentation for more information.

# Advanced methods

The JavaScript / TypeScript interface of the RNAcanvas app object
can also be used to draw nucleic acid structures
(documentation [here](https://pzhaojohnson.github.io/rnacanvas.embedded/)).

Usage of the JavaScript / TypeScript interface
allows for granular script-based control of nucleic acid structure drawings.
