# CSS is hard

Yep, you probably heard. CSS is hard. Here are some notes about CSS that might make this not so hard.

CSS files have the extension `.css` and typically these files are named `style.css` or `styles.css`.

You can also use inline CSS in a `.html` file by using the `<style>` tag.

If you create CSS files, they need to be linked to the html by using a `<link>` tag.  This goes inside the `<head>` near the top of the HTML file, otherwise the browser will not know where the CSS is linked to.

This is typically done using the following line

    `<link rel="stylesheet" type="text/css" href="styles.css" />`

The type attribute is not required in HTML5 so you can:

    `<link rel="stylesheet" href="styles.css" />`

Calling the paths to the `.css` file are very important in this tag, as the browser may not be able to find it if you don't have the path correct.
It may also issue a cors error in the browser console.

CSS stylesheets and .css files can use both relative and absolute paths. A relative path is used to link the CSS file relative to the location of the HTML file. On the other hand, an absolute path is the full URL to the file, specifying the complete location from the root of the website. When using a relative path, the href attribute in the link tag should specify the file path of the CSS file relative to the location of the HTML file. For example, if the CSS file is in a subdirectory, the link would be:

    `<link rel="stylesheet" type="text/css" href="subdirectory/style.css" />`

If the CSS file is in the parent directory of the HTML file, the link would be:

    `<link rel="stylesheet" type="text/css" href="../style.css" />`

On the other hand, absolute paths specify the complete URL to the file, for example:

    `<link rel="stylesheet" type="text/css" href="https://www.example.com/style.css" />`

Using relative paths is generally considered a best practice, as it makes the file paths more flexible and portable, working regardless of the website’s domain or root folder structure

The choice between inline CSS and included (external) CSS can impact performance and maintainability. Here are some insights:

    Performance:
        Inline CSS: Reduces the number of files the browser needs to download before displaying the web page, potentially leading to faster loading. However, inline CSS is not cached, so it may impact performance on subsequent visits.
        External CSS: Allows the browser to cache the CSS file, leading to improved efficiency on subsequent visits. It also enables parallel downloading of resources, which can enhance performance

    Maintainability:
        Inline CSS: Adding CSS rules to every HTML element can make the HTML structure messy and affect page size and download time. It's not recommended for managing an entire website's styles.
        External CSS: Provides a more organized and maintainable way to manage styles, especially for larger projects. It also promotes reusability and easier maintenance.

## Global Styles

Global styles in CSS refer to styles that are applied to the entire document or website, rather than being limited to a specific component or element. They can be achieved in several ways, such as by using the `:root` or `<body>` elements, the unqualified `*` selector, or by creating and importing global CSS files. Global styles are important for creating a consistent and efficient design system, as they allow for the separation of branding/aesthetic from layout, and the treatment of the two as separate concerns.

Typical CSS files that are used to contain global styles are `index.css` and `app.css` (if your page/site is a PWA or App or Web App).

## Special Characters

In CSS, there are special characters:

- ";" is used to separate individual declarations in a style rule.

- "$" is not a valid character in CSS and is typically used in preprocessors like Sass for variables.

- "#" is used to denote an ID selector in CSS.

- "~" is used in CSS to select sibling elements that are preceded by a specified element.

- "" is used to escape special characters in CSS.

- A ' and " character are used to denote strings in CSS.

- "/" is used to separate parts of a CSS property value, such as in the case of specifying a font stack.

- A space is used as the multiplication operator in CSS, and also in the case of the universal selector "".

- "@" is used to denote at-rules in CSS, such as @media or @import.

- "!" is used in CSS to denote the important flag, which gives a declaration higher priority.

- "{" and "}" are used to enclose the declarations within a style rule.

- ":" are used for pseudo-classes, which are used to define the special state of an element. For example, ":hover" is a pseudo-class that
matches when the user designates an element (with some pointing device), but does not activate it. Another example is ":visited", which
matches links that have been visited by the user.

- "::" are used for pseudo-elements, which are used to style specified parts of an element. For example, "::first-line" is a pseudo-element that matches the first formatted line of a paragraph.

