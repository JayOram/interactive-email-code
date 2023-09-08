# Checkbox checked

This technique uses a checkbox immediately after the opening `<body>` tag which is set to checked. If an email client supports `.class:checked` then the interactive element will work.

```
<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml" xmlns:v="urn:schemas-microsoft-com:vml" xmlns:o="urn:schemas-microsoft-com:office:office">
  <head>
    <meta content="text/html; charset=utf-8" http-equiv="Content-Type" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!--[if !mso]><!-->
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <!--<![endif]-->
    <meta name="format-detection" content="telephone=no, date=no, address=no, email=no, url=no">
    <meta name="x-apple-disable-message-reformatting" />
    <!--Built in London by the ActionRocket team - @ActionRocket -->
    <title>Checkbox Checked</title>
    <style>
      .checkboxsupported:checked ~* .interactive {display:block!important}
      .checkboxsupported:checked ~* .fallback {display:none}
    </style>
  </head>
  <body style="margin:0!important; padding:0!important; width:100%!important;" class="body">
  
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
