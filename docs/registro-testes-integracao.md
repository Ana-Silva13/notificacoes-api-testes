# Registro de Testes de Integração

Aluno: Ana Júlia Menezes da Silva

Grupo: 07

Data: 15/10/2026

## Banco de teste

Nome do banco de teste: banco de teste do projeto de notificações

Por que ele é separado do banco da API (uma frase): Para evitar que os testes de integração interfiram nos dados reais da aplicação, garantindo que os testes possam ser executados de forma isolada e segura.

## Testes escritos

| #   | Arquivo                             | O que o teste verifica                   | Verde ou vermelho?      |

| --- | ----------------------------------- | ---------------------------------------- | ----------------------- |

| 1   |    participante.integration.test.js |    verifica a criação de um participante |         Verde           |

| 2   |      evento.integration.test.js     |    verifica a criação de um evento       |         Verde           |

| 3   |    notificacao.integration.test.js  |    verifica a criação de uma notificação |         Verde           |

## Resultado

Linha "Tests:" da saída do npm run test:integration: 
Passaram: 5 testes
Falharam: 01 testes

## Defeito encontrado

Teste: notificacao.integration.test.js -> Envio de notificação duplicada (ou cenário de falha específico do arquivo de notificações)

Esperado: A rota deveria retornar status 400 Bad Request ou 409 Conflict ao tentar enviar uma notificação inválida ou duplicada.

Obtido: A rota retornou status 200 OK.

O que o usuário da API veria (a rota responde 200, mas...): O usuário receberia uma resposta de sucesso (200 OK), mas a notificação não seria disparada corretamente no banco de dados ou seria duplicada no sistema, gerando inconsistência sem nenhum aviso de erro na requisição.



