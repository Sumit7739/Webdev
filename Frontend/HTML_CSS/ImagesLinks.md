### Adding Images in HTML

In HTML, images are added using the `<img>` tag. This is a self-closing tag, meaning it doesn’t require a separate closing tag. Images enhance the content of a webpage, providing visual context or improving aesthetics.

#### Basic Syntax

The basic syntax for embedding an image in an HTML document is:

```html
<img src="imageURL" alt="alternative text" />
```

#### Attributes of the `<img>` Tag

1. **`src` (Source):**
   - This attribute is mandatory.
   - It specifies the path to the image file. The path can be:
     - **Absolute URL**: Links to images hosted online (e.g., `https://example.com/image.jpg`)
     - **Relative URL**: Links to images stored locally on the same website (e.g., `images/photo.jpg`).

   **Example**:
   ```html
   <img src="https://example.com/photo.jpg" alt="Description of photo" />
   ```

2. **`alt` (Alternative Text):**
   - This attribute is optional but highly recommended for accessibility and SEO.
   - It provides a description of the image that will be shown if the image fails to load. It also assists screen readers in explaining images to visually impaired users.

   **Example**:
   ```html
   <img src="images/photo.jpg" alt="A scenic view of mountains during sunset" />
   ```

3. **`width` and `height`:**
   - These attributes control the size of the image.
   - You can define the dimensions in pixels (`px`), percentages (`%`), or leave it unset to maintain the original image dimensions.

   **Example**:
   ```html
   <img src="images/photo.jpg" alt="A mountain view" width="500" height="300" />
   ```

4. **`title`:**
   - This optional attribute provides additional information about the image.
   - It displays a tooltip when the user hovers over the image.

   **Example**:
   ```html
   <img src="images/photo.jpg" alt="A mountain view" title="Mountain view during sunset" />
   ```

#### Image File Types

Common image formats supported by browsers include:

- **JPEG/JPG**: Suitable for photographs and complex images. It provides good compression while maintaining quality.
- **PNG**: Ideal for images requiring transparency or high-quality graphics.
- **GIF**: Best for small, simple animations or images with fewer colors.
- **SVG**: A vector format for scalable images, ideal for logos and icons.
- **WebP**: A modern image format providing superior compression.

#### Image Paths: Absolute vs. Relative URLs

1. **Absolute URL**: The full web address of the image, including the protocol (`http` or `https`), domain, and file path.

   **Example**:
   ```html
   <img src="https://example.com/images/photo.jpg" alt="Example photo" />
   ```

2. **Relative URL**: A path relative to the current HTML document. It assumes the image is stored within your website’s directory.

   **Example**:
   ```html
   <img src="images/photo.jpg" alt="Example photo" />
   ```

   Relative paths can be:
   - **Same folder**: If the image is in the same directory as the HTML file:
     ```html
     <img src="photo.jpg" alt="Example photo" />
     ```

   - **Subfolder**: If the image is in a subfolder relative to the HTML file:
     ```html
     <img src="images/photo.jpg" alt="Example photo" />
     ```

   - **Parent folder**: If the image is stored in a parent directory:
     ```html
     <img src="../photo.jpg" alt="Example photo" />
     ```

#### Responsive Images

In modern web development, making images responsive ensures they adapt to different screen sizes and devices. You can use CSS to handle responsive design:

```css
img {
    max-width: 100%;
    height: auto;
}
```

This ensures that the image scales according to the screen size while maintaining its aspect ratio.

Alternatively, HTML5 introduced the `<picture>` element and the `srcset` attribute for responsive image handling:

```html
<picture>
  <source media="(min-width: 650px)" srcset="large-image.jpg">
  <source media="(min-width: 465px)" srcset="medium-image.jpg">
  <img src="small-image.jpg" alt="Responsive example image">
</picture>
```

In the above example, different images are loaded based on the screen size.

#### Example of an Image with Multiple Attributes:

```html
<img src="images/mountain.jpg" alt="Mountain range at sunset" width="600" height="400" title="Mountain View" />
```

In this example:
- The image source is set to a local file path (`images/mountain.jpg`).
- The `alt` attribute provides a description in case the image doesn't load.
- The `width` and `height` attributes control the size of the image.
- The `title` attribute displays additional information when the user hovers over the image.

#### Best Practices

1. **Use Alt Text**: Always provide meaningful `alt` text for accessibility and SEO benefits.
2. **Optimize Images**: Compress images to reduce their file size and improve page load times.
3. **Use Responsive Design**: Make sure images scale appropriately on different devices by using CSS or HTML attributes like `srcset`.
4. **Use Appropriate Formats**: Select image formats based on the use case (e.g., `JPG` for photos, `PNG` for images with transparency).

#### Conclusion

Embedding images in HTML is straightforward using the `<img>` tag. By properly using attributes like `src`, `alt`, and `title`, you can ensure your images are accessible, responsive, and optimized for different screen sizes. Always keep in mind the type of image and the context in which it will be displayed for the best user experience.

---

### Links in HTML

Links are one of the core components of the web, allowing users to navigate between different pages, documents, or sections of a website. In HTML, links are created using the `<a>` tag (which stands for "anchor").

#### Basic Syntax

The basic syntax for adding a link in HTML is:

```html
<a href="URL">Link Text</a>
```

- **`href`**: This is the "Hypertext Reference" attribute, which holds the destination URL.
- **Link Text**: The clickable text that users will see.

