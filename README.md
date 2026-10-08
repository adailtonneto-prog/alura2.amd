# 🎯 Jogo de Adivinhação

Um jogo simples em JavaScript onde o jogador tenta adivinhar um número secreto em até **5 tentativas**. A cada palpite errado, o programa informa se o número secreto é maior ou menor.

## Como jogar

1. O jogador digita um palpite na caixa de diálogo (`prompt`).
2. O programa compara o palpite com o número secreto:
   - Se acertar, exibe **"Parabéns"** e o jogo termina.
   - Se errar, dá uma dica: o número secreto é **maior** ou **menor**.
3. Se as 5 tentativas acabarem sem acerto, o jogador perde e o número secreto é revelado.

## Como executar

**Opção 1 – Console do navegador**

1. Abra qualquer página no navegador.
2. Pressione `F12` e vá até a aba **Console**.
3. Cole o código e pressione `Enter`.

**Opção 2 – Arquivo HTML**

Crie um arquivo `index.html` com o conteúdo abaixo e abra-o no navegador:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Jogo de Adivinhação</title>
</head>
<body>
  <script src="jogo.js"></script>
</body>
</html>
```

## Código (`jogo.js`)

```javascript
let numeroSecreto = 42;
let tentativas = 5;
let acertou = false;

for (let i = 1; i <= tentativas; i++) {
    let palpite = parseInt(prompt(`Tentativa ${i}/${tentativas} - Adivinhe o número secreto:`));

    if (palpite === numeroSecreto) {
        alert("Parabéns");
        acertou = true;
        break;
    } else if (palpite > numeroSecreto) {
        alert("Dica: o número secreto é menor.");
    } else {
        alert("Dica: o número secreto é maior.");
    }
}

if (!acertou) {
    alert(`Você perdeu! O número secreto era ${numeroSecreto}.`);
}
```

## Conceitos utilizados

- **Laço `for`**: limita o jogo a 5 tentativas.
- **Condicionais `if / else if / else`**: comparam o palpite com o número secreto usando `===`, `>` e `<`.
- **`break`**: encerra o laço quando o jogador acerta.
- **`prompt()` e `alert()`**: entrada e saída de dados no navegador.
- **`parseInt()`**: converte o texto digitado em número.

## Personalização

Para mudar o número secreto ou a quantidade de tentativas, altere as variáveis no início do código:

```javascript
let numeroSecreto = 42;  // qualquer número que você quiser
let tentativas = 5;      // número máximo de tentativas
```
