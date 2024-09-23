## Lists and Tables in HTML

#### 1. Lists in HTML

HTML provides various types of lists to organize and structure content. The two main types are **unordered lists** and **ordered lists**, but HTML also supports **definition lists** for term-definition pairs.

##### a. Unordered List (`<ul>`)

Unordered lists display items with bullet points by default. They are best for non-sequential items where the order doesn’t matter.

**Basic Syntax:**

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

- **`<ul>`**: Defines an unordered list.
- **`<li>`**: Defines a list item.

**Example**:

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

Output:
- HTML
- CSS
- JavaScript

##### b. Ordered List (`<ol>`)

Ordered lists display items with numbers or letters to indicate the sequence. They are used when the order of the items is important.

**Basic Syntax:**

```html
<ol>
  <li>Step 1</li>
  <li>Step 2</li>
  <li>Step 3</li>
</ol>
```

- **`<ol>`**: Defines an ordered list.
- **`<li>`**: Defines a list item.

**Example**:

```html
<ol>
  <li>Preheat the oven</li>
  <li>Mix the ingredients</li>
  <li>Bake for 20 minutes</li>
</ol>
```

Output:
1. Preheat the oven
2. Mix the ingredients
3. Bake for 20 minutes

**Changing the Type of Markers:**

- You can change the marker style (numbers, letters, or Roman numerals) using the `type` attribute in `<ol>`.
  - `1`: Default (numbers)
  - `A`: Uppercase letters
  - `a`: Lowercase letters
  - `I`: Uppercase Roman numerals
  - `i`: Lowercase Roman numerals

**Example:**

```html
<ol type="A">
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
</ol>
```

Output:
A. First
B. Second
C. Third

##### c. Nested Lists

You can nest lists within other lists by placing a `<ul>` or `<ol>` inside a `<li>` element.

**Example:**

```html
<ul>
  <li>Fruits
    <ul>
      <li>Apples</li>
      <li>Bananas</li>
      <li>Oranges</li>
    </ul>
  </li>
  <li>Vegetables</li>
</ul>
```

Output:
- Fruits
  - Apples
  - Bananas
  - Oranges
- Vegetables

##### d. Definition List (`<dl>`)

Definition lists are used for terms and their descriptions.

**Basic Syntax:**

```html
<dl>
  <dt>Term 1</dt>
  <dd>Description for Term 1</dd>
  <dt>Term 2</dt>
  <dd>Description for Term 2</dd>
</dl>
```

- **`<dl>`**: Defines a definition list.
- **`<dt>`**: Defines a term.
- **`<dd>`**: Defines the description or definition of the term.

**Example:**

```html
<dl>
  <dt>HTML</dt>
  <dd>A markup language for creating web pages</dd>
  <dt>CSS</dt>
  <dd>A style sheet language for designing web pages</dd>
</dl>
```

Output:
- HTML
  A markup language for creating web pages
- CSS
  A style sheet language for designing web pages

---

### 2. Tables in HTML

Tables in HTML allow you to display data in rows and columns, which is useful for structuring data like schedules, price lists, or comparison charts.

##### a. Basic Table Structure

A basic HTML table is made up of the following elements:

- **`<table>`**: Wraps the entire table.
- **`<tr>`** (Table Row): Defines a row in the table.
- **`<td>`** (Table Data): Defines a cell in the row.
- **`<th>`** (Table Header): Defines a header cell (typically bold and centered).

**Basic Syntax:**

```html
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <tr>
    <td>Row 1, Cell 1</td>
    <td>Row 1, Cell 2</td>
    <td>Row 1, Cell 3</td>
  </tr>
  <tr>
    <td>Row 2, Cell 1</td>
    <td>Row 2, Cell 2</td>
    <td>Row 2, Cell 3</td>
  </tr>
</table>
```

**Example:**

```html
<table border="1">
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>City</th>
  </tr>
  <tr>
    <td>John</td>
    <td>25</td>
    <td>New York</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>30</td>
    <td>London</td>
  </tr>
</table>
```

Output:

| Name   | Age | City |
|--------|-----|------|
| Aditya | 20  | BGP  |
| Pritam | 20  | BGP  |

##### b. Table Attributes

1. **`border`**: Adds a border around the table and cells.

   **Example**:

   ```html
   <table border="1">
     <!-- Table content -->
   </table>
   ```

2. **`cellpadding`**: Adds padding inside the cells.

   **Example**:

   ```html
   <table border="1" cellpadding="10">
     <!-- Table content -->
   </table>
   ```

3. **`cellspacing`**: Adds spacing between cells.

   **Example**:

   ```html
   <table border="1" cellspacing="5">
     <!-- Table content -->
   </table>
   ```

4. **`width`** and **`height`**: Define the dimensions of the table or cells.

   **Example**:

   ```html
   <table border="1" width="500">
     <!-- Table content -->
   </table>
   ```

##### c. Spanning Rows and Columns

You can merge cells across rows and columns using the `rowspan` and `colspan` attributes.

1. **`colspan`**: Merges multiple columns into one cell.

   **Example**:

   ```html
   <table border="1">
     <tr>
       <th colspan="2">Header 1 & 2</th>
     </tr>
     <tr>
       <td>Cell 1</td>
       <td>Cell 2</td>
     </tr>
   </table>
   ```

   Output:

   | Header 1 & 2 |
   |--------------|
   | Cell 1       | Cell 2 |

2. **`rowspan`**: Merges multiple rows into one cell.

   **Example**:

   ```html
   <table border="1">
     <tr>
       <td rowspan="2">Merged Row</td>
       <td>Cell 2</td>
     </tr>
     <tr>
       <td>Cell 3</td>
     </tr>
   </table>
   ```

   Output:

   | Merged Row | Cell 2 |
   |------------|--------|
   |            | Cell 3 |

##### d. Advanced Table Features

1. **`<thead>`, `<tbody>`, `<tfoot>`**: These tags structure the table into a header, body, and footer.

   **Example**:

   ```html
   <table border="1">
     <thead>
       <tr>
         <th>Header 1</th>
         <th>Header 2</th>
       </tr>
     </thead>
     <tbody>
       <tr>
         <td>Row 1, Cell 1</td>
         <td>Row 1, Cell 2</td>
       </tr>
       <tr>
         <td>Row 2, Cell 1</td>
         <td>Row 2, Cell 2</td>
       </tr>
     </tbody>
     <tfoot>
       <tr>
         <td colspan="2">Footer</td>
       </tr>
     </tfoot>
   </table>
   ```

   This provides a structured way to handle table data, making it more semantic and easier to style with CSS.

##### e. Best Practices for Tables

1. **Use Tables for Tabular Data**: Avoid using tables for layout purposes. Tables should be used only for presenting data in a tabular form.
2. **Keep Tables Accessible**: Use proper `<th>` and `<td>` tags to distinguish

---

Next -> [Forms and Input Field](FormsInput.md)

Back to Contents page [click here](../Contents.md)
