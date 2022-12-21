# Como adicionar jquery via browser console

```javascript
var element = document.createElement('script');
element.src = "https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js";
document.getElementsByTagName('head')[0].appendChild(element);
// dê tempo para o script carregar e digite (ou veja abaixo a opção sem espera)
jQuery.noConflict();
```

Adicione o código no console do seu navegador.