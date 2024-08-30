index.html
# Calculadora de Média Aritmética

Este repositório contém uma aplicação web simples para calcular a média aritmética de quatro números fornecidos pelo usuário. O projeto é uma introdução básica às tecnologias de front-end: HTML, CSS e JavaScript.

## Estrutura do Projeto

O projeto é composto pelos seguintes arquivos:

1. **`index.html`**: O arquivo HTML define a estrutura da página web. Ele inclui um formulário para o usuário inserir quatro números e um botão para calcular a média.

2. **`styles.css`**: O arquivo CSS é responsável pelo estilo visual da página. Ele define a aparência dos elementos HTML, como fontes, cores, e espaçamentos, para criar uma interface limpa e amigável.

3. **`script.js`**: O arquivo JavaScript contém a lógica para calcular a média dos quatro números inseridos pelo usuário. Ele é responsável por capturar os valores dos campos de entrada, calcular a média e exibir o resultado na página.

## Como Funciona

### HTML

O `index.html` estrutura a página com um formulário que contém quatro campos de entrada para números e um botão para acionar o cálculo. O HTML também inclui uma área para exibir o resultado.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Média</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Calculadora de Média Aritmética</h1>
        <form id="calculator-form">
            <label for="num1">Número 1:</label>
            <input type="number" id="num1" required>
            
            <label for="num2">Número 2:</label>
            <input type="number" id="num2" required>
            
            <label for="num3">Número 3:</label>
            <input type="number" id="num3" required>
            
            <label for="num4">Número 4:</label>
            <input type="number" id="num4" required>
            
            <button type="button" onclick="calculateAverage()">Calcular Média</button>
        </form>
        <div id="result">
            <p id="average">A média é: </p>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>





CSS
O styles.css estiliza a página, proporcionando um layout agradável e responsivo. Ele define o estilo dos inputs, botões e áreas de resultado, além de adicionar um fundo claro e sombras sutis para melhorar a aparência visual.

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f9;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    width: 100%;
}

h1 {
    text-align: center;
    color: #333;
}

form {
    display: flex;
    flex-direction: column;
}

label {
    margin-top: 10px;
    font-weight: bold;
}

input {
    padding: 8px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

button {
    margin-top: 20px;
    padding: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background-color: #0056b3;
}

#result {
    margin-top: 20px;
    text-align: center;
}

#average {
    font-size: 18px;
    font-weight: bold;
}


JavaScript
O script.js realiza o cálculo da média dos quatro números inseridos. Ele lê os valores dos campos de entrada, calcula a média aritmética e atualiza o conteúdo da página com o resultado.

function calculateAverage() {
    // Obtém os valores dos inputs
    const num1 = parseFloat(document.getElementById('num1').value);
    const num2 = parseFloat(document.getElementById('num2').value);
    const num3 = parseFloat(document.getElementById('num3').value);
    const num4 = parseFloat(document.getElementById('num4').value);

    // Verifica se todos os números são válidos
    if (isNaN(num1) || isNaN(num2) || isNaN(num3) || isNaN(num4)) {
        alert('Por favor, insira todos os números corretamente.');
        return;
    }

    // Calcula a média
    const average = (num1 + num2 + num3 + num4) / 4;

    // Exibe o resultado
    document.getElementById('average').textContent = `A média é: ${average.toFixed(2)}`;
}

