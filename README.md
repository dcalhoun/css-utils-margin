# css-utils-margin
Immutable, CSS margin utilities.

## Naming Convention
Due to the ubiquitous nature of setting margin, these utilities use a shorthand
naming convention.

| Shorthand | Description                |
| --------- | -----------                |
| m         | Margin                     |
| t         | Top                        |
| r         | Right                      |
| b         | Bottom                     |
| l         | Left                       |
| x         | XAxis (left and right)     |
| y         | YAxis (top and bottom)     |
| n         | Negative                   |
| 0         | 0 reset                    |
| 1         | --space-1 (default 0.5rem) |
| 2         | --space-2 (default 1rem)   |
| 3         | --space-3 (default 2rem)   |
| 4         | --space-4 (default 4rem)   |

Change or reset default margins using the white space scale. Negative u-xAxis
margins are used to offset margins and padding of child elements. Margin auto is
used to horizontally center block-level elements with a set width.

```css
.u-m0  { margin:        0 }
.u-mt0 { margin-top:    0 }
.u-mr0 { margin-right:  0 }
.u-mb0 { margin-bottom: 0 }
.u-ml0 { margin-left:   0 }
.u-mx0 { margin-left:   0; margin-right:  0 }
.u-my0 { margin-top:    0; margin-bottom: 0 }

.u-m1  { margin:        var(--space-1) }
.u-mt1 { margin-top:    var(--space-1) }
.u-mr1 { margin-right:  var(--space-1) }
.u-mb1 { margin-bottom: var(--space-1) }
.u-ml1 { margin-left:   var(--space-1) }
.u-mx1 { margin-left:   var(--space-1); margin-right:  var(--space-1) }
.u-my1 { margin-top:    var(--space-1); margin-bottom: var(--space-1) }

.u-m2  { margin:        var(--space-2) }
.u-mt2 { margin-top:    var(--space-2) }
.u-mr2 { margin-right:  var(--space-2) }
.u-mb2 { margin-bottom: var(--space-2) }
.u-ml2 { margin-left:   var(--space-2) }
.u-mx2 { margin-left:   var(--space-2); margin-right:  var(--space-2) }
.u-my2 { margin-top:    var(--space-2); margin-bottom: var(--space-2) }

.u-m3  { margin:        var(--space-3) }
.u-mt3 { margin-top:    var(--space-3) }
.u-mr3 { margin-right:  var(--space-3) }
.u-mb3 { margin-bottom: var(--space-3) }
.u-ml3 { margin-left:   var(--space-3) }
.u-mx3 { margin-left:   var(--space-3); margin-right:  var(--space-3) }
.u-my3 { margin-top:    var(--space-3); margin-bottom: var(--space-3) }

.u-m4  { margin:        var(--space-4) }
.u-mt4 { margin-top:    var(--space-4) }
.u-mr4 { margin-right:  var(--space-4) }
.u-mb4 { margin-bottom: var(--space-4) }
.u-ml4 { margin-left:   var(--space-4) }
.u-mx4 { margin-left:   var(--space-4); margin-right:  var(--space-4) }
.u-my4 { margin-top:    var(--space-4); margin-bottom: var(--space-4) }

.u-mxn1 { margin-left: -var(--space-1); margin-right: -var(--space-1); }
.u-mxn2 { margin-left: -var(--space-2); margin-right: -var(--space-2); }
.u-mxn3 { margin-left: -var(--space-3); margin-right: -var(--space-3); }
.u-mxn4 { margin-left: -var(--space-4); margin-right: -var(--space-4); }

.u-mlAuto { margin-left: auto }
.u-mrAuto { margin-right: auto }
.u-mxAuto { margin-left: auto; margin-right: auto; }
```

## Resetting Margins
To increase information density and to better align elements, remove default
margins from typographic elements using the margin utilities.

```html
<h1 class="u-m0">No margin</h1>
<h1 class="u-mt0">No margin top</h1>
<h1 class="u-mb0">No margin bottom</h1>
```

## Add Spacing
Add spacing around elements using a combination of margin utilities.

```html
<div class="u-mxn1">
  <div class="u-m1">Hamburger</div>
  <div class="u-m1">Hamburger</div>
  <div class="u-m1">Hamburger</div>
</div>
```

The negative margin utilities also work with padded children.

```html
<div class="border">
  <div class="u-mxn2">
    <div class="u-px2 border">Padded div</div>
  </div>
</div>
```

## Center Elements
Block elements with a set width can be centered with `.u-mxAuto`.

```html
<img src="http://d2v52k3cl9vedd.cloudfront.net/assets/images/placeholder-square.svg"
  width="96"
  height="96"
  class="block u-mxAuto" />
```

## Credits
This utility is heavily inspired by [Basscss](http://www.basscss.com) and
[SuitCSS](http://suitcss.github.io). This repository is merely a combining of
great principles championed by each.
