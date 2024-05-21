# Using @supports to target email clients

The technique below uses very minimal code to show and hide an interactive section. 

```
<!DOCTYPE html>
<html>
  <head>
    
    <style>
      @supports(--css: variables) {
        .interactive {display:block!important}
        .fallback {display:none}
      }  
    </style>

  </head>
<body>

  <div class="fallback">Fallback</div>

  <!--[if !mso]><!-->
    <div class="interactive" style="display:none">Interactive content</div>
  <!--<![endif]-->

</body>
</html>
```
