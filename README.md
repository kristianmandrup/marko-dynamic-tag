marko-dynamic-tag
=================

[![Greenkeeper badge](https://badges.greenkeeper.io/kristianmandrup/marko-dynamic-tag.svg)](https://greenkeeper.io/)

Installation
============

```
npm install marko-dynamic-tag --save
```

Usage
=====

```xml
<dynamic-tag tag-name='h$data.lv' class='ui header'>hello world</dynamic-tag>
```

NOTE: If the value of the `tag-body` is left blank then it will default to `data.renderBody`.

```javascript
template.renderSync({
        lv: '1'
    });
```

Output:

```html
<h1 class='ui header'>hello world</h1>
```

```javascript
template.renderSync({
        renderBody: function(out) {
            out.write('My body content')
        }
    });
```

Output:

```html
<div>
    <h1>Hello World</h1>
    <p>
        My body content
    </p>
</div>
```
