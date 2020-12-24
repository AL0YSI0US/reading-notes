HTML / Markup / Semantics / Wireframe / Personas / Meta / Content / Element / Tag / Attribute / Structure vs Presentation 

# Structure Web Pages with HTML

## HTML & CSS

:electron: [HTML MASTER CHEAT](https://overapi.com/html)

:electron: [CSS MASTER CHEAT](https://overapi.com/css)

:mortar_board: [HTML](https://html.spec.whatwg.org/multipage/)

:mortar_board: [Beginner’s guide to CSS](https://friendlybit.com/css/beginners-guide-to-css-and-standards/)

[HTML PDF Cheat Sheet](https://overapi.com/static/cs/html-cheat-sheet.pdf)

> HTML Example

|**Term**|**Context**|
| ----------- | ----------- |
| HTML | **Hypertext Markup Language (HTML)** is the standard markup language for documents designed to be displayed in a web browser. It can be assisted by technologies such as *Cascading Style Sheets (CSS)* and scripting languages such as *JavaScript.* Web browsers receive HTML documents from a web server or from local storage and render the documents into multimedia web pages. HTML describes the structure of a web page semantically and originally included cues for the appearance of the document. HTML elements are the building blocks of HTML pages.  With HTML constructs, images and other objects such as interactive forms may be embedded into the rendered page. HTML provides a means to create structured documents by denoting structural semantics for text such as headings, paragraphs, lists, links, quotes and other items. HTML elements are delineated by tags, written using angle brackets. Tags directly introduce content into the page. Other tags surround and provide information about document text and may include other tags as sub-elements. Browsers do not display the HTML tags, but use them to interpret the content of the page. HTML can embed programs written in a scripting language such as *JavaScript*, which affects the behavior and content of web pages. Inclusion of *CSS* defines the look and layout of content. The World Wide Web Consortium (W3C), former maintainer of the HTML and current maintainer of the *CSS* standards, has encouraged the use of *CSS* over explicit presentational HTML since 1997.|
| Markup | When creating a web page, you add ***tags*** (known as **Markup**) to the contents of the page. These tags provide extra meaning and allow browsers to show users the appropriate structure for the pages. |
| Structural Markup|the elements you can use to describe both headings and paragraphs |
| Semantic Markup| which provides extra information; such as where emphasis is placed in a sentence, that something you have written is a quotation (and who said it), the meaning of acronyms and so on |
| WireFrame  | is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require. Graphics applications examples: illustrator or inDesign or online tools [gomockingbird](gomockingbird.com) or [lovelycharts](lovelycharts.com) |
| Personas | The purpose of personas is to create reliable and realistic representations of your key audience segments for reference. These representations should be based on qualitative and some quantitative user research and web analytics. Personas are only as good as the research behind them. Effective personas: Represent a major user group for your website, Express and focus on the major needs and expectations of the most important user groups, Give a clear picture of the user's expectations and how they're likely to use the site, Aid in uncovering universal features and functionality, Describe real people with backgrounds, goals, and values [Read More about Personas](https://www.usability.gov/how-to-and-tools/methods/personas.html) |
| Meta  | The **Meta** element lives inside the ***head*** element and contains information about the web page. It is not visible to users but fulfuls a number of pyrposes such as telling search engines wbout your page, who created it, and whether or not it is time sensitive. (If the page is time sensitive, it can be set to expire)|
| Content | Content is the stuff people see in the browser. We use HTML to organize that content into familiar element type like headings, lists, and paragraphs. ***See image below table***|
| Element | The HTML code is made up of characters that live inside angled brackets. These are called HTML **elements** Elements are usually made up of two ***tags***: an opening tag and a closing tag. (The closing tag has am extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags. ***the term "tag" and "element" are often used interchangebly*** |
| Tag  | **Tags** act like containers. They tell you something about the information that lies between their opening and closing tags. ***the term "tag" and "element" are often used interchangebly***|
| Attribute  | **Attributes** tell us more about elements. Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a ***name*** and a ***value***, seperated by an equals sign.|
| Structure   | HTML uses elements to describe the **structure** of the page. **html** / **body** / **h1** / **p** / **h2** / **p** / **h2** / **p** / **/body** / **/html** |
| Presentation | **Presentation** is the style you give the content. In most cases presentation is about the way a document looks, but it can also affect how a document sounds ***not everybody uses a graphical web browser.*** Adding CSS to existing applications creates a richer visual experience |
| Render | **Rendering** or ***image synthesis*** is the process of generating a photorealistic or non-photorealistic image from a 2D or 3D model by means of a computer program. The resulting image is referred to as the render. Multiple models can be defined in a scene file containing objects in a strictly defined language or data structure. The scene file contains geometry, viewpoint, texture, lighting, and shading information describing the virtual scene. The data contained in the scene file is then passed to a rendering program to be processed and output to a digital image or raster graphics image file. The term "rendering" is analogous to the concept of an artist's impression of a scene. The term "rendering" is also used to describe the process of calculating effects in a video editing program to produce the final video output. |

**Content example:** The image below represents a document. The words and pictures are content. The red labels indicate the element type of each bit of content. In HTML you use HTML tags to define chunks of content like that;

![content example](https://qph.fs.quoracdn.net/main-qimg-f3435b90460e56ec9d26859394f3ba43.webp)

## index.html - is the standard

Used in conjunction with **CSS** to provide visual formatting. *Allows you to create structure of paragraphs and headings.*

## PROCESS
1. **HTML** (repository/git site/index.html)
2. **CSS** to make it look good
3. **JavaScript** makes the site functional.
- *tags are used to establish structural components*

**Read**

-Duckett: HTML & CSS, ***Chapter 18. Process & Design***

**Skim**

- Duckett:***HTML & CSS, Chapter 1: Structure***

**Read**
-Duckett: HTML & CSS, ***Chapter 17. HTML5 Layout*** Note how these elements are common to the vast majority of web pages

-Duckett: HTML & CSS, ***Chapter 8 . Extra Markup***

[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) [Forward ==>](style_web_pages_with_css.md)