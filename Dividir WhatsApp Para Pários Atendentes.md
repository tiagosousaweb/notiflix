# Dividir WhatsApp para vários atendentes:

```

<script>
    function getWhatsAppNumber() {
        var mensagemWhats = 'Eu quero testar!';
        var phones = [
            119911111111,
            119911111112,
            119911111113,
            119911111114,
        ];

        var url = 'https://api.whatsapp.com/send?phone='
                + phones[Math.floor(Math.random() * phones.length)]
                + '&text='
                + encodeURIComponent(mensagemWhats);

        window.open(url, '_blank');
    }
</script>
<a href="#" onclick='getWhatsAppNumber()'>Falar com um atendente</a>
```