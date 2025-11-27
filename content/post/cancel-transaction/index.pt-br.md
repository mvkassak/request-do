---
title: Desbloqueando sessões com um único comando
description:
date: '2023-12-03'
categories:
    - Dicas
tags:
    - Sessão
---

Já viu uma barrinha amarela rodando escrito Running Transaction e aquele contador não para de subir nunca?
Pois é, eu já vi também — principalmente quando estou rodando uns scripts meio suspeitos no background...

## O que é o `cancel_my_transaction.do`?

É basicamente o comando que vai te salvar quando estiver em uma sessão travada por muito tempo.  
Quando o ServiceNow congela — normalmente por causa de uma transação que demorou demais — esse comando manda a plataforma cancelar o que está travando tudo, e assim você consegue voltar a trabalhar sem precisar dar refresh ou fazer logout.

## Como usar

É super simples:

- Pegue a URL atual do seu ServiceNow e adicione `/cancel_my_transaction.do` no final.
- Aperte Enter — e pronto, sua sessão deve destravar quase que na hora.

Exemplo:  
`https://suainstancia.service-now.com/cancel_my_transaction.do`

## Pontos de atenção

Antes de sair usando, só um aviso rápido:

- **Você pode perder trabalho não salvo.**  
  Se você cancelar uma transação que estava no meio de salvar ou processar dados, pode perder essas informações.
- **Pode impactar workflows.**  
  Se a sessão travada fazia parte de um processo maior (como uma aprovação ou um script rodando em background), cancelar pode afetar o andamento.

Então é isso — use quando precisar, mas use com consciência.

## Considerações finais

O `cancel_my_transaction.do` é um daqueles truques simples que todo dev de ServiceNow deveria conhecer. Não é mágica, mas quando você está travado e precisa continuar, ele salva o dia de verdade.

---