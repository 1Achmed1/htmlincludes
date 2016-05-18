# htmlincludes
HTMLIncludes makes it easier to load common and/or repetitive documents between pages, like, for instance, a page footer.

## Usage
Here's a footer template file that is identical between pages:

`footer.html`:
```html
<div class="card footer" data-hover="false" id="footer" data-role="footer">
  <span id="footerspan">HTMLIncludes is developed by Andrew Ward and the open source community, whomever that may be. Code hosted and open-sourced on GitHub.</span>
</div>
```

Let's import that using HTMLIncludes. Firstly, put a block element (like a `div`) where you'd like the template to be inserted:
`index.html`
```html
<div class="page-footer"></div>
```
Now you'll need some js to make the magic happen using the htmlinclude function:

`index.html`
```html
<script type="text/javascript">htmlInclude(".page-footer", "templates/footer.html");</script>
```
Here's the function:
```javascript
htmlinclude([element], [file]);
```
The `element` can be a class, id, or data attribute. The `file` must be a path to the file, and the file name ending in `.html` (see code example). Templates need to be compliant with the [jQuery `load` function](http://api.jquery.com/load/).

HTMLImports also supports using `data-include` on block elements that you'd like to import into, but I found that while Vivaldi worked with this method, Chrome and Firefox didn't.

## Download HTMLIncludes
You can use either online always-updated code or download the code for production.

To use it from the online source, add this script in your project:
`//raw.githubusercontent.com/1Achmed1/htmlincludes/master/htmlincludes.js` <br/>
\>\> As a side note, you can remove the `http[x]:` thing from URLs (as I have above), as it will automatically use the same HTTP protocol this way.

For production releases, download the a source release: <br/>
https://github.com/1Achmed1/htmlincludes/releases
