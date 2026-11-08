# Volume 12 — Respondendo comentários e mensagens com n8n

Pasta de trabalho do volume (`aula12`), versionada com git. O n8n, o app da Meta e a credencial
`Instagram TEP` são os do Volume 11; o agente do Direct usa a credencial `Groq` do Volume 10.

| Arquivo | Seção | Papel |
| --- | --- | --- |
| `eventos/comentario.json` | 2.2, 5.2 | Evento de comentário, no formato que a Meta envia ao webhook, com identificadores fictícios |
| `eventos/mensagem.json` | 2.2, 6.1 | Evento de mensagem do Direct, no mesmo formato |
| `.gitignore` | 1.1 | Exclui `.env`, `.venv/` e `__pycache__/` do controle de versão |
| `workflows/` | Prática | Recebe os workflows exportados do n8n (passo 5 do roteiro) |

Os eventos servem para construir o fluxo antes de o túnel estar no ar: cole o conteúdo no nó
**Evento do Instagram** como dado fixado (*Pin data*) e troque o `media.id` pelo id do seu post.
Desafixe os dados antes de publicar o workflow.

Nenhum arquivo daqui contém token nem segredo. No `verificacao-webhook.json`, o token de
verificação do webhook (seção 3.1) foi trocado por `COLE-AQUI-O-TOKEN-DE-VERIFICACAO` no nó
**Token confere?**: ao importar o workflow, escreva ali o token que você registrou na Meta.
As credenciais `Instagram TEP` e `Groq` não vão nas exportações; crie-as no n8n e escolha-as nos nós.
