## &#9873; Color and Background
These properties can apply the colors to the elements.

*There are 3 popular color models used in CSS. That are RGB, HSL, HEX.*

### &#9780; Overview:
1. [Color models](#-color-models)
2. [Color Opacity](#-color-opacity)
3. [Background color](#-background-color)
4. [Background images](#-background-images)
5. [Background positioning](#-background-positioning)
6. [Background repetition](#-background-repetition)
7. [Background attachment](#-background-attachment)
8. [Gradient Text](#-gradient-text)

### &#10022; Color models:
- RGB (Red Green Blue) Color Model:
  - It represents colors by combining varying intensities of red, green, and blue colors.
  - *Syntax: `rgb(red, green, blue)`*

  ```css
  color: rgb(255, 0, 0); // Red
  ```
- HSL (Hue Saturation Lightness) Color Model:
  - It represents colors using hue (color), saturation (intensity), and lightness (brightness).
  - *Syntax: `hsl(hue, saturation%, lightness%)`*

  ```css
  color: hsl(0, 100%, 50%); // Red
  ```
- Hexadecimal (HEX) Color Model:
  - It represents colors using a six-character hexadecimal code (e.g., #RRGGBB) or in the 3 character short-code.
  - *Syntax: `#RRGGBB` or `#RGB`*

  ```css
  color: #ff0000; // Red
  ```

### &#10022; Color Opacity:
- RGBA (Red Green Blue Alpha) Color Model:
  - It represents colors by combining varying intensities of red, green, and blue colors with alpha transparency for opacity of the color value. 
  - Alpha value ranges from `0` - no opacity to `1` - full opacity.
  - *Syntax: `rgb(red, green, blue, alpha)`*

  ```css
  color: rgba(255, 0, 0, 1); // Red
  ```
- HSLA (Hue Saturation Lightness Alpha) Color Model:
  - It represents colors using hue (color), saturation (intensity), and lightness (brightness) with alpha transparency for opacity of the color value. 
  - Alpha value ranges from `0` - no opacity to `1` - full opacity..
  - *Syntax: `hsla(hue, saturation%, lightness%, alpha)`*

  ```css
  color: hsla(0, 100%, 50%, 1); // Red
  ```
- Hexadecimal (HEX) Color Model:
  - It represents colors using a six-character hexadecimal code (e.g., #RRGGBB) or in the 3 character short-code with alpha transparency for opacity of the color value. 
  - Alpha value ranges from `0` - no opacity to `f` - full opacity for short-code or `00` to `ff` for six-character hexadecimal code.
  - *Syntax: `#RRGGBBAA` or `#RGBA`*

  ```css
  color: #ff0000ff; // Red
  ```

### &#10022; Background color:
It sets the background color of an element.

*Syntax: `background-color: value;`*

```css
div {
  background-color: #f0f0f0;
}
```

### &#10022; Background images:
It adds an image to the background of an element.

*Syntax: `background-image: url(url);`*

```css
body {
  background-image: url("image.jpg");
}
```

### &#10022; Background positioning:
It specifies the position of a background image within an element

*Syntax: `background-position: value;` or `background-position: x-position y-position;`*

```css
div {
  background-position: center;
}
```

### &#10022; Background repetition:
It controls how a background image is repeated

*Syntax: `background-repeat: value;`*

```css
div {
  background-repeat: no-repeat;
}
```

### &#10022; Background attachment:
It determines whether a background image scrolls with the content or remains fixed.

*Syntax: `background-attachment: value;`*

```css
body {
  background-attachment: fixed;
}
```

### &#10022; Gradient Text:
The linear gradient property does not work with text. But it can be done with `background-clip`property.

```css
h1 {
  background: linear-gradient(to right, red, blue);
  background-clip: text;
  color: transparent;
}
```

---
[&#8682; To Top](#-color-and-background)

[&#10094; Previous Topic](../docs/text-styling.md) &emsp; [Next Topic &#10095;](../docs/layouts.md)

[&#8962; Goto Home Page](../README.md)