- "," is used to separate multiple selectors in a rule, allowing the rule to apply to several elements. For example, "h1, h2, h3" will apply the same style to all h1, h2, and h3 elements.

- "." is used to denote a class selector in CSS. It is followed by the class name and is used to select elements with a specific class attribute. For example, ".example" will select all elements with the class
"example".

- "&" is used in CSS preprocessors like Sass and LESS to reference the parent selector in nested selectors.

- "*" is used as the universal selector in CSS to select any element.

There are various types of selectors in CSS that are used to target HTML elements for styling. Some of the key types of selectors include

- Type selectors: Select elements based on their element type (e.g., p for paragraphs, h1 for headings).

 A CSS type selector, also known as a tag name selector or element selector, matches elements by their node name, selecting all elements of the given type within a document. It is used to style HTML elements based on their tag names. For example, to select all <p> elements and center-align them, you can use the following CSS rule:

    p {
    text-align: center;
    }

 Type selectors are not case-sensitive, and they can be combined with other selectors to target specific elements. They are one of the simplest and most frequently used selectors in CSS

- Class selectors: Select elements based on their class attribute (e.g., .example for elements with class "example").

 For instance, A CSS class selector is used to select HTML elements with a specific class attribute. It is denoted by a period (.) followed by the class name. To use it, you can define a class in your CSS file and then apply that class to HTML elements in your document. For example, to create a class called "highlight" and apply it to certain elements, you can use the following CSS rule:

    .highlight {
    background-color: yellow;
    }

And in your HTML document:

    ```html
    <p class="highlight">This is a highlighted paragraph.</p>
    <div class="highlight">This is a highlighted div.</div>
    ```

This will apply the specified styles to all elements with the "highlight" class. Class selectors allow you to apply unique style properties to groups of HTML elements to achieve your desired web page appearance

