# Atividade 3: Desafio "Verificador de Maioridade"

Este repositório contém a resolução do Desafio 1 da Atividade 3, que consiste em um script PHP para validação de maioridade com base no ano de nascimento informado pelo usuário. Se o usuário for maior de idade, o acesso é liberado e um arquivo de log é gerado.

## 👤 Informações do Aluno
* **Nome:** Maiara Soriano Lazzerini
* **Número:** 22
* **Turma:** 1|E DS

## 💻 Código Base Utilizado

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desafio 1</title>
</head>
<body>
    <?php
    if (\$_SERVER["REQUEST_METHOD"] == "POST") {
        \(nome = htmlspecialchars(\)_POST['nome']);
        \(ano_nascimento = intval(\)_POST['ano_nascimento']);
        
        \(idade = date("Y") - \)ano_nascimento;

        if (\$idade >= 18) {
            echo "<h3>Acesso permitido, \$nome!</h3>";
            \$log = "Nome: \(nome \vert{} Idade:\)idade anos | Data: " . date("d/m/Y H:i:s") . "\n";
            file_put_contents("log_acessos.txt", \$log, FILE_APPEND);
        } else {
            echo "<h3>Acesso negado, \$nome!</h3>";
        }
    }
    ?>

    <form method="POST">
        <label>Nome: <input type="text" name="nome" required></label><br><br>
        <label>Ano de Nascimento: <input type="number" name="ano_nascimento" required></label><br><br>
        <button type="submit">Enviar</button>
    </form>
</body>
</html>
```

## 🌐 Link para Acessar o Trabalho
Para testar o projeto localmente (com o servidor Apache/XAMPP ativo), acesse:
[http://localhost/php-exemplos-basicos/Assunto_3/5a_desafio1.php](http://localhost/php-exemplos-basicos/Assunto_3/5a_desafio1.php)
