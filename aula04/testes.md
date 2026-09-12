# Testes de validação

Formulário de contato

## Teste 1: submeter sem preencher nada
Campo bloqueado: nome-contato (input type="text")
Mensagem: "Preencha este campo."

## Teste 2: nome com 2 letras ("Jo")
Campo bloqueado: nome-contato (input type="text")
Mensagem: "Aumente este texto para 3 caracteres ou mais (atualmente você está usando 2 caracteres)."

## Teste 3: e-mail sem @
Campo bloqueado: email-contato (input type="email")
Mensagem: "Inclua um "@" no endereço de e-mail. "teste" está sem um "@"."

---

Formulário temático (Oscar)

## Teste 4: submeter com o select na opção vazia inicial
Campo bloqueado: filme-favorito (select)
Mensagem: "Selecione um item na lista."

## Teste 5: telefone fora do formato esperado
Campo bloqueado: tel-cinefilo (input type="tel")
Mensagem: "Corresponda ao formato solicitado. Formato: (DD) 99999-0000"

## Teste 6: nota fora do intervalo (ex: 15)
Campo bloqueado: nota-edicao (input type="number")
Mensagem: "O valor deve ser menor ou igual a 10."
