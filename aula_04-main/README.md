# Gerenciador de Tarefas (ToDo List)

Aplicação Spring Boot com Thymeleaf para gerenciamento de tarefas.

## Tecnologias

- Java 21
- Spring Boot 4.0.3
- Thymeleaf
- Maven
- Bean Validation (Jakarta Validation)

## Como Executar

### Pré-requisitos

- Java 21 instalado
- Maven instalado (ou use o wrapper `./mvnw`)

### Passos

```bash
# 1. Clone o repositório
git clone <url-do-repositorio>
cd aula_04-main

# 2. Execute com Maven Wrapper (recomendado)
./mvnw spring-boot:run

# Ou com Maven instalado
mvn spring-boot:run
```

A aplicação iniciará na porta **8080**. Acesse: [http://localhost:8080/tarefas](http://localhost:8080/tarefas)

> **Windows:** use `mvnw.cmd spring-boot:run` no lugar de `./mvnw spring-boot:run`

## URLs Disponíveis

| URL                              | Método | Descrição                          |
|----------------------------------|--------|------------------------------------|
| `/tarefas`                       | GET    | Listar todas as tarefas            |
| `/tarefas?filtro=pendentes`      | GET    | Listar apenas tarefas pendentes    |
| `/tarefas?filtro=concluidas`     | GET    | Listar apenas tarefas concluídas   |
| `/tarefas/novo`                  | GET    | Formulário para nova tarefa        |
| `/tarefas/editar/{id}`           | GET    | Formulário para editar tarefa      |
| `/tarefas/salvar`                | POST   | Salvar tarefa (criar/atualizar)    |
| `/tarefas/excluir/{id}`          | POST   | Excluir tarefa                     |
| `/tarefas/status/{id}`           | GET    | Alternar status da tarefa          |

## Estrutura do Projeto

```
com.biopark.tarefas/
├── TarefasAppApplication.java    # Classe principal
├── controller/
│   └── TarefaController.java     # Controlador MVC
├── service/
│   └── TarefaService.java        # Regras de negócio
├── repository/
│   └── TarefaRepository.java     # Armazenamento em memória
└── model/
    └── Tarefa.java                # Entidade Tarefa
```

## Funcionalidades

- Criar, editar e excluir tarefas
- Alternar status entre "Pendente" e "Concluída"
- **Filtrar tarefas por status** (Todas / Pendentes / Concluídas)
- **Contador de tarefas** mostrando total, pendentes e concluídas
- Validação de formulários com mensagens de erro
- Mensagens flash de sucesso/erro
- 3 tarefas de exemplo pré-cadastradas
- Interface responsiva com CSS customizado
