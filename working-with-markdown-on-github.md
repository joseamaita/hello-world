# Working with Markdown on GitHub

## Introduction

Markdown is a lightweight and easy-to-use syntax for styling all forms of writing on the GitHub platform.

Basically, [Markdown](http://daringfireball.net/projects/markdown/) is a way to style text on the web. You control the display of the document; formatting words as bold or italic, adding images, and creating lists are just a few of the things we can do with Markdown. Mostly, Markdown is just regular text with a few non-alphabetic characters thrown in, like `#` or `*`.

## Examples

### Text

```
It's very easy to make some words **bold** and other words *italic* with Markdown. You can even 
[link to Google!](http://google.com)
```

It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)

### Lists

```
Ordered lists:

1. One
1. Two
1. Three

Unordered lists:

* Start a line with a star
* Profit!

Alternatively,

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  - Like this
  - And this
```

Ordered lists:

1. One
1. Two
1. Three

Unordered lists:

* Start a line with a star
* Profit!

Alternatively,

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  - Like this
  - And this

### Images

```
If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
```

If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

### Headers & Quotes

```
# Structured documents

Sometimes it's useful to have different levels of headings to structure your documents. Start lines with 
a `#` to create headings. Multiple `##` in a row denote smaller heading sizes.

### This is a third-tier heading

You can use one `#` all the way up to `######` six for different heading sizes.

If you'd like to quote someone, use the > character before the line:

> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway
```

# Structured documents

Sometimes it's useful to have different levels of headings to structure your documents. Start lines with a `#` to create headings. Multiple `##` in a row denote smaller heading sizes.

### This is a third-tier heading

You can use one `#` all the way up to `######` six for different heading sizes.

If you'd like to quote someone, use the > character before the line:

> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway

### Code

````````````
There are many different ways to style code with GitHub's markdown. If you have inline code blocks, wrap 
them in backticks: `var example = true`.  If you've got a longer block of code, you can indent with 
four spaces:

    if (isAwesome){
      return true
    }

GitHub also supports something called code fencing, which allows for multiple lines without indentation:

```
if (isAwesome){
  return true
}
```

And if you'd like to use syntax highlighting, include the language:

```javascript
if (isAwesome){
  return true
}
```
``````

Test paragraph
