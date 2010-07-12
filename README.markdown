Hintify
===

What is it?
---
Hintify is a simple jQuery plugin that makes it easy to add helper texts inside of form inputs.  When the user clicks into the field the text disappears and allows the user to type whatever he or she wants.  If nothing is typed and the user leaves the field by clicking somewhere else the hint text reappears.

Why?
---
I recently finished up a project with three separate methods for doing this.  I decided I needed an easy unified technique.  This does almost everything I need in the way I expect it to work. The one thing it doesn't do is password fields. 

Last time I checked one or more browsers wouldn't let you change the type of an input field (from text to password) so the kind of technique used here wouldn't fly if you wanted to label your username & password fields inside the text box.  The best technique I've found for that is one where you position the label under the text box and make it transparent - then on focus change the box background to opaque. You can check out that technique in the wild viewing the source at http://spokt.com/

Requirements
---
  * jQuery - probably any version but I've only tested with 1.4.1

I've tested (manually) in Firefox 3, Safari 4, Chrome 5, & IE 7.  It is pretty simple so I expect it to work in all browsers.
  
Installation
---

1. Include jQuery and the hintify script in your HTML:

        <script src="/javascripts/jquery-1.4.1.js" type="text/javascript"></script>
        <script src="/javascripts/jquery.hintify.js" type="text/javascript"></script>

2. Add hints using the data-hint-text attribute:

        <input type="text" name="city[name]" data-hint-text="Phoenix" />
        <input type="text" name="city[population]" data-hint-text="20 million" />

3. Wire it up with something like the following. Alternately you could call the hintify() method on the selector directly but I always want class for CSS anyway which brings us to the next step

        $(document).ready(function(){
          $('input[data-hint-text]').addClass('hinter');
          $('.hinter').hintify();
        });

4. (Optional) You probably want to gray out the hint text with some CSS:

        input.hinter { color: #888; }
        input.hinter.filled { color:#000; }

License: see LICENSE for details (MIT)

___
