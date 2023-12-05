# CSS is hard

Yep, you probably heard. CSS is hard. Here are some notes about CSS that might make this not so hard.

In CSS, there are special characters:

    ";" is used to separate individual declarations in a style rule.
    "$" is not a valid character in CSS and is typically used in preprocessors like Sass for variables.
    "#" is used to denote an ID selector in CSS.
    "~" is used in CSS to select sibling elements that are preceded by a specified element.
    "" is used to escape special characters in CSS.
    "'" and """ are used to denote strings in CSS.
    "/" is used to separate parts of a CSS property value, such as in the case of specifying a font stack.
    "" is used as the multiplication operator in CSS, and also in the case of the universal selector "".
    "@" is used to denote at-rules in CSS, such as @media or @import.
    "!" is used in CSS to denote the important flag, which gives a declaration higher priority.
    "{" and "}" are used to enclose the declarations within a style rule.
    ":" are used for pseudo-classes, which are used to define the special state of an element. For example, ":hover" is a pseudo-class that matches when the user designates an element (with some pointing device), but does not activate it. Another example is ":visited", which matches links that have been visited by the user.
    "::" are used for pseudo-elements, which are used to style specified parts of an element. For example, "::first-line" is a pseudo-element that matches the first formatted line of a paragraph.
    "," is used to separate multiple selectors in a rule, allowing the rule to apply to several elements. For example, "h1, h2, h3" will apply the same style to all h1, h2, and h3 elements.
    "." is used to denote a class selector in CSS. It is followed by the class
    "&" is used in preprocessors like Sass and LESS to reference the parent selector in nested selectors.
    "*" is used as the universal selector in CSS to select any element.
    name and is used to select elements with a specific class attribute. For example, ".example" will select all elements with the class "example".

There are various types of selectors in CSS that are used to target HTML elements for styling. Some of the key types of selectors include:

    Type selectors: Select elements based on their element type (e.g., p for paragraphs, h1 for headings).
    Class selectors: Select elements based on their class attribute (e.g., .example for elements with class "example").
    ID selectors: Select a single element based on its ID attribute (e.g., #header for an element with id "header").
    Attribute selectors: Select elements based on the presence or value of their attributes (e.g., [type="text"] selects input elements with type "text").
    Pseudo-classes and pseudo-elements: Select elements based on their state or position in the document (e.g., :hover, :first-child, ::before).
    Combinators: Select elements based on their relationship to other elements (e.g., descendant combinator, child combinator).

CSS selectors and rules should not be empty and your editor or IDE might even warn you about that.

    ```css
    body {

    };

    ```

## CSS Variables

CSS variables, also known as custom properties, are entities defined by CSS authors that represent specific values to be reused throughout a document. They are set using the @property at-rule or by custom property syntax (e.g., --primary-color: blue;). Custom properties are accessed using the CSS var() function (e.g., color: var(--primary-color);). They allow a value to be defined in one place and then referenced in multiple other places, making it easier to work with and improving readability and semantics. CSS variables can have global or local scope, and they can be changed with JavaScript and based on media queries. They are useful for managing websites with numerous similar values, reducing the friction associated with refactoring or updating code

To declare a CSS variable, you use the following syntax:

	```css
	:root {
	--primary-color: blue;
	}

	.element {
	color: var(--primary-color);
	}
```

In this example, --primary-color is the variable name, and blue is the value. The variable is then accessed using the var() function, as shown in the color property of the .element selector

CSS variables provide a more efficient way to write and manage CSS code, making it easier to maintain and update styles across a project. They are particularly beneficial for larger projects where consistency and maintainability are crucial.
