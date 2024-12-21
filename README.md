# Teste Técnico - Desenvolvedor Backend

Bem-vindo ao teste técnico para a posição de Desenvolvedor Backend na Weatech Solutions! Este teste foi projetado para avaliar suas habilidades técnicas em desenvolvimento backend.

## Contexto do Sistema
Você deverá desenvolver um backend para um **Portal de Fornecedores de Oficinas**. O sistema será usado para gerenciar fornecedores de peças e serviços automotivos, permitindo cadastro, login, upload de documentos e controle de permissões.

## Requisitos Funcionais

### 1. Autenticação e Autorização
- **Login**: Implementar autenticação via JWT.
- **Cadastro de usuários**:
  - Deve permitir o cadastro de três tipos de usuários: `admin`, `fornecedor` e `cliente`.
- **Permissionamento**:
  - Apenas usuários `admin` podem criar ou remover outros usuários.
  - Apenas usuários `fornecedor` podem enviar documentos de suas empresas.
  - Apenas usuários `cliente` podem visualizar documentos enviados pelos fornecedores.

### 2. Gerenciamento de Documentos
- Implementar um endpoint para **upload de documentos** (ex.: PDF ou imagens).
  - Os arquivos devem ser salvos em um diretório específico no servidor.
  - Armazene no banco de dados o caminho do arquivo, o usuário que enviou e uma data de envio.
- Implementar um endpoint para **listar documentos**.
  - Apenas usuários `cliente` podem acessar os documentos.

### 3. Gestão de Fornecedores
- Criar um CRUD básico para fornecedores com os seguintes campos:
  - Nome da empresa
  - CNPJ
  - Telefone
  - Email de contato

### 4. Logs de Atividades
- Implementar logs de atividades em uma tabela separada no banco de dados. Os logs devem registrar:
  - ID do usuário
  - Tipo de ação (ex.: login, upload de documento, etc.)
  - Timestamp

### 5. Desafio Extra
- Criar um endpoint para **relatórios**:
  - Permitir que administradores façam download de um relatório consolidado em formato CSV com todos os fornecedores cadastrados e os documentos enviados.

## Tecnologias Aceitas
- **JavaScript/TypeScript** (Node.js, Express, Fastify, etc.)
- **PHP** (Laravel)
- **Python** (Django, Flask, FastAPI)

## Requisitos Técnicos

### Estrutura do Projeto
- Organize o projeto com uma estrutura clara e escalável.
- Utilize boas práticas de código, como separação de responsabilidades, uso de middlewares, etc.

### Banco de Dados
- Escolha entre PostgreSQL, MySQL ou SQLite.
- Crie as tabelas necessárias para suportar os requisitos acima.

### Segurança
- Armazene senhas de forma segura (ex.: hash bcrypt).
- Implemente validação no backend para todos os dados recebidos.

### Testes
- Escreva pelo menos 5 testes unitários para validar endpoints críticos.

## Instruções de Entrega

1. Faça um fork do repositório que será compartilhado com você (ou crie um repositório público no GitHub/GitLab).
2. Suba o código do seu projeto.
3. Inclua um arquivo README.md com:
   - Instruções para rodar o projeto.
   - Exemplos de chamadas de API (se possível, use ferramentas como Postman ou Curl).
4. Envie o link do repositório para avaliação.

## Critérios de Avaliação
- Funcionalidade: O sistema atende os requisitos descritos?
- Qualidade do código: Legibilidade, organização e boas práticas.
- Segurança: Implementação de autenticação, autorização e proteção de dados.
- Testes: Cobertura e qualidade dos testes.
- Documentação: Clareza e completude do README.

Boa sorte!
