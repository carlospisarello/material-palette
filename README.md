# material-palette
Material palette is the lightweight sass library of material colors.

The library consists of one single .scss file with simple utils to use [material design colors](https://material.io/design/color/).

There are two ways in which you can take advantage of the library:

## Using Material palette with classes

Material palette includes classes with `color` and `background-color` css properties, it's as simple as writing the name of the color, the number on the scale and the lightness desired and the optional accent keyword

```
<h1 class="red-400-light-accent">This title will be rendered with the light accented Red 400 color</h1> 
```
The classes consist of four segments:

### Color

Any of the 19 color of the [material design colors](https://material.io/design/color/) palette. it must be lowercased and must not have spaces (e.g. Light Blue would be lightblue).

### Scale number.

Must match one of the 10 sclae numbers of the palette, (`50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`).

### Lightness (optional).

Has three possible values: `neutral`, `light` and `dark`.

### Accent (optional).

If we add the word `accent`, the accented color will be rendered (Note that accent colors is only available in 4 scale numbers: `50`, `200`, `400` and `700`).

Following the previous rules, we can render any color of the palette:

*Accented Red 400 light*: `red-400-light-accent`.
*Light Blue 900*: `lightblue-900`.
*Green 900 dark*: `green-900-dark`.

### Background prefix

If we add the `bg-` prefix to the class, the color will be applied to the background of the element and not the text.

```
<div class="bg-teal-700-dark bluegrey-50">
  <p>This is a dark Teal 700 div element with a Blue Grey 50 text</p>
</div>
```

## Using material function to get color value

The second option is get any color of the palette with the `material()` function. This is useful if you do not want to use the library classes, or want to add material colors to properties the classes doesn't cover (Such as `border` or using it with the `gradient` function)

The function receives four params:

#### material($color, $scale, $lightness(optional), $type(optional))

### Color

*String*. Any of the 19 color of the [material design colors](https://material.io/design/color/) palette. it must be lowercased and must not have spaces (e.g. Light Blue would be lightblue).

### Scale number.

*Number*. Must match one of the 10 sclae numbers of the palette, (`50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`).

### Lightness (optional).

*String*. Has three possible values: `"neutral"`, `"light"` and `"dark"`. The default value is `"neutral"`, we can type `null` if we want to ommit this param.

### Type (optional).

*String*. Has two possible values: `"regular"` and `"accent"`. The default value is `"regular"`.

## material() function use examples.

Set the `border-color` property to accented Deep Orange 700:

`border-color: material("deeporange", 700, null, "accent")`

Manually set the `background-color` property to light Lime 500:

`border-color: material("deeporange", 700, "light")`



