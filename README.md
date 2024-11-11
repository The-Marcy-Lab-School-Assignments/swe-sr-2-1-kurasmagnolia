# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:

- Examples of semantic and non-semantic tags
- The differences between semantic and non-semantic tags
- The benefits of using semantic tags (when possible)

### Response 1

Semantic and non-semantic elements both help structure content on web pages, but they differ in terms of meaning and purpose.

Some examples of semantic elements are:

- `<header>`: Represents the header section of a document.
- `<footer>`: Represents the footer section of a document.
- `<main>`: Represents the main content of a document.

Some examples of non-semantic elements are:

- `<div>`: A generic container for content.
- `<span>`: A generic inline container for content.
- `<br>`: Inserts a line break in between content.

The differences between semantic and non-semantic elements is that semantic elements provide meaning to what they are in a human and machine-readable way. They provide context and meaning to both the browser and developers, as non-semantic elements don't provide any information about them, and is used for layout and styling without providing context.

Benefits of Using Semantic Elements:

- **Improved Accessibility**: Semantic elements help screen readers and other assistive technologies navigate and interpret the content.
- **Enhanced SEO**: Search engines can better understand and rank the content when semantic tags are used.
- **Better Maintainability**: Semantic elements make code more concise, readable, and easier to maintain, as they clearly define the structure and purpose of the content.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

Some ways to make your website more accessible include:

1. Use Alt Attributes for Images:

- Add descriptive alt text to <img> tags. This helps users who rely on screen readers to understand the content of images and provides a fallback if images fail to load.

2. Ensure Sufficient Color Contrast:

- Use colors with high contrast to improve readability, especially for users with visual impairments or color blindness.

3. Keyboard Navigation:

- Ensure your website is fully navigable using a keyboard alone. This benefits users who cannot use a mouse due to mobility impairments.

4. Provide Descriptive Link Text:

- Use meaningful text for links (e.g., "Learn more about our services" instead of "Click here") to give users context about where the link leads.

5. Add Captions and Transcripts for Multimedia:

- Provide captions for videos and transcripts for audio content to assist users who are deaf or hard of hearing.

**Why Accessibility is Important:**

1. Inclusivity:

- Ensures that your website is usable by all individuals, including those with disabilities.

2. Legal Compliance:

- Many countries have laws (e.g., ADA in the U.S., WCAG globally) requiring websites to meet accessibility standards.

3. Improved User Experience:

- Accessibility features often benefit all users, such as better readability or easier navigation.

4. Wider Audience Reach:

- By accommodating users with disabilities, you expand your potential audience, improving engagement and retention.

5. Ethical Responsibility:

- It’s part of a developer’s duty to create an equitable web experience for everyone.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;">hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

Using inline CSS styles can be useful in certain situations. For example, they are helpful for quick testing or applying styles to a specific element without the need to create or edit an external stylesheet. Inline styles can also be a convenient solution for one-off customizations when styling a unique element that won’t be reused elsewhere.

However, for most cases, writing styles in a separate CSS file is strongly recommended. This approach promotes the separation of concerns by keeping structure (HTML) and presentation (CSS) distinct. It makes the code easier to read and maintain, especially in larger projects. Additionally, styles defined in an external CSS file ensure consistency across multiple pages, reducing the likelihood of style discrepancies.

Another key advantage of external stylesheets is performance improvement. CSS files can be cached by browsers, meaning they don’t need to be reloaded on each page visit, leading to faster load times. Furthermore, using a separate CSS file enhances scalability, making it easier to manage styles as the project grows, while keeping the HTML clean and focused on content rather than presentation.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

- An explanation of the concept of "classes" and "ids" with an analogy.
- An example of the usage using an HTML code block and a CSS code block.
- An explanation of the syntax using the terms: **attribute**, **selector**

### Response 4

Class and id attributes are both used to apply styles to HTML elements, but they behave differently in important ways. The `class` attribute is used to style multiple elements that share the same styling, which is ideal for applying a consistent style to a group of elements. On the other hand, the `id` attribute is used to style a single, unique element on a page. IDs must be unique within a document, meaning they cannot be applied to more than one element.

Think of both attributes as a friend group and a specific friend. The `class` attribute is like a friend group who all go to the same movie together. They're all wearing matching t-shirts, so you can easily identify them as part of the same group. An `id` is like a specific friend in that group who is wearing their own unique shirt with their name on it, identifying that one specific individual.

```html
<h1 id="main-heading">This is the main heading.</h1>

<p class="highlight">This is a paragraph.</p>
<span class="highlight">This is a span.</span>
```

```css
#main-heading {
  font-size: 50px;
  color: red;
}

.highlight {
  color: blue;
}
```

In the first code block above, the `id="main-heading"` is applied to a heading element, while the `class="highlight"` is applied to both a paragraph and a span element. The second code block shows how these attributes are targeted using CSS selectors. The `#main-heading` selector applies styles to the specific `h1` element with that unique `id`, changing its font size to **50px**, or **50 pixels**, and its color to red. The `.highlight` selector applies styles to all elements with the `highlight` class, changing the text color of both the paragraph and span to blue.

Using `class` and `id` helps developers efficiently manage styles. Classes allow for reusability and consistency across multiple elements, making it easier to apply and update styles in bulk. IDs, on the other hand, provide a way to target specific elements for unique styling. This separation makes code more organized, maintainable, and scalable, especially as projects grow.

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however, is that the best practice?

When deciding how to structure your website, it's important to understand the unique roles of HTML, CSS, and JavaScript. HTML is responsible for the structure and content of the webpage, such as paragraphs, headings, and links. CSS handles the layout and styling of the webpage, such as fonts, positioning, and colors. Lastly, JavaScript adds interactivity and handles dynamic behavior, as in animations, form validation, or content that changes in response to user actions across the website.

You would use HTML and CSS for static content, which is content that doesn't change frequently, and for styling that content. JavaScript and the DOM API should be used when working with content that needs to be updated in real time, like interactive elements or user-driven updates (e.g., adding items to a shopping cart).

This is the best practice because it makes debugging and maintenance easier. The separation of concerns—keeping structure, styling, and interactivity separate—keeps the codebase more readable, organized, and maintainable.
