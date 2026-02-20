# CSS (Cascading Style Sheets)

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML or XML. It allows developers to separate content from design, enabling more flexibility and control over the layout and appearance of web pages.

Types:

- **Inline CSS**: Applied directly within an HTML element using the `style` attribute.
- **Internal CSS**: Defined within a `<style>` tag in the `<head>` section of an HTML document.
- **External CSS**: Linked to an external stylesheet using the `<link>` tag.

## Advantages of CSS

- Separation of content and design.
- Improved website maintainability.
- Enhanced page load speed by reducing HTML file size.
- Greater control over layout and design.

## Disadvantages of CSS

- Browser compatibility issues.
- Learning curve for beginners.
- Complexity in managing large stylesheets.
- Segmentation of styles across multiple files.

Basic Syntax:

```css
selector {
    property: value;
}
```

- **Selector**: Specifies the HTML element(s) to be styled.
- **Property**: The CSS property to be modified (e.g., color, font-size).
- **Value**: The value assigned to the property.
Example:

```css
body {
    background-color: lightblue;
}
h1 {
    color: navy;
    font-size: 24px;
}
```

Common Properties:

- `color`: Sets the text color.
- `background-color`: Sets the background color of an element.
- `font-size`: Sets the size of the font.
- `margin`: Sets the space outside the element's border.
- `padding`: Sets the space inside the element's border.
- `border`: Sets the border around an element.
- `display`: Controls the layout behavior of an element (e.g., block, inline, flex).
- `position`: Specifies the positioning method of an element (e.g., static, relative, absolute, fixed).
- `width` and `height`: Set the dimensions of an element.

Selectors:

- **Element Selector**: Selects all elements of a specific type (e.g., `p`, `h1`).
- **Class Selector**: Selects elements with a specific class attribute (e.g., `.classname`).
- **ID Selector**: Selects a single element with a specific ID attribute (e.g., `#idname`).
- **Universal Selector**: Selects all elements (`*`).
- **Attribute Selector**: Selects elements based on an attribute or attribute value (e.g., `[type="text"]`).
- **Pseudo-class Selector**: Selects elements based on their state (e.g., `:hover`, `:first-child`).
- **Pseudo-element Selector**: Selects and styles a part of an element (e.g., `::before`, `::after`).

## Media Queries

Media queries allow for responsive design by applying different styles based on the device's characteristics, such as screen width.

```css
@media (max-width: 600px) {
    body {
        background-color: lightgray;
    }
}
```

This example changes the background color to light gray for screens that are 600 pixels wide or smaller.

## CSS Frameworks

CSS frameworks are pre-prepared libraries that make it easier to design web pages. They provide a set of CSS classes and components that can be used to create responsive and consistent designs quickly. Popular CSS frameworks include Bootstrap, Foundation, and Bulma.

## Conclusion

CSS is an essential tool for web development, enabling developers to create visually appealing and user-friendly websites. By mastering CSS, developers can enhance the user experience and ensure that their web pages look great across different devices and screen sizes.
