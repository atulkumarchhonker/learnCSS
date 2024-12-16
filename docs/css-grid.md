## &#9873; CSS Grid:
These properties are used for create and manage complex layout in the webpages.

*The elements are treated as grid item. By assigning the property, `display: grid;` to the parent element.*

### &#9780; Overview:
1. [Setting Grid Items](#-setting-grid-items)
2. [Gap Property](#-gap-property)
3. [Grid Template Columns](#-grid-template-columns)
4. [Repeat Function](#-repeat-function)
5. [Grid Column](#-grid-column)
6. [Grid Row](#-grid-row)
7. [Grid Template Area](#-grid-template-area)
8. [Grid Auto Columns And Rows](#-grid-auto-columns-and-rows)
9. [Note](#-note)

### &#10022; Setting Grid Items:
It will defines the grid items for their children elements.

*Syntax: `display: grid;`*

```css
.parent-element {
  display: grid;
}
```
> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
		display: grid;		
	}
</style>

<section class="articles">
	<article>
		<img src="./images/profile-picture.jpg">
		<h3>User Name</h3>
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
		tempor incididunt ut labore et dolore magna aliqua.</p>
	</article>
	<article>
		...
	</article>
	<article>
		...
	</article>
</section>

```

### &#10022; Gap Property:
This property is used to add some space between grid items on both co-ordinates.

*Syntax: `gap: value;`*

```css
.parent-element {
  display: grid;
  gap: 1em;
}
```
> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
		display: grid;
		gap: 1em;
	}
</style>

<section class="articles">
	<article>...</article>
	<article>...</article>
	<article>...</article>
</section>
```

### &#10022; Grid Template Columns:
This will accepts space separated number of values for the property. Which taken into an account that, Each value will be considered as number of columns to be in the row of the parent container element. And assigns that column width to respective column. 

*Syntax: `grid-template-columns: value value ....;`*

> Values accepted in the Grid Template Columns
```css
grid-template-columns: 100px 100px 100px;

grid-template-columns: 5em 10em 5em;

grid-template-columns: 10rem 5rem 5rem;

grid-template-columns: 20vw 25vw 55vw;

grid-template-columns: 25% 25% 50%;

grid-template-columns: 1fr 1fr 1fr;
```

*Where, fr means fraction. It is the grid related sizing unit. If 1fr means 1 fraction. That 1fr is equal to the average value of the grid items in the row.*

```css
.parent-element {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```
> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
	  display: grid;
	  gap: 1em;
	  grid-template-columns: 1fr 1fr 1fr;
	}
</style>

<section class="articles">
	<article>...</article>
	<article>...</article>
	<article>...</article>
	<article>...</article>
	<article>...</article>
</section>

```

*The above grid-template-columns will have 3 columns in a row. And the parent has 5 grid items. The remaining grid items will be wrapped into new line and follows the previous template columns.*

### &#10022; Repeat Function:
The repeat function is used to repeat same values for number of times.

*This is useful for assigning a large and repeated columns in a `grid-template-columns` property.*

*Syntax: `grid-template-columns: repeat(number_of_times, size_of_grid_items);`*

*Repeat function can accept another function as input value.*

*Syntax: `grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));`*

```css
.parent-element {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```
> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
	  display: grid;
	  gap: 1em;
	  grid-template-columns: repeat(3, 1fr);
	}
</style>

<section class="articles">
	<article>...</article>
	<article>...</article>
	<article>...</article>
	<article>...</article>
	<article>...</article>
</section>

```

### &#10022; Grid Column:
This property is used for spanning the grid items from start and end of the specific column.

*For example, If one of the grid item to be span across the two columns than actually defined as each grid item to be one. Then it is possible as below syntax.*

*Syntax:*
```css
grid-column: span 2;
grid-column: 1 / 3;
```

*These are shorthand definition of the properties called `grid-column-start: value;` and `grid-column-end: value;`.*

*Syntax: `grid-column-start: 2; grid-column-end: 4;`* 

*The above start and end is same as `span 2`. But it exactly mentions where it should be start and end to span across.*

```css
.parent-element {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.grid-column-span-2 {
  grid-column: span 2;
}

.parent-element:last-child {
	grid-column-start: 3;
	grid-column-end: 5;
}
```
> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
	  display: grid;
	  gap: 1em;
	  grid-template-columns: repeat(3, 1fr);
	}

	.grid-column-span-2 {
	  grid-column: span 2;
	}

	.articles:last-child {
		grid-column-start: 3;
		grid-column-end: 5;
	}
</style>

<section class="articles">
	<article>...</article>
	<article class="grid-column-span-2">...</article>
	<article>...</article>
	<article class="grid-column-span-2">...</article>
	<article>...</article>
</section>

```

### &#10022; Grid Row:
This property is used for spanning the grid items from start and end of the specific row.

*For example, If one of the grid item to be span across the two rows than actually defined as each grid item to be one. Then it is possible as below syntax.*

*Syntax:*
```css
grid-row: span 2;
grid-row: 1 / 3;
grid-row: 1 / span 2;
```

*These are shorthand definition of the properties called `grid-row-start: value;` and `grid-row-end: value;`.*

*Syntax: `grid-row-start: 2; grid-row-end: 4;`* 

*The above start and end is same as `span 2`. But it exactly mentions where it should be start and end to span across.*

```css
.parent-element {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.parent-element:nth-child(3) {
	grid-row: 1 / 3;
}

.grid-column-span-2 {
  grid-column: span 2;
}

.parent-element:last-child {
	grid-column-start: 3;
	grid-column-end: 5;
}
```
> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
	  display: grid;
	  gap: 1em;
	  grid-template-columns: repeat(3, 1fr);
	}

	/* This span across two rows starting from 1st row to before 3rd row of starting point.  */
	.article:nth-child(3) {
		grid-row: 1 / 3;
	}

	.grid-column-span-2 {
	  grid-column: span 2;
	}

	.articles:last-child {
		grid-column-start: 3;
		grid-column-end: 5;
	}
</style>

<section class="articles">
	<article>...</article>
	<article class="grid-column-span-2">...</article>
	<article>...</article>
	<article class="grid-column-span-2">...</article>
	<article>...</article>
</section>
```

### &#10022; Grid Template Area:
This property is useful for designing complex layout with grid layouts. To avoid any messy spanning of the grid items then use this property with `grid-area` property for each grid item.

*With the help of `@media` query, This can create different set of layouts as much as possible.*

*In grid item, The `grid-area` defines the label or identity of it. That identity is used to create a template area with span of it.*

*This `grid-template-area` property is useful when the need for dynamic layout changes on different screen sizes.*

*Syntax:* 
```css
.child-element-1 {
	grid-area: label/identity-name;
}
.child-element-2 { ... }
.child-element-3 { ... }
.child-element-4 { ... }
.child-element-5 { ... }
.child-element-6 { ... }

.parent-element {
	grid-template-area: 'grid-items-identity' '...' '...';
}
```

*The each quotation mark in the `grid-template-area` is considered as an row span, Which is space separated grid items known by `grid-area` label or identity described before.*

*Each grid items mentioned in a row span as space separated, Each row span denoted between quotes and Each row span separated by space. Finally, need a semi-colon to end template-area definition.*

> Demonstrating with multiple article card elements
```xml

<style type="text/css">
	.articles {
		display: grid;
		gap: 1em;
		/* default layout to stack on vertically as one by one */
		grid-template-area: 
			'one'
			'two'
			'three'
			'four'
			'five';
	}
	article:first-child {
		grid-area: 'one';
	}	
	article:nth-child(2) {
		grid-area: 'two';
	}	
	article:nth-child(3) {
		grid-area: 'three';
	}	
	article:nth-child(4) {
		grid-area: 'four';
	}	
	article:last-child {
		grid-area: 'five';
	}

	@media(min-width: 768px) {
		.articles {
			grid-template-area: 
				'one one'
				'two five'
				'three five'
				'four four';
		}
	}

	@media(min-width: 1200px) {
		.articles {
			grid-template-area: 
				'one one two five'
				'three four four five';
		}
	}

</style>

<section class="articles">
	<article>
		<img src="./images/profile-picture.jpg">
		<h3>User Name</h3>
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
		tempor incididunt ut labore et dolore magna aliqua.</p>
	</article>
	<article>...</article>
	<article>...</article>
	<article>...</article>
	<article>...</article>
</section>
```


### &#10022; Grid Auto Columns And Rows:
The `grid-template-area` property will make the different layout to span across as per the definition. But the size of the grid items taken by their decision. To set default size for automatically generated column with one span of column width and row with one span of row height by this property.

*Syntax:*
```css
grid-auto-columns: 1fr;
grid-auto-rows: 1fr;

...
grid-auto-columns: 100px;
grid-auto-rows: 50px;
```

### &#10022; Note:
For changing responsive grid layout for different screen sizes, Use `@media` media query for different screen sizes.  

---
[&#8682; To Top](#-css-grid)

[&#10094; Goto Layouts Topic](./layouts.md)

[&#8962; Goto Home Page](../README.md)