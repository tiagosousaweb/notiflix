# Back Redirect

Com esse script sempre que o potencial cliente clicar no back redirect do navegador, ele será apontado para a url definida.

Todos os parâmetros da url serão adicionados automaticamente ao final da url.

```
<script>
    var urlBackRedirect = 'SUA URL AQUI'; // lembre-se de usar a url sem espaços
    // não altere nada abaixo dessa linha
    urlBackRedirect = urlBackRedirect = urlBackRedirect.trim() +
            (urlBackRedirect.indexOf("?") > 0 ? '&' : '?') +
            document.location.search.replace('?', '').toString();
    history.pushState({}, "", location.href);
    history.pushState({}, "", location.href);
    window.onpopstate = function () {
        setTimeout(function () {
            location.href = urlBackRedirect;
        }, 1);
    };
</script>
```

Para usar em múltiplos domínios:

```
var urlBackRedirect = '//' + window.location.hostname + '/PATH_RMKT'
```

