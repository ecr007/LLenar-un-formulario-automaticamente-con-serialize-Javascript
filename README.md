# LLenar-un-formulario-automaticamente-con-serialize-Javascript

```javascript
var str_data = $(form).serialize();

$.each(str_data.split('&'), function (index, elem) {
   var vals = elem.split('=');
   $("[name='" + vals[0] + "']").val(decodeURIComponent(vals[1].replace(/\+/g, ' ')));
});
```
