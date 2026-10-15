# Registro de Testes Unitários
Aluno: Ana Júlia Menezes da Silva
Grupo: 07
Data: 24/09/2026
## Testes escritos
| # | Arquivo                         | O que o teste verifica                               | Tipo                    |
| - | ------------------------------- | ---------------------------------------------------- | ----------------------- |
| 1 | `tests/unit/validators.test.js` | Aceita um e-mail válido                              | sucesso                 |
| 2 | `tests/unit/validators.test.js` | Rejeita e-mail sem `@`                               | falha                   |
| 3 | `tests/unit/validators.test.js` | Aceita nome com exatamente o tamanho mínimo          | borda                   |
| 4 | `tests/unit/parseId.test.js`    | Rejeita ID não numérico (`abc`)                      | falha                   |
| 5 | `tests/unit/parseId.test.js`    | Rejeita ID parcialmente numérico (`12abc`)           | falha                   |
| 6 | `tests/unit/ambiente.test.js`   | Confirma a configuração básica do ambiente de testes | sucesso                 |
## Resultado
Passaram: 5 testes
Falharam: 1 teste
## Defeito encontrado
Teste: `parseId › rejeita um id parcialmente numérico como '12abc'`
Esperado: lançar `ValidationError`
Obtido: não lançou erro e retornou o valor `12`
## Cobertura
60% de Lines da linha `helpers`
Em uma frase, o que esse número significa: 60% das linhas de código dos helpers foram executadas pelos testes.

## Arrange, Act e Assert
No teste `aceita um nome com exatamente o tamanho mínimo`, do arquivo `tests/unit/validators.test.js`:

- **Arrange:** define `nome = "Ana"`, o tamanho mínimo `3` e o campo `"nome"`.
- **Act:** chama `minLength(nome, 3, "nome")` e guarda o resultado.
- **Assert:** verifica que o resultado é `null`, indicando que não há erro.

## 3. Teste que nunca fica vermelho
Um teste que nunca falha, mesmo quando o código está quebrado, não serve para verificar corretamente o comportamento do sistema. Ele pode dar uma falsa sensação de segurança, porque aparenta estar protegendo o código, mas não detecta defeitos. Um bom teste deve falhar quando a implementação não atende ao comportamento esperado.