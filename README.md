## Strapdown.js

[Strapdown.js](http://strapdownjs.com/) makes it embarrassingly simple to create elegant Markdown documents. No server-side compilation required. 

For more, please see:

- https://strapdown-js.balloon.net.eu.org/5/ - Bootstrap 5 themes
- https://strapdown-js.balloon.net.eu.org/4/ - Bootstrap 4 themes
- https://strapdown-js.balloon.net.eu.org/3/ - Bootstrap 3 themes
- https://strapdown-js.balloon.net.eu.org/2/ - Bootstrap 2 themes

Tip: The original Strapdown.js is a **Bootstrap 2 themes**

___

## Original Project

Oops! This is a forked project. The original README.md can be found here:

[README.original.md](https://github.com/fu-sen/strapdown/blob/main/README.original.md)

See original project if needed:

<https://github.com/arturadib/strapdown>

___

## Version and Branch

I split the branch according to the version of Bootstrap themes

|Themes     |Version|Source branch|
|-----------|:-----:|:-----------:|
|Bootstrap 5| v0.5  | main        |
|Bootstrap 4| v0.4  | bootstrap4  |
|Bootstrap 3| v0.3  | bootstrap3  |
|Bootstrap 2| v0.2  | bootstrap2  |

The main changes from the original are:

- Add theme (v0.2 only)
- Add CSS (v0.4 and v0.5)
- Add set navbar color (v0.3, v0.4 and v0.5)
- Change padding-top `60px` to `90px` (Consideration of Lux theme, v0.4 and v0.5)
- Change `nav` class in `strapdown.js`
- Change `viewport` of `strapdown.js`
- Updated [Marked](https://github.com/markedjs/marked), [Google Code Prettify](https://github.com/googlearchive/code-prettify) and [Bootswatch themes](https://bootswatch.com/)

Bootstrap 3 is effectively this fork. Great job, @bhhaskin !:

- <https://github.com/arturadib/strapdown/pull/51>
- <https://github.com/OCG-labs/strapdown/tree/dev>

___

## Add and change CSS (v0.4 and v0.5)

Bootstrap 4 has major changes to the CSS specification. I needed to add strapdown.css for this.

There was a large space above the text. This had to be changed, especially as a consideration for the Lux theme.

The following is considered in Strapdown.js v0.4 and v0.5 (To have the same design as v0.2 and v0.3). This is necessary because it inherits the style of Google Code Prettify:

- `<pre><code>`
- `<code>`

The following is not taken into consideration. You can apply Custom CSS if necessary.

- `<blockquote>` (Changed it to use `class="blockquote"` )

___

## Set navbar color (v0.3, v0.4 and v0.5)

You can change the color of the navbar after Bootstrap3. I made it possible to specify this with `navbar`.

### v0.4 and v0.5

The types of navbar color are `primary`, `dark` and `light`. Default is `primary`:
```
<textarea theme="yeti" navbar="light">
```

### v0.3:

If navbar has a value, it works inverse:

```
<textarea theme="yeti" navbar="inverse">
```

___

## CDN

Now we can apply the CDN using [jsDelivr](https://www.jsdelivr.com/). I have prepared different projects for the CDN:

- <https://github.com/fu-sen/strapdown.js>

___

## Contributor guide

The build in this project inherits the original:

> You will need Node.js (>0.6.x) and CoffeeScript to generate the bundles. To bundle/compile the assets, issue in the project directory:
> 
> ```
> $ npm install
> $ coffee bundle <version_number>
> ```

___

## Consideration

- Remove Google Code Prettify  
It's [an archive project](https://github.com/googlearchive/code-prettify). Deletion prevents unintended `<code>` conversion. You can also select and use [highlight.js](https://github.com/highlightjs/highlight.js) etc.  
I don't want to add extra features to Strapdown.js to reduce the load in many environments. Instead, I had to think about removing the feature.

___

## License

[MiT License](https://github.com/fu-sen/strapdown/blob/main/LICENSE)

日本語: <https://mit.balloon.net.eu.org/>

Excludes `vendor/` and themes. These are licensed separately.
