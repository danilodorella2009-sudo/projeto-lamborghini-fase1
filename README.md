# 🚀 Minhas Atividades de Java Web — Edição Lamborghini

Este repositório foi criado para centralizar e organizar todas as atividades práticas desenvolvidas durante as aulas de desenvolvimento web com Java. O objetivo principal é evoluir conceitos de Orientação a Objetos (como encapsulamento e herança) e manipulação de arquivos locais (TXT e CSV), integrando-os diretamente a serviços web e APIs com retornos em formato JSON sobre o universo da **Automobili Lamborghini**.

---

## 📌 Índice do Projeto

Abaixo estão listados os tópicos principais com os sistemas desenvolvidos e o acesso às documentações técnicas.

---

## 📖 1. Documentações

Toda a API do projeto foi modelada e documentada para garantir padronização, testes práticos e fácil integração.

- **Padrão OpenAPI 3.0.3:** Especificação completa com descrições de rotas, schemas de dados, códigos de resposta HTTP e exemplos de payload JSON.
- **Testes Interativos:** Compatível diretamente com o **Swagger Editor** e **Postman**.

📄 **[Acessar Arquivo Swagger (swagger.yaml)](#)** *(Substitua este link pelo arquivo do seu projeto)*

---

## 🏎️ 2. Linha Automobili Lamborghini

Sistemas e endpoints focados na gestão de garagem, modelos de alta performance e processamento de configurações personalizadas.

### 🎵 1. A Garagem Virtual (Playlist de Superesportivos)
- **O que faz:** Transforma um programa de terminal em uma garagem inteligente. O sistema lê um arquivo de texto local com os veículos cadastrados na coleção, converte os dados em objetos Java (modelo, motorização e ano de lançamento) e os envia para o cliente em formato JSON. Também permite cadastrar novos veículos sem apagar os existentes.
- **Endpoints desenvolvidos:**
  * `GET /garagem/listar` — Lê o arquivo `minha_garagem.txt` linha por linha e retorna a lista completa de carros em JSON.
  * `POST /garagem/adicionar` — Recebe um novo modelo no corpo da requisição e salva no final do arquivo em modo append.
- **Conceitos aplicados:** Criação de endpoints HTTP, manipulação de arquivos com `FileReader`/`BufferedReader` e `FileWriter`/`BufferedWriter` (modo append), e configuração de CORS para testes via Swagger Editor.

📂 **[Acessar arquivos desta atividade](#)**

---

### ⚔️ 2. O Catálogo de Modelos Web
- **O que faz:** Simula o backend de uma vitrine de seleção de superesportivos da Lamborghini. O servidor lê uma base de dados no formato CSV, interpreta as regras de herança das categorias de veículos (`V12Hibrido` e `SuperSUV`) e entrega uma lista completa ou filtrada conforme a escolha do usuário na URL.
- **Endpoints desenvolvidos:**
  * `GET /modelos/todos` — Lê o arquivo CSV, faz o `split(";")` e instancia as classes filhas corretas.
  * `GET /modelos/categoria/{tipo}` — Filtra os veículos da categoria especificada (`v12` ou `suv`) usando o operador `instanceof`.
- **Conceitos aplicados:** Herança de classes, manipulação de arquivos estruturados (CSV), uso de parâmetros de caminho na URL e filtros de busca com listas.

📂 **[Acessar arquivos desta atividade](#)**

---

### 🏆 3. O Portal de Configuração (L-Code Hackathon)
- **O que faz:** Atua como o painel de controle de pedidos do estúdio de customização. Ao ser acionado pela web, o servidor processa em lote um arquivo com pedidos de configuração brutos, valida as regras de elegibilidade (disponibilidade do motor e personalização *Ad Personam*), gera arquivos separados de pedidos aprovados e pendências de fábrica, e retorna um relatório estatístico em tempo real.
- **Endpoints desenvolvidos:**
  * `POST /configurador/processar` — Valida os pedidos, gera os arquivos locais de saída (`pedidos_aprovados.txt` e `pendencias_fabrica.txt`) e retorna um JSON com o resumo do processamento.
- **Conceitos aplicados:** Validação de regras de negócio complexas, leitura/escrita simultânea de múltiplos arquivos com `BufferedReader`/`BufferedWriter` e criação de objetos de transferência de dados (DTOs) para respostas personalizadas.

📂 **[Acessar arquivos desta atividade](#)**

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Função no Projeto |
| :--- | :--- |
| **Java** | Linguagem de programação principal do ecossistema. |
| **OpenAPI / Swagger** | Documentação e testes interativos dos endpoints da API. |
| **JSON** | Formato de comunicação e transferência de dados entre a API e o cliente. |
| **TXT / CSV** | Utilizados como persistência local de dados (simulando bancos de dados em arquivos). |

---

*Projeto desenvolvido para fins educacionais e demonstrativos integrando conceitos de Java Web com a identidade visual da Automobili Lamborghini.*
