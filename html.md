# Description lists

```
<dl>
	<dt>term</dt>
	<dd>description</dd>
</dl>
```

it can possible to have more than one term per item. Also, possible to have several descriptions per item. 
Also, possible to have multiple terms multiple descriptions.

# frames

used to divide browser window into multiple sections, each section can be loaded with a seperate html doc.
A collection of frames in a browser window is known as a *frameset*. Divided into frames in a similar way
used in tables; rows and columns.

## disadvantages of frames

+ Some smaller devices cannot cope with frames.
+ Sometimes page will be displayed differently on different computers due to different screen resolution.
+ The browser's back button might not work as the user hopes.
+ Few browsers that do not support frame technology.

## usage

```
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Frames</title>
   </head>
	
   <frameset rows = "10%,80%,10%">
      <frame name = "top" src = "/html/top_frame.htm" />
      <frame name = "main" src = "/html/main_frame.htm" />
      <frame name = "bottom" src = "/html/bottom_frame.htm" />
   
      <noframes>
         <body>Your browser does not support frames.</body>
      </noframes>
      
   </frameset>
   
</html>
```

Note using of `<frameset>` instead of body. `rows` attrib of frame set is for rows, unit should be supplied
(`px`, `%`, `em` etc.). `col` is for columns. If no unit is mentioned, (ex: `100` instead of `100%`) it is
considered as a pixel value like `100px`.

+ `border` attrib is for width of the border in each frame.
+ `frameborder` is a boolean attrib takes 0 or 1 to mention wether the frames should have a 3d border.
+ `framespacing` is for the space between frames.

## frame tag

Following is a list of attribs.

+ `src` - Gives the file that should be loaded into that frame.
+ `name` - This allows to give a name
+ `frameborder` - boolean attrib, takes 1 or 0, indicate wether the border should be displayed, overrides frameset's style.
+ `marginwidth` & `marginheight` - margin width and height, value is given in pixels no need to put unit as `px`.

## 3 mechanisms used to apply styles

1. Inline css
    - That's what they call applying css in "style" attr.
1. Internal css
    - That's the name they assigned for the action of using \<style\> element.
1. External css

## Important for exam!!!

+ Eventhough in real world, almost all the browsers by default open links having "\_blank" for "target" 
attribute, in exam, assume those links will open in a new window rather than a new tab. Exam Logic!

## Uses of [external] CSS

+ **Easy maintainance** and update web pages
+ **consistency** throughout the **website**.
+ **Re-style** any document, without modifying original html structure.
+ **single document** can be presented in **multiple styles** with multiple
stylesheets (Multiple device compatability)
+ **More formatting options**
+ **Reduce code duplication**
+ **SEO benifits**
+ **Clean code**

## CSS group selector

`.elem1, .elem2, .elem3 {}`
