## Javascript and jQuery Scripts and Snippets

![Screenshot](https://github.com/shb-services/imortant-scripts-for-web/blob/main/assets/js%20and%20jquery.jpg)

#

### Hide Nitropack Branding

JavaScript Code
```Javascript

// Nitropack JS

document.addEventListener("DOMContentLoaded", function(){ 
  let divc = document.querySelectorAll('div[style]'); 
  for (let i = 0, len = divc.length; i < len; i++) { 
  let actdisplay = window.getComputedStyle(divc[i], null).display; 
  let actclear = window.getComputedStyle(divc[i], null).clear; 
  if(actdisplay == 'block' && actclear == 'both') { divc[i].remove(); 
} } });

```
jQuery Code

```javascript

// Hide Nitropack Branding


jQuery(document).ready(function(){

setTimeout(function(){

     //var tag_new = jQuery("template").eq(38).attr("id");
     var tag_new = jQuery("template").last().attr("id");
     console.log(tag_new);

     //alert(tag_new);
     jQuery("#" + tag_new).css("display", "none");
     jQuery("#" + tag_new).next().next().css("display", "none");
}, 100);

});
