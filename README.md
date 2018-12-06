# CSS - Playground

Have come across any new implementation of CSS or just want to dive deep into the some existing concept. 
Here is my personal notebook of CSS that will consist live examples as well as notes. I will try to keep 
it minimal and simple so it can benefit others.

> Cascading Style Sheets (CSS) is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG, MathML or XHTML). CSS describes how elements should be rendered on screen, on paper, in speech, or on other media.

> **// TODO: Under Construction**

___

## Index

- [How CSS works](#how-css-work)
    - Anatomy of CSS rule
    - Rendering
    - Ways to write CSS rules
- [CSS rules - deep dive](#css-rules-deep)

___

## How CSS works<a name="how-css-work"></a>

CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.

- A **document** is usually a text file structured using a markup language
- **Presenting** a document to a user means converting it into a usable form for your audience.
- **Web browsers** apply **CSS rules** to a document to affect how they are displayed.

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

## CSS rules - deep dive<a name="css-rules-deep"></a>

- #### Selectors

1.  You can make a rule match multiple elements by including multiple selectors separated by commas i.e. `h1, h2`
2.  Selectors can be chained together. i.e. `div p`. 
3.  An element may be matched by several selectors, therefore several rules may set a given property multiple times.
4.  CSS defines which one has precedence over the others and must be applied: this is called the `cascade algorithm`.