#### Types of Links

1. **External Links**:
   These links point to resources outside of your website, such as another webpage, social media, or any other external resource.

   **Example**:
   ```html
   <a href="https://www.example.com">Visit Example Website</a>
   ```

2. **Internal Links**:
   These links point to other pages within the same website. You use relative URLs to navigate between internal pages.

   **Example**:
   ```html
   <a href="about.html">About Us</a>
   ```

   If your webpage structure has folders, you’ll need to adjust the path based on file locations:

   - **Same folder**:
     ```html
     <a href="services.html">Our Services</a>
     ```

   - **Different folder**:
     ```html
     <a href="blog/post1.html">Read our latest post</a>
     ```

   - **Parent folder**:
     ```html
     <a href="../index.html">Home</a>
     ```

3. **Anchor Links (Internal Page Sections)**:
   Anchor links navigate to a specific section within the same page or another page. You must give an element (usually a heading or section) an `id` attribute, and link to it using the `#` symbol followed by the `id` value.

   **Example**:
   ```html
   <a href="#section1">Go to Section 1</a>

   <!-- Later in the page -->
   <h2 id="section1">Section 1</h2>
   ```

4. **Email Links**:
   You can use the `mailto:` protocol in the `href` attribute to create a link that opens the user's default email client and starts composing an email.

   **Example**:
   ```html
   <a href="mailto:contact@example.com">Email Us</a>
   ```

5. **Telephone Links**:
   Similar to email links, you can use the `tel:` protocol to link phone numbers. This is useful for mobile users who can click the link to initiate a call.

   **Example**:
   ```html
   <a href="tel:+1234567890">Call Us</a>
   ```

#### Attributes of the `<a>` Tag

1. **`href` (Hypertext Reference)**:
   - This attribute specifies the URL or link destination.
   - The URL can be absolute (full path) or relative (relative path within your website).

   **Example**:
   ```html
   <a href="https://www.example.com">Visit Example</a>
   ```

2. **`target`**:
   - This attribute specifies where to open the linked document.
   - Common values:
     - **`_self`**: (default) Opens the link in the same window/tab.
     - **`_blank`**: Opens the link in a new tab or window.
     - **`_parent`**: Opens the link in the parent frame.
     - **`_top`**: Opens the link in the full body of the window, breaking out of frames.

   **Example**:
   ```html
   <a href="https://www.example.com" target="_blank">Open in New Tab</a>
   ```

3. **`title`**:
   - This attribute provides additional information about the link when users hover over it. It serves as a tooltip.

   **Example**:
   ```html
   <a href="https://www.example.com" title="Click to visit Example">Visit Example</a>
   ```

4. **`download`**:
   - If you want the link to prompt a file download rather than navigating to a webpage, use the `download` attribute.

   **Example**:
   ```html
   <a href="files/document.pdf" download>Download PDF</a>
   ```

#### Linking to Different File Types

You can link to various file types such as PDFs, images, videos, and more. When a user clicks the link, their browser will handle the file based on its type:

- **PDF**:
  ```html
  <a href="files/ebook.pdf">Download Ebook</a>
  ```

- **Image**:
  ```html
  <a href="images/photo.jpg">View Photo</a>
  ```

- **Video**:
  ```html
  <a href="videos/demo.mp4">Watch Video</a>
  ```

#### Opening Links in New Tabs

To open a link in a new browser tab, set the `target` attribute to `_blank`:

```html
<a href="https://www.example.com" target="_blank">Visit Example in New Tab</a>
```

This is useful when linking to external websites, as it keeps the user on your site while giving them the option to view other content.

#### Linking Images

You can also make an image a clickable link by wrapping the `<img>` tag within an `<a>` tag:

```html
<a href="https://www.example.com">
    <img src="images/photo.jpg" alt="Example Image" />
</a>
```

In this case, clicking on the image will navigate the user to the destination specified in the `href`.

#### Example of a Complex Link:

```html
<a href="https://www.example.com" target="_blank" title="Visit our homepage" download>
    Visit Example Website
</a>
```

In this example:
- The link points to an external URL (`https://www.example.com`).
- The `target="_blank"` ensures it opens in a new tab.
- The `title` attribute provides additional information when hovered over.
- The `download` attribute will initiate a file download instead of loading the page, assuming the link points to a downloadable file.

#### Best Practices for Adding Links

1. **Use Meaningful Link Text**: Avoid generic phrases like "click here." Use descriptive text that gives users context about where the link leads.
   - **Bad Example**: `<a href="example.com">Click here</a>`
   - **Good Example**: `<a href="example.com">Learn more about our services</a>`

2. **Open External Links in New Tabs**: For links pointing outside your website, consider using `target="_blank"` so users remain on your site.

3. **Use Anchor Links for Better Navigation**: Especially in longer pages, anchor links improve usability by letting users jump to specific sections.

4. **Check for Broken Links**: Regularly check for and fix any broken links (links leading to dead or incorrect pages) on your site.

5. **Ensure Accessibility**: Include meaningful `title` attributes for users who rely on screen readers and ensure link color or underline contrasts well with the background.

#### Conclusion

Links are an essential part of web navigation, allowing users to move between pages, sections, and external resources. By properly using attributes like `href`, `target`, and `title`, you can create meaningful and functional links that enhance the user experience.

---

Next -> [List and Tables](ListTable.md)

[go back](../Contents.md)