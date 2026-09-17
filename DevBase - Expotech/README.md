# 🗃️ DevBase | Rede Social em Python e MySQL

Sistema de terminal que simula uma rede social simples, desenvolvido em Python com integração ao MySQL. O projeto foi construído para a Expotech, aplicando desde a modelagem do banco de dados até a lógica de negócio da aplicação — cobrindo cadastro de usuários, publicação de conteúdo, interações sociais (curtidas e comentários) e funcionalidades de sistema como feedback e notificações.

## 🎯 Objetivo

Praticar o desenvolvimento de um sistema completo (CRUD + regras de negócio) integrado a um banco de dados relacional, aplicando conceitos de estruturação de projeto backend, organização de código em funções e manipulação de dados via SQL.

## ⚙️ Funcionalidades

**Usuário**
- Criar conta
- Login (autenticação por email e senha)
- Listar usuários
- Buscar usuário por ID
- Atualizar dados do usuário
- Deletar usuário (remove também seus tópicos, comentários, perfil, feedbacks e notificações)

**Conteúdo**
- Criar tópico
- Listar tópicos
- Comentar em um tópico

**Interações**
- Curtir tópico ou comentário

**Perfil**
- Criar perfil (bio, nível de experiência e área de interesse)

**Sistema**
- Enviar feedback
- Criar notificação
- Registrar acesso diário (sistema de pontuação)
- Gerar recuperação de senha (via token único)

## 🗂️ Estrutura do banco de dados

| Tabela | Principais campos |
|---|---|
| `tbl_usuario` | nome_usuario, email_usuario, senha_usuario, sexo_usuario |
| `tbl_topico` | titulo_topico, tipo_topico, id_usuario |
| `tbl_comentario` | texto_comentario, id_usuario, id_topico |
| `tbl_curtida` | id_usuario, id_topico, id_comentario |
| `tbl_perfil` | bio_perfil, nivel_perfil, area_interesse_perfil, id_usuario |
| `tbl_feedback` | msg_feedback, id_usuario |
| `tbl_notificacao` | msg_notificacao, id_usuario |
| `tbl_acesso_diario` | pontuacao_dia_acesso_diario, id_usuario |
| `tbl_projeto` | titulo_projeto, descricao_projeto, link_projeto, id_usuario |
| `tbl_recuperacao_senha` | token_recuperacao_senha, id_usuario |

## 🛠️ Tecnologias

- **Python** — lógica da aplicação e regras de negócio
- **MySQL** — armazenamento e persistência dos dados
- **mysql-connector-python** — conexão entre a aplicação Python e o banco MySQL
- **Git & GitHub** — versionamento de código

## ⚙️ Como rodar

```bash
# Clone o repositório
git clone https://github.com/iamgabrielferreira/devbase-crud-python-mysql.git

# Entre na pasta do projeto
cd devbase-crud-python-mysql

# Instale a dependência
pip install mysql-connector-python

# Configure a conexão com o banco em conexao.py
# (host, usuário, senha, nome do banco e porta)

# Crie o banco de dados "devbase_expotech" no MySQL
# e as tabelas correspondentes (ver seção "Estrutura do banco de dados")

# Execute a aplicação
python main.py
```

## 📚 O que aprendi

Este projeto me permitiu praticar a modelagem de um banco de dados relacional com múltiplas entidades relacionadas entre si (usuários, tópicos, comentários, curtidas, perfis), além de estruturar a exclusão em cascata manualmente e organizar um sistema de menu para navegação entre as funcionalidades — reforçando lógica de programação, manipulação de dados via SQL e organização de código em Python.

## 🔮 Próximos passos

- [ ] Mover credenciais do banco para variáveis de ambiente
- [ ] Criar arquivo `requirements.txt`
- [ ] Adicionar validações de entrada (ex: impedir email duplicado, senha vazia)
- [ ] Migrar a lógica para uma API REST (ex: com Flask ou FastAPI)
- [ ] Adicionar testes automatizados

## 🔗 Contato

- [LinkedIn](https://www.linkedin.com/in/gabrielferreiradias-ti/)
- [GitHub](https://github.com/iamgabrielferreira)
