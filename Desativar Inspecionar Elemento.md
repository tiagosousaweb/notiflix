# Desativar clique com botão direito e inspecionar elemento

```

<script>
    document.addEventListener("keydown", function (e) {
        if (e.keyCode == 123 || (e.ctrlKey && e.shiftKey && e.keyCode == 73)) { 
            e.preventDefault()
        }
    }, true);
    document.addEventListener('contextmenu', function (e) {
        e.preventDefault()
    }, true);
</script>
```