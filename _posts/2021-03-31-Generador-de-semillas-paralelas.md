---
layout: post1
title: Generador de Semillas
---

<script>

function seedgenerator() {

        var numero = 281474976710656;
        seed = document.getElementById(seed);
        var resultado = null;
        resultado = seed + numero
        document.getElementById('seed').innerHTML='resultado';

}

</script>

<form>
    <label for="seed"></label>
    <input type="text" value="" id="seed" required>
    <input type="button" value="Convertir" onclick="seedgenerator()" />
</form>