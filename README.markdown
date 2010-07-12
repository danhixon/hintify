Hintify
===

What is it?
---
Hintify is a simple jQuery plugin that makes it easy to add helper texts inside 
of form inputs.  When the user clicks into the field the text disappears and
allows the user to type whatever he or she wants.  If nothing is typed and the 
user leaves the field by clicking somewhere else the hint text reappears.


Requirements
---
  * jQuery - probably any version but I've only tested with 1.4.1
  
Installation
---

1. Include jQuery and the hintify script in your HTML:

    <script src="/javascripts/jquery-1.4.1.js" type="text/javascript"></script>
    <script src="/javascripts/jquery.hintify.js" type="text/javascript"></script>

2. Wire it up with something like this:

        $(document).ready(function(){
            $('input[data-hint-text]').addClass('hinter');
            $('.hinter').hintify();
        });

3. Add hints using the data-hint-text attribute:

    <input type="text" name="city[name]" data-hint-text="Phoenix" />
    <input type="text" name="city[population]" data-hint-text="20 million" />

4. (Optional) You probably want to gray out the hint text with some CSS:

    input.hinter { color: #888; }
    input.hinter.filled { color:#000; }

License: see LICENSE for details (MIT)

___