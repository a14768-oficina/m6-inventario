# 📊 Inventário de Computadores – Aplicação Web (PHP + SQL)

## 👤 Identificação
- **Nome do aluno:** Afonso Almeida  
- **Turma:** 2ºI  
- **Disciplina:** REDES – M6 – Programação de Sistemas de Informação  
- **Curso:** GPSI – 2.º Ano  

---

## 🎯 Objetivo do Projeto

Este projeto consiste no desenvolvimento de uma aplicação web para gestão e consulta de um inventário de computadores de uma sala informática, utilizando **PHP** para a lógica da aplicação e **SQL** para a base de dados.

A aplicação permite:
- Consultar informações técnicas dos computadores
- Visualizar especificações completas de hardware
- Organizar os equipamentos por salas
- **Pesquisa dinâmica em tempo real** (AJAX)
- Aceder a detalhes completos de cada computador

**🔗 Link da aplicação:** [https://a14768-oficina.infinityfree.me/m6-inventario/index.php](https://a14768-oficina.infinityfree.me/m6-inventario/index.php)

---

## 🧱 Estrutura Geral do Projeto

### 📁 Organização das Pastas e Ficheiros

```
m6-inventario/
│
├── index.php           # Página principal - Centro de Comando
├── detalhe.php         # Página de detalhes técnicos
├── pesquisa.php        # Sistema de pesquisa dinâmica (Live Search)
├── api_pesquisa.php    # API para pesquisa AJAX
├── config.php          # Configuração da base de dados
└── README.md           # Documentação
```

### 🗄️ Estrutura da Base de Dados

A base de dados foi desenvolvida em **MySQL** e contém as seguintes tabelas principais:

#### Tabela: `salas`
| Campo      | Tipo         | Descrição                    |
|------------|--------------|------------------------------|
| id_sala    | INT (PK)     | Identificador único da sala  |
| nome_sala  | VARCHAR(100) | Nome da sala                 |

#### Tabela: `computadores`
| Campo              | Tipo         | Descrição                           |
|--------------------|--------------|-------------------------------------|
| id_computador      | INT (PK)     | Identificador único do computador   |
| nome_computador    | VARCHAR(100) | Nome/hostname do computador         |
| id_sala            | INT (FK)     | Referência à sala                   |
| processador        | VARCHAR(100) | Modelo do processador               |
| ram                | VARCHAR(50)  | Capacidade de memória RAM           |
| armazenamento      | VARCHAR(50)  | Capacidade de armazenamento         |
| placa_grafica      | VARCHAR(100) | Modelo da placa gráfica             |
| sistema_operativo  | VARCHAR(100) | Sistema operativo instalado         |

#### Tabela: `software`
| Campo         | Tipo         | Descrição                      |
|---------------|--------------|--------------------------------|
| id_software   | INT (PK)     | Identificador único do software|
| nome_software | VARCHAR(100) | Nome do software               |
| versao        | VARCHAR(50)  | Versão do software             |

#### Tabela: `computador_software`
| Campo         | Tipo     | Descrição                              |
|---------------|----------|----------------------------------------|
| id_computador | INT (FK) | Referência ao computador               |
| id_software   | INT (FK) | Referência ao software                 |

### 🔗 Relações entre Tabelas
- **Salas ↔ Computadores**: Relação 1:N (uma sala pode ter vários computadores)
- **Computadores ↔ Software**: Relação N:M através da tabela `computador_software`

---

## ⚙️ Funcionalidades Desenvolvidas

Lista das funcionalidades implementadas no projeto:

- [x] Ligação à base de dados com PHP (PDO)
- [x] Listagem de computadores por sala
- [x] Visualização das características técnicas de cada computador
- [x] Consulta do software instalado
- [x] Página de detalhes por computador
- [x] **Pesquisa dinâmica em tempo real (AJAX/Live Search)** ⭐ **NOVO**
- [x] **API RESTful para pesquisa** ⭐ **NOVO**
- [x] **Navegação por teclado na pesquisa** ⭐ **NOVO**
- [x] Organização do dashboard com estatísticas por sala
- [x] Melhorias visuais no interface (design futurista profissional)
- [x] Sistema de navegação por abas (filtro por salas)
- [x] Design responsivo (adaptado para mobile)
- [x] Animações e efeitos visuais modernos

### 🆕 Funcionalidades Novas Adicionadas

#### 1. **Pesquisa Dinâmica (Live Search) com AJAX**
- Pesquisa em tempo real sem recarregar a página
- Resultados aparecem enquanto o utilizador escreve
- Debounce de 300ms para otimizar pedidos ao servidor
- Pesquisa em múltiplos campos:
  - Nome do computador
  - Processador
  - Sistema operativo
  - RAM, Armazenamento
  - Software instalado
- Navegação por teclado (setas ↑↓, Enter, ESC)
- Mensagens de status dinâmicas

#### 2. **API REST (api_pesquisa.php)**
- Endpoint que recebe termo de pesquisa via GET
- Retorna dados em formato JSON
- Segurança com prepared statements
- Validação de inputs (mínimo 2 caracteres)
- Proteção contra SQL Injection

#### 3. **Campo Placa Gráfica**
- Adicionado campo `placa_grafica` à tabela
- Exibição no detalhe de cada computador
- Informação sobre GPU de todos os equipamentos

---

## 🤖 Utilização da Inteligência Artificial (IA)

### 🔹 Onde utilizei IA

Durante o desenvolvimento deste projeto, utilizei Inteligência Artificial (Claude AI) nas seguintes áreas:

1. **Apoio na escrita e correção de código PHP**
   - Estruturação das queries SQL com PDO
   - Implementação de prepared statements para segurança
   - Organização do código com comentários explicativos

2. **Desenvolvimento da estrutura da base de dados**
   - Sugestões para relacionamentos entre tabelas
   - Otimização das queries SQL
   - Normalização da base de dados

3. **Implementação do sistema de pesquisa AJAX**
   - Arquitetura cliente-servidor
   - API RESTful em PHP
   - JavaScript assíncrono com fetch()
   - Debounce para otimização

4. **Melhoria do interface gráfico (CSS/Layout)**
   - Implementação do design futurista
   - Sistema de cores e gradientes
   - Animações e transições suaves
   - Responsividade para diferentes dispositivos

5. **Organização do dashboard**
   - Criação das estatísticas por sala
   - Sistema de navegação por abas
   - Layout da tabela de listagem

6. **Resolução de erros e problemas técnicos**
   - Debug de problemas de conexão à base de dados
   - Correção de erros de sintaxe PHP e JavaScript
   - Otimização do código

### 🔹 Como utilizei a IA

**Metodologia de trabalho:**

1. **Análise e Planeamento**
   - Apresentei o objetivo do projeto à IA
   - Recebi sugestões de estrutura e organização
   - Validei as propostas e escolhi as mais adequadas

2. **Desenvolvimento Iterativo**
   - A IA forneceu código base funcional
   - Solicitei ajustes e personalizações específicas
   - Testei as funcionalidades e reportei problemas
   - A IA corrigiu e melhorou o código

3. **Refinamento e Personalização**
   - Pedi alterações específicas (cores, layout, funcionalidades)
   - A IA adaptou o código às minhas necessidades
   - Implementei as versões finais no servidor

4. **Aprendizagem Contínua**
   - Cada sugestão da IA vinha com explicações
   - Aprendi através dos comentários no código
   - Consegui compreender o funcionamento de cada parte

**Exemplo concreto - Sistema de Pesquisa AJAX:**

A IA ajudou-me a implementar o sistema de pesquisa dinâmica explicando:
- Como funciona o AJAX e a comunicação assíncrona
- Porque usar debounce (evitar sobrecarga do servidor)
- Como prevenir SQL Injection com prepared statements
- Como escapar HTML para prevenir ataques XSS
- Navegação por teclado para melhor UX

```javascript
// Debounce: espera 300ms após parar de escrever
input.addEventListener('input', () => {
  clearTimeout(debounceTimer);
  debounceTimer = setTimeout(() => fetchResults(q), 300);
});
```

---

## ✍️ Trabalho Desenvolvido Manualmente

Apesar do apoio da IA, várias partes do projeto foram desenvolvidas ou adaptadas por mim:

### 🔧 Adaptações e Personalizações

1. **Configuração do ambiente**
   - Setup do hosting InfinityFree
   - Configuração da base de dados MySQL
   - Upload e organização dos ficheiros no servidor

2. **Decisões de design**
   - Escolha do tema de cores (azul/cyan futurista)
   - Decisão sobre layout e organização da informação
   - Simplificações e ajustes de UX

3. **Testes e validação**
   - Testei todas as funcionalidades no ambiente real
   - Verifiquei a responsividade em diferentes dispositivos
   - Validei a ligação à base de dados

4. **Inserção de dados**
   - Populei a base de dados com informações reais dos computadores
   - Organizei os equipamentos por salas
   - Registei as especificações técnicas

5. **Ajustes finais**
   - Correção de pequenos bugs visuais
   - Melhorias de usabilidade
   - Otimização do carregamento das páginas

---

## 🚧 Dificuldades Encontradas

Durante o desenvolvimento do projeto, encontrei algumas dificuldades:

### 1. **Configuração inicial do ambiente**
- **Dificuldade:** Configurar corretamente as credenciais da base de dados no InfinityFree
- **Solução:** Com ajuda da IA, compreendi a estrutura do ficheiro config.php e ajustei os parâmetros

### 2. **Compreensão do AJAX e comunicação assíncrona**
- **Dificuldade:** No início, não percebia bem como funcionava a comunicação cliente-servidor sem recarregar a página
- **Solução:** A IA explicou passo a passo o fluxo de dados e forneceu exemplos práticos

### 3. **SQL Injection e segurança**
- **Dificuldade:** Compreender a importância dos prepared statements
- **Solução:** Aprendi sobre ataques SQL Injection e como preveni-los

### 4. **Design responsivo**
- **Dificuldade:** Fazer o site funcionar bem em dispositivos móveis
- **Solução:** Aprendi sobre media queries e como adaptar o layout

### 5. **Debounce e otimização**
- **Dificuldade:** Evitar fazer muitos pedidos ao servidor durante a pesquisa
- **Solução:** Implementei debounce com setTimeout() para aguardar 300ms

---

## 📚 Aprendizagens Realizadas

Este projeto foi muito enriquecedor e permitiu-me desenvolver várias competências:

### 💡 Competências Técnicas

1. **PHP e Bases de Dados**
   - Compreendi como fazer a ligação entre PHP e MySQL usando PDO
   - Aprendi a importância dos prepared statements para segurança
   - Percebi como organizar código PHP de forma limpa e legível

2. **SQL**
   - Domínio de queries básicas (SELECT, WHERE, JOIN)
   - Compreensão de relações entre tabelas (1:N, N:M)
   - Organização de dados em estruturas relacionais

3. **JavaScript e AJAX**
   - Comunicação assíncrona com fetch()
   - Manipulação do DOM
   - Event listeners e programação orientada a eventos
   - Técnicas de otimização (debounce)

4. **Frontend**
   - Desenvolvimento de interfaces modernas com CSS puro
   - Técnicas de design futurista
   - Animações e transições CSS
   - Design responsivo com media queries

5. **APIs RESTful**
   - Criação de endpoints
   - Formato JSON para troca de dados
   - Validação de inputs
   - Códigos de status HTTP

### 🧠 Competências Transversais

1. **Utilização consciente da IA**
   - Aprendi a formular perguntas claras à IA
   - Compreendi que devo validar e adaptar as sugestões recebidas
   - Percebi a importância de entender o código, não apenas copiá-lo

2. **Resolução de problemas**
   - Desenvolvimento de pensamento lógico
   - Capacidade de debug e correção de erros
   - Persistência na procura de soluções

3. **Documentação**
   - Importância de comentar o código
   - Criação de documentação clara (este README)
   - Organização da informação de forma estruturada

4. **Gestão de projeto**
   - Planeamento de funcionalidades
   - Priorização de tarefas
   - Iteração e melhoria contínua

### 🎯 Reflexão Final

Este projeto foi a minha primeira experiência séria com desenvolvimento web full-stack e AJAX. 

**O que correu bem:**
- Consegui criar uma aplicação funcional e visualmente apelativa
- Implementei com sucesso um sistema de pesquisa em tempo real
- A utilização da IA acelerou muito o desenvolvimento
- Aprendi conceitos que vou usar em projetos futuros

**O que posso melhorar:**
- Aprofundar conhecimentos de segurança web
- Explorar frameworks PHP (Laravel, Symfony)
- Implementar mais funcionalidades avançadas
- Melhorar a gestão de estado em aplicações AJAX

**Importância da IA:**
A IA foi uma ferramenta essencial, mas percebi que **não substitui o conhecimento**. É necessário:
- Compreender o código gerado
- Ser capaz de adaptar e personalizar
- Tomar decisões informadas sobre o projeto
- Testar e validar todas as funcionalidades

Esta experiência preparou-me para projetos futuros mais complexos e deu-me confiança para continuar a aprender programação web.

---

## 🔗 Repositório GitHub

Link para o repositório do projeto: [https://github.com/a14768-oficina/m6-inventario](https://github.com/a14768-oficina/m6-inventario)

---

## 👨‍💻 Autor

**Afonso Almeida**  
Turma 2ºI – GPSI  
Ano Letivo 2024/2025

---

*Documentação criada com auxílio de Inteligência Artificial (Claude AI)*
