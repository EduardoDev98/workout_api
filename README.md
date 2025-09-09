🚀 WorkoutAPI
🔹 O que é o FastAPI?

O FastAPI é um framework moderno para construção de APIs em Python (3.6+), projetado para ser extremamente rápido, simples de aprender e pronto para produção. Ele aproveita os type hints do Python, trazendo validações automáticas, geração de documentação e alta performance para aplicações web.

🔹 Programação Assíncrona

Quando falamos em código assíncrono, significa que a aplicação consegue “aguardar” certas tarefas (como consultas ao banco de dados ou chamadas externas) sem travar o restante da execução. Isso permite que várias operações sejam tratadas de forma eficiente ao mesmo tempo.

🏋️ Projeto: WorkoutAPI

Esse projeto une duas paixões: programação e crossfit.
A ideia foi criar uma API simples, mas funcional, chamada WorkoutAPI, que pode ser utilizada para gerenciar competições. Apesar de enxuta, ela traz recursos práticos para aprender de forma hands-on como trabalhar com o FastAPI.

📊 Modelagem de Dados

O modelo de entidades e relacionamentos (MER) foi estruturado para contemplar atletas, centros de treinamento e categorias.

🛠️ Tecnologias Utilizadas

FastAPI (assíncrono)

SQLAlchemy + Alembic (ORM e migrations)

Pydantic (validações e schemas)

PostgreSQL (banco de dados via Docker)

⚙️ Como Executar

O ambiente foi configurado com Python 3.11.4 utilizando pyenv
.

Criar e ativar o ambiente
pyenv virtualenv 3.11.4 workoutapi
pyenv activate workoutapi
pip install -r requirements.txt

Subir o banco de dados

Requer docker-compose

make run-docker

Criar novas migrations
make create-migrations d="nome_da_migration"

Aplicar migrations no banco
make run-migrations

Rodar a API
make run


Acesse a documentação interativa em: http://127.0.0.1:8000/docs

🎯 Desafio Proposto

Implementar query parameters nos endpoints:

Atleta → nome, cpf

Customizar as respostas nos endpoints de listagem:

Atleta → nome, centro de treinamento, categoria

Tratar exceções de integridade do banco:

Exemplo: sqlalchemy.exc.IntegrityError

Mensagem: "Já existe um atleta cadastrado com o cpf: x"

Status: 303

Implementar paginação usando fastapi-pagination (limit e offset)

📚 Referências

FastAPI

Pydantic

SQLAlchemy

Alembic

FastAPI Pagination
