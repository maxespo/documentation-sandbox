# Printing to PDF tips

In this article:

 * [PDF editor scheme](#pdf-editor-scheme)
 * [PDF syntax](#pdf-code-syntax)
 * [Text](#text)
 * [Logo/Image](#logo-image)
 * [Table](#table)
 * [link](#link)

## PDF editor scheme

![pdf-editor-scheme]()

## PDF code syntax

If you open a template code view (`</>`) you will see that your PDF document data is markupped with the tags well known in HTML.

**Note!**
Due to a security policy some of HTML tags, attributes or styles may not be supported or allowed by editor. So it will truncate them automatically.

![image with the code view]()

## Text

* `<b>some text</b>` - bold text style
* `<u>some text</u>` - underlined text style
* `<i>some text</i>` - italic text style
* `<s>some text</s>` - crossline the text
* `<br>` - insert single line breaks in a text
* `<span>some text</span>` - element which is used to color a part of a text: `<span style="color: rgb(255, 255, 255);>`. Also in PDF constructor the <span> tag is very helpful for setting the single string parameters or putting a single line of an empty string.
* `<p>some text</p>` - defines a paragraph.
* `<div>some text</div>` - used as a container for HTML elements.

## Logo/Image

#### How to add image

You can add a logo of your company or other images to your PDF document with the next ways:
* Click the picture button in the tools panel -> Browse -> select a file.

Code view: `<img style="width: 350px;" src="?entryPoint=attachment&amp;id=5fec48f49f577cc31">`

By utilizing this code line you are even able to fetch the image from the Document, or any other entity either. All you need is to define the `id` parameter of the desired image.
* Click the picture button in the tools panel -> input Image URL line -> Insert

Code view: `<img style="width: 350px;" src="https://www.espocrm.com/images/espocrm-logo.png">`

#### Resize image

* Setting size with the percentage: `style="width: 25%;"`
* Setting size with the pixel amount: `width="300" height="100"`

## Table

You can easily add a new table with the adding table tools on the panel.

Table 2x2 structure:
```
<table class="table table-bordered" border="0.5pt">
  <tbody>
    <tr bgcolor="#659B86">
      <td bgcolor="#659B86" width="25%" style="text-align: center;">
        <span style="color: rgb(0, 0, 0); font-size: 12px; line-height: 1;">some text</span>
      </td>
      <td width="75%" style="text-align: center;">
      </td>
    </tr>
    <tr>
      <td width="25%" style="text-align: center;">
      </td>
      <td width="75%" style="text-align: center;">
      </td>
    </tr>
  </tbody>
</table>
```
* `border="0.5pt"` - table attribute for setting the width of a table border. Without this parameter you won't see the table borders.
* `bgcolor="#659B86"` - set a background color. Works for the `<tr>` and the `<td>` tags.
* `width="25%"` - set a table cell width.
* `text-align: center;` - set a text position. Supports: `center`, `left`, `right`, ` justify`.
* `color: rgb(0, 0, 0);` - set the color of the text.
* `font-size: 12px;` - set the text size.
* `line-height: 1;` - set a line height.
* `<tr>` & `</tr>` - defines a table raw.
* `<td>` & `</td>` - defines a standard data cell in a table.
* `<td ><span style="font-size: 10px;">{{dateQuoted}}</span><br></td>`

## Link

You can create a link by clicking the link button in the tool panel.
Code view: `<a href="https://www.espocrm.com">Click me</a>`
