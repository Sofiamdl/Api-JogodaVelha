# Api-JogodaVelha
## Descrição do Projeto
Projeto de API de um jogo da velha que será implementado em Node+Express. Proposto para a disciplina IF977 - Engenharia de Software - Prof Vinícius Garcia.

### O Projeto


###### Método para o usuário criar uma nova sessão: 
- POST /session

Exemplo:
Pedido:
```
{ 
player1ID: "123"
}
```
Resposta:
```
body: {
  id: 223,
  player1ID: 123,
  player2ID: null,
  board: [
  [null,null,null],
  [null, null, null],
  [null, null, null]
  ]
}
```


###### Método para o usuário entrar em uma sessão com ID aleátoria, escolhida pelo sistema
- PATCH /session/id

Exemplo:
Pedido:
```
{ 
player2ID: 4
}
```
Resposta: 
```
body: {
  id: 224,
  player1ID: 3,
  player2ID: 4,
  board: [
  [null,null,null],
  [null, null, null],
  [null, null, null]
  ]
}
```


##### Método para o usuário entrar em uma sessão com ID já existente, que o usuário colocará como input
- PATCH /session/boardID

Exemplo:
Pedido:
```
{ 
player2ID: 2
}
```
Resposta: 
```
body: {
  id: 223,
  player1ID: 1,
  player2ID: 2,
  board: [
  [null,null,null],
  [null, null, null],
  [null, null, null]
  ]
}
```


##### Método para o usuário mudar o "board" da sessão
- PATCH /session/boardID

Exemplo:
Pedido:
```
{ 
board: [
  [null,null,null],
  [null, 1, null],
  [null, null, null]
  ]
}
```
Resposta: 
```
body: {
  id: 224,
  player1ID: 3,
  player2ID: 4,
  board: [
  [null,null,null],
  [null, 1, null],
  [null, null, null]
  ]
}
```


##### Método para deletar sessão quando jogo terminar
- DELETE/session/id



