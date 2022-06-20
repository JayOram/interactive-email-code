# Interactive email code
A repository to share different interactive email techniques.

The aim of this repo is to share examples of ways to code interactive elements in email, therefore only using HTML and CSS.

## 1. Techniques to show/hide an interactive section
CSS and HTML to include in your emails to show the interactive element where it is supported and show a different experience for email clients that don't support those techniques.

For example: 

CSS
```
@media screen { 
  /* This CSS will not be shown in 
  Windows Desktop Outlook clients */ 
  }
```

HTML
```
<!--[if !mso]><!-->
<p>This will be hidden on Windows Desktop Outlook</p>
<!--<![endif]-->
```

All of these techniques put the 'fallback' or code that is not interactive before the interactive section. This is deliberate, as some interactive elements can add a lot of code and as email developers we need to consider <a href="https://github.com/hteumeuleu/email-bugs/issues/41">Gmail's 100kb(ish) limit</a>. Another Gmail limitation is the size of the `<style>` tag in the head, which needs to be kept to <a href="https://github.com/hteumeuleu/email-bugs/issues/90">16kb</a>.

## 2. Full interactive elements
The second type of file will be full interactive modules, with all the CSS and HTML needed to implement in your emails.
