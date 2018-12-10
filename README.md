# CSS - Playground

Have come across any new implementation of CSS or just want to dive deep into the some existing concept. 
Here is my personal notebook of CSS that will consist live examples as well as notes. I will try to keep 
it minimal and simple so it can benefit others.

> Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG, MathML or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

> **// TODO: Under Construction**

___

## Index

- [How CSS works](#how-css-work)
    - Classification of CSS statements
    - Anatomy of CSS rule
    - Rendering
    - Ways to write CSS rules
- [CSS rules - deep dive](#css-rules-deep)
- [Code snippets]()
- [Best practices]()

___

## How CSS works<a name="how-css-work"></a>

CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

- A **document** is usually a text file structured using a markup language
- **Presenting** a document to a user means converting it into a usable form for your audience.
- **Web browsers** apply **CSS rules** to a document to affect how they are displayed.

### Classification of CSS statements

![Classification of CSS Statements](resources/css-statements.png)

- **CSS Rules** are the main building blocks of a style sheet — the most common block you'll see in CSS.
- **At-rules** are used in CSS to convey metadata, conditional information, or other descriptive information. They start with an at sign (@), followed by an identifier to say what kind of rule it is


### Anatomy of CSS rules

![Anatomy of CSS Rule](resources\css-declaration.png)

- **Selector:**, which selects the element(s) you want to apply the updated property values to. 
- **Property:** Human-readable identifiers that indicate which stylistic features you want to change. 
- **Value:**  Each specified property is given a value, which indicates how you want to change those stylistic features.
- **Declaration:** A property paired with a value.
- **CSS declarations** are put within **CSS Declaration Blocks**.
- **CSS declaration blocks** are paired with **selectors** to produce **CSS Rulesets** (or CSS Rules).

### Rendering

1. The browser converts **HTML** and **CSS** into the **DOM (Document Object Model)**. The DOM represents the document in the computer's memory. It combines the document's content with its style.
2. The browser displays the contents of the **DOM**.
3. The **CSS engine** calculates which declarations apply to every single element of a page in order to appropriately lay it out and style it.
4. If a **property** is unknown or if a **value** is not valid for a given **property**, the declaration is deemed invalid and is wholly ignored by the browser's **CSS engine**.


![How HTML and CSS Renders](resources\Html-Css-Rendering.svg)

### Ways to write CSS rules

| # | way used to apply css | Pros        | Cons        |
|---|-----------------------|-------------|-------------|
| 1 | External Stylesheet   | Can be used for multiple documents. Easy to maintain, Best approach | _
| 2 | Inernal Stylesheet    | Better than Inline, Relatively easy to maintain | Scope is limited to particular document, Should be avoided.
| 3 | Inline Stylesheet     | Last resort, Must be avoided | Scope is limited to particular element, redundancy is highest, Really difficult to Maintain

___

## CSS - deep dive<a name="css-rules-deep"></a>

- ### Selectors

1.  **Simple selectors:** Match one or more elements based on `element type`, `class`, or `id`.
2.  **Attribute selectors:** Match one or more elements based on their `attributes/attribute values`.
3.  **Pseudo-classes:** Match one or more elements that exist in a certain state, such as an element that is being hovered over by the mouse pointer, or a checkbox that is currently `disabled` or `checked`, or an element that is the first child of its parent in the DOM tree.
4.  **Pseudo-elements:** Match one or more parts of content that are in a certain position in relation to an element, for example the first word of each paragraph, or generated content appearing just before an element.
5.  **Combinators:** These are not exactly selectors themselves, but ways of combining two or more selectors in useful ways for very specific selections. So for example, you could select only paragraphs that are direct descendants of divs, or paragraphs that come directly after headings. We can also refer selectors are **chained**.
6.  **Multiple selectors:** Again, these are not separate selectors; the idea is that you can put multiple selectors on the same CSS rule, separated by commas, to apply a single set of declarations to all the elements selected by those selectors.
7.  An element may be matched by several selectors, therefore several rules may set a given property multiple times.
8.  CSS defines which one has **precedence** over the others and must be applied: this is called the `cascade algorithm`.

#### Classification of selectors

![Classification of CSS Selectors](resources/css-selectors.png)

---

## Code Snippets

1. [Stackblitz - code snippet - CSS selectors invalid selector in group or chain](https://stackblitz.com/edit/css-selector-experiment)

---

## Best Practices

1. You can add white space to make your style sheets more readable.
2. Add comments