- ID selectors: Select a single element based on its ID attribute (e.g., #header for an element with id "header").

    A CSS ID selector is used to select a specific HTML element based on the value of its id attribute, which must be unique within a page. To use an ID selector in CSS, you write a hash (#) followed by the ID of the element, and then define the style properties you want to apply to the element in curly brackets. Here's an example of how to use an ID selector:

    #idname {
      Define properties here
    }

The IDs are used to identify a single element, and they have a higher specificity than classes, making them useful for applying specific styles to individual elements. In contrast, a class selector is used to select elements with a specific class attribute, and it can be applied to multiple elements. Here's an example of a class selector:

    .class-name {
      /* Define properties here */
    }

In general, it's a best practice to use IDs for unique elements and classes for multiple elements, and to avoid using IDs for styling purposes in order to keep the styling separate from the content

- Attribute selectors: Select elements based on the presence or value of their attributes (e.g., [type="text"] selects input elements with type "text").

CSS attribute selectors are used to select elements based on the presence of certain attributes or the values of those attributes. There are different types of attribute selectors that can be used:

- Presence and value selectors: These selectors enable the selection of an element based on the presence of an attribute alone, or on various different matches against the value of the attribute. For example, to select all `<a>` elements with a target attribute, you can use the following selector: a[target]. To select elements with a specific attribute value, you can use a selector like this: a[href="https://example.com"].

- Substring matching selectors: These selectors allow for more advanced matching of substrings inside the value of your attribute. For example, to select elements with an attribute value that contains a specific word, you can use a selector like this: [title~="flower"]. There are also selectors for matching attribute values that start with a specific value, end with a specific value, or contain a specific value.

Attribute selectors provide a powerful way to target and style elements based on their attributes, giving you more flexibility and control over the styling of your web pages

- Pseudo-classes and pseudo-elements: Select elements based on their state or position in the document (e.g., :hover, :first-child, ::before).

- Combinators: Select elements based on their relationship to other elements (e.g., descendant combinator, child combinator).

CSS rules should not be empty and your editor or IDE might even warn you about that:

    body {
       /* Not a great idea to leave this part empty */
    };

## CSS Variables

CSS variables, also known as custom properties, are entities defined by CSS authors that represent specific values to be reused throughout a document. They are set using the @property at-rule or by custom property syntax (e.g., --primary-color: blue;). Custom properties are accessed using the CSS var() function (e.g., color: var(--primary-color);). They allow a value to be defined in one place and then referenced in multiple other places, making it easier to work with and improving readability and semantics. CSS variables can have global or local scope, and they can be changed with JavaScript and based on media queries. They are useful for managing websites with numerous similar values, reducing the friction associated with refactoring or updating code

To declare a CSS variable, you use the following syntax:

    :root {
    --primary-color: blue;
    }

    .element {
    color: var(--primary-color);
    }

In this example, --primary-color is the variable name, and blue is the value. The variable is then accessed using the var() function, as shown in the color property of the .element selector

CSS variables provide a more efficient way to write and manage CSS code, making it easier to maintain and update styles across a project. They are particularly beneficial for larger projects where consistency and maintainability are crucial.

## Other basic CSS stuff you should know if you don't already

The universal selector in CSS is denoted by an asterisk (*) and is used to select all elements on an HTML page. It matches elements of any type and can be used to apply styles globally. Here's a brief overview of how to use the universal selector:

    * {
      margin: 0;
      padding: 0;
      /*Add more global styles here*/
    }

The universal selector selects all elements and can also be used to select all elements inside another element. It is a powerful tool for applying styles globally, but it's important to use it judiciously as it can affect the performance of the page if overused.

This section should only get CSS rule applied to it that will be the same across the page or pages you intend to style.

It is valuable tool for applying styles to all elements on a page and can be used to set global styles. However, it should be used carefully to avoid unintended consequences on the page's performance.

## CSS Media Queries and other important usage of @

In addition to @media and @import, there are other @ rules in CSS that serve different purposes. Some of the commonly used @ rules include:

- @font-face: This rule is used to define custom fonts and enable you to use them in your CSS. It allows you to specify a font's name and provide the source of the font file.

- @keyframes: This rule is used to define animations in CSS. It allows you to specify the styles that should be applied at various points during the animation.

- @supports: This rule is used to apply a block of styles only if a certain condition is true. It allows you to write a style block that will only be applied if the browser supports a certain feature.

- @page: This rule is used to specify the style of a page when printed. It allows you to set the margins, size, and orientation of the printed page.

These @ rules provide additional functionality and flexibility to CSS, allowing you to define custom fonts, create animations, apply styles conditionally, and specify the style of printed pages

When using @media queries, both min-width and max-width are important, but their usage depends on the specific design approach.

Use min-width when following a "mobile-first" approach, where the default styles are for mobile and then enhanced for larger screens. This means the styles will be applied when the viewport width is equal to or greater than the specified width.

Use max-width when following a "desktop-first" approach, where the default styles are for larger screens and then adjusted for smaller screens. This means the styles will be applied when the viewport width is equal to or less than the specified width

For example, to apply styles when the viewport width is less than or equal to 600px, you would use @media (max-width: 600px) { ... }
Both min-width and max-width are essential for creating responsive designs that adapt to various screen sizes and devices2
The choice between min-width and max-width depends on the specific design strategy, such as mobile-first or desktop-first, and the behavior you want to achieve for different screen sizes.

In short, min-width is suitable for applying styles as the viewport width increases, following a mobile-first approach. On the other hand, max-width is used for applying styles as the viewport width decreases, following a desktop-first approach

## Advanced CSS

To use the :root pseudo-class in CSS, you can define global CSS variables and apply styles to the root element of the document. Here's a brief overview of how to use it:

    :root {
      --main-color: hotpink;
      --pane-padding: 5px 42px;
      /* Add more global variables and styles here */
    }

The :root pseudo-class matches the root element of a document, which is typically the `<html>` element in HTML. It is similar to the html selector but has higher specificity, making it useful for declaring global CSS variables that can be accessed throughout the document

One practical benefit of using :root is that it allows you to declare global CSS variables that are accessible throughout the HTML code. Additionally, variables set in :root can be used to style SVG graphics, which is not possible with the html selector

It is a useful tool for defining global CSS variables and applying styles to the root element of a document, providing a convenient way to manage styles across a project.
