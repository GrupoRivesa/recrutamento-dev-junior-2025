# Desafio Técnico – API de Gestão de Veículos
## Objetivo

Desenvolver uma API RESTful para gerenciar uma entidade de veículos. A API deve permitir operações de CRUD (Create, Read, Update, Delete) e estar protegida por autenticação via token fixo.

---

## Entidade: Vehicle

A entidade `Vehicle` deve conter os seguintes campos:

- `id`: int (Auto Increment)
- `vin`: string (Vehicle Identification Number)
- `placa`: string
- `modelo`: string
- `data_entrega`: date
- `data_fabricacao`: date
- `data_venda`: date
- `pais_operacao`: string
- `concessionaria_venda`: string
- `data_ultimo_reparo`: date
- `documento_proprietario`: string (CNPJ ou CPF)
- `ultima_atualizacao`: datetime

---

## Requisitos Funcionais (RF)

- **RF01**: A API deve permitir criar um novo veículo.
- **RF02**: A API deve permitir listar todos os veículos.
- **RF03**: A API deve permitir buscar um veículo por ID.
- **RF04**: A API deve permitir atualizar os dados de um veículo.
- **RF05**: A API deve permitir deletar um veículo.
- **RF06**: A API deve estar protegida por autenticação via token fixo no header `Authorization`.

---

## Regras de Negócio (RN)

- **RN01**: O campo `vin` deve ser único.
- **RN02**: O campo `documento_proprietario` deve aceitar tanto CPF quanto CNPJ válidos.
- **RN03**: A `data_fabricacao` não pode ser posterior à `data_entrega` ou `data_venda`.
- **RN04**: A `data_ultimo_reparo` não pode ser anterior à `data_fabricacao`.

---

## Requisitos Não Funcionais (RNF)

- **RNF01**: Utilizar uma ORM (como Sequelize, Prisma, TypeORM ou outra de sua escolha).
- **RNF02**: Utilizar migrações para criação da estrutura do banco de dados.
- **RNF03**: Tipar os dados da aplicação (preferencialmente com TypeScript).
- **RNF04**: A API deve seguir o padrão REST.
- **RNF05**: O código deve estar versionado em um repositório Git (público ou privado com acesso concedido).
- **RNF06**: Incluir um arquivo `README.md` com instruções de setup e execução do projeto.

---

## Autenticação

- A autenticação deve ser feita via token fixo.
- O token pode ser algo como: `Bearer 1234567890abcdef`
- Todas as rotas devem exigir esse token no header `Authorization`.

---

## Entrega

- Link para o repositório com o código.
- Banco de dados pode ser SQLite, PostgreSQL, MySQL ou outro de sua preferência.

---

Boa sorte! 🍀
