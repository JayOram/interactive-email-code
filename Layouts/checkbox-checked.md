# Checkbox checked

This technique uses a checkbox immediately after the opening `<body>` tag which is set to checked. If an email client supports `.class:checked` then the interactive element will work.

```
<!DOCTYPE html>
<html>
  <head>
    
    <style>
      .checkboxsupported:checked ~* .interactive {display:block!important}
      .checkboxsupported:checked ~* .fallback {display:none}
    </style>

  </head>
  <body>
  
<!--[if !mso]><!-->
  <input type="checkbox" style="display:none" class="checkboxsupported" checked>
<!--<![endif]-->

<div class="fallback">Fallback</div>
<!--[if !mso]><!-->
<div class="interactive" style="display:none">Interactive content</div>
<!--<![endif]-->

  </body>
</html>
```
