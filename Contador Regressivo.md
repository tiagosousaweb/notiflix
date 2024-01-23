# Contador regressivo

![Contador Regressivo](https://raw.githubusercontent.com/tiagosousaweb/scripts-uteis/main/images/img2.png)

Código do contador, coloque onde o contador deverá aparecer:

```
<div class="countdown">
    <div class="label">O desconto encerra em:</div>
    <div class='time'>00:00</div>
</div>
```

No rodapé da página coloque o seguinte código:

```

<script>
    var MINUTOS = 15;
    // Não altere nada abaixo dessa linha
    function startTimer(duration, display) {
        var timer = duration,
                minutes, seconds;
        setInterval(function () {
            minutes = parseInt(timer / 60, 10);
            seconds = parseInt(timer % 60, 10);
            minutes = minutes < 10 ? "0" + minutes : minutes;
            seconds = seconds < 10 ? "0" + seconds : seconds;
            display.forEach(function (el) {
                el.textContent = minutes + ":" + seconds;
            })
            if (--timer < 0) {
                timer = 0;
            }
        }, 1000);
    }
    window.onload = function () {
        var minutesToSeconds = MINUTOS * 60,
                display = document.querySelectorAll('.time');
        startTimer(minutesToSeconds, display);
    };
</script>
<style>
    .countdown {
        font: normal 12px/20px Arial, Helvetica, sans-serif;
        word-wrap: break-word;
        box-shadow: 0 1px 1px 0 rgba(1, 1, 1, 0.4);
        width: 250px;
        height: 90px;
        text-align: center;
        background: #f1f1f1;
        border-radius: 5px;
        margin: 30px auto;
        font-weight: lighter;
    }
    .countdown .label {
        font-size: 12px;
        color: #65584c;
        text-align: center;
        text-transform: uppercase;
        display: inline-block;
        letter-spacing: 2px;
        padding: 7px 0;
    }
    .countdown .time {
        color: #fff;
        position: relative;
        z-index: 1;
        text-shadow: 1px 1px 0px #ccc;
        font-size: 48px;
        text-align: center;
        padding: 20px;
        border-radius: 0 0 5px 5px;
        display: block;
        background: #e5554e;
        box-shadow: 0 1px 2px 0 rgba(1, 1, 1, 0.4);
    }
</style>
```
