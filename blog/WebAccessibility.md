# Web Accessibility
## What is it?
> Web Accessibility is making websites easily usuable for all people. It is mainly designed to help those with disablities. This encompasses a wide range of disabilites, including visual, auditory, physical, speech, cognitive, neurological, etc. Examples of tools that aid in accessibility include

## It's Importance
> The importance of web accessibiity is to be inclusive. One in six people have a disability. That's a chunk of people who aren't able to easily access the web as others can. It's also just the right thing to do. Besides ethical reasons, it also has business benefits. It shows the company's commitment to inclusivity, ergo, enchancing the brand reputation. Accessible websites can also yield better search results, increased audience reach, and demonstrate corporate social responsibility. Therfore, a well created and accessible website ensures accessibility for peopl with disabiliteies and enhances the overall experience for all visitors of the site.

## Examples of Applications
### Auditory
> For those with auditory disabilities, textual alternatives must be provided. Videos must be captioned along with an added transcript. Text-Simplification, the process of making text easier to understand, serves as another solutions, particulary in cases where deaf children weren't exposed to langauge, a condition known as language deprivation.

### Physical
> Physical accessibility is somwhat difficult to implement. However, there are still ways to make it easier for physical disabilities. Those with dexterity issues may not be able to use the mouse properly. To remedy this, the webpage should have other ways to interact with the website, such as the keyboard. Another solution would be to ensure the ease of use of the drag-and-drop functionalities, by appropriately spacing the positions or, ideally, eliminated altogether.

### Cognitive
> Cognitive disabilities covers a broad range, from intellectual and learning disabilities to mental illnesses. A solid framework to work around these disablities include:
> - Presenting content in multiple ways, such as text-to-speech or video
> - Easily understood content by using plain-langauge
> - Emphasizing important parts of the text
> - Reduce distractions, such as ads to avoid overstimulation
> - Maintain consistent webpage layout and navigation
> - Etc.

# ARIA Attributes
## What Does ARIA Mean
> ARIA stands for Accessible Rich Internet Applications. ARIA is a means to make webpages easily accessible for those with disabilties who use assistive technology, by providing additional information, or attributes, to HTML elements.

## How It Works
> There are three main components to ARIA: Roles, States, and Properties.

### Roles
> Roles are used to define the purpose or function of an element. It specifies what the element is supposed to do or represent; helping the user understanding how to interact with it.\
Here is how you would initialize it:
```html
<div role="role_name"><div>
```
> There are multple applications of roles such as:
> - Document Structure: provide descriptions for sections; Examples:
>   - img
>   - document 
>   - heading 
> - Landmark: created for easier navigation, identify each section of content; Examples:
>   - banner
>   - contentinfo
>   - main
> - Widget: doesn't define elements, but add meaning to UIs (User Interface); Examples:
>   - alert
>   - button
>   - grid
>   - menu

### States and Properties
> States and Properties desribe the current condition and information about an element. States represent dynamic characteristics that change over time based on user interaction or application behavior, while Properties, describe static characteristics that don't change. States convey real-time information and Properties provide context information. \
These attributes are organized in to four categories:
> - Drag and Drop Attrbutes: conveys information about drag-and-drop elements
>   - aria-dropeffect
>   - aria-grabbed
> - Live Region Attrbutes: indicates changes in content, assists screen reader or other Assertive Technologies to know what to read
>   - aria-live
>   - aria-atomic
>   - aria-busy
> - Relationship Attrbutes: add relationships between elements that otherwised can't be determined, helps Assertive Techonologies understand how differents parts of a web page connect
>   - aria-describedby
>   - aria-description
>   - aria-owns
> - Widget Attrbutes: helps Assertive Technologies understand the behavior and purpose of the Widget/UI
>   - aria-disabled
>   - aria-expanded
>   - aria-hidden
>
> Here is how you would initialize it:

**Aria-label gives the button a label to convey its purpose**

**Aria-disabled will determine if the button works or not, False means it works, True means it doesn't work**
```html
<button aria-label="Click me" aria-disabled="false">Click Me</button>
```


**Aria-live will check if the content has been updated for screen readers, so that the screen reader will also read it**
```html
<div aria-live="polite" id="liveRegion">
    <!--Content-->
</div>
```
```javascript
// Example of updating content within the live region
var liveRegion = document.getElementById("liveRegion");
liveRegion.innerHTML = "New content has been added!";
```

**Aria-expanded just indicates whether a collapsible element, like a menu is currently expanded or collapsed**

**Aria-controls indicates what elements on the page are affected by the element aria-contols applies to, usually with an id**<br>
**This means that the element with the menu id will be affected by aria-expanded**
```html
<button aria-expanded="false" aria-controls="menu">Show Menu</button>
<div id="menu" hidden>
  <!-- Menu content -->
</div>
```

# Resoruces

[Monsido](https://monsido.com/web-accessibility)

[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/What_is_accessibility)

[Accessibility.com](https://www.accessibility.com/blog/digital-accessibility-for-physical-disabilities)

[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes)

[LullaBot](https://www.lullabot.com/articles/what-heck-aria-beginners-guide-aria-accessibility)

[web.dev](https://web.dev/learn/accessibility/aria-html)