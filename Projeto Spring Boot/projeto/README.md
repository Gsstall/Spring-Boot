# TODOLIST

## Como executar

- É preciso ter o java 17 e o maven instalados

- No linux, basta executar
- ```mvn clean install```
- ```java -jar ./target/todolist-1.0.0.jar```

## Sobre a aplicação

- Trata-se de um crud de tarefas, com as rotas de tarefa autenticadas usando o metodo basic auth e criptografia de senha. É utilizado um banco de dados em memoria.

## Rotas

### Criar Usuario

POST /users
</br>

Request
```
{
  "username": "username",
  "password": "password",
  "name": "name"
}
```

### Deletar Usuario

DELETE /users
</br>

Request</br>
Autenticada
```
{
  "username": "username",
  "password": "password"
}
```

### Criar Tarefa

POST /tasks
</br>

Request</br>
Autenticada
```
{
    "description": "tarefa",
    "title": "description",
    "priority": "alta",
    "startAt": "2023-11-18T17:24:12",
    "endAt": "2023-11-19T17:24:12"
}
```

### Atualizar Tarefa

PUT /tasks
</br>

Request</br>
Autenticada
```
{
    "description": "tarefa",
    "title": "description",
    "priority": "alta",
    "startAt": "2023-11-18T17:24:12",
    "endAt": "2023-11-19T17:24:12"
}
```

### Deletar Tarefa

DELETE /tasks/{taskId}
</br>

Autenticada

- GET /tasks
</br>

Autenticada