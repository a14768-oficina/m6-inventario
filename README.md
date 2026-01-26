
📊 Inventário de Computadores – Aplicação Web (PHP + SQL)
👤 Identificação

Nome do aluno: Afonso Almeida
Turma: 2ºI
Disciplina: REDES – M6 – Programação de Sistemas de Informação
Curso: GPSI – 2.º Ano


🎯 Objetivo do Projeto
Este projeto consiste no desenvolvimento de uma aplicação web para gestão e consulta de um inventário de computadores de uma sala informática, utilizando PHP para a lógica da aplicação e SQL para a base de dados.
A aplicação permite:

Consultar informações técnicas dos computadores
Visualizar o software instalado em cada equipamento
Organizar os equipamentos por salas
Aceder a detalhes completos de cada computador

🔗 Relações entre Tabelas

Salas ↔ Computadores: Relação 1:N (uma sala pode ter vários computadores)
Computadores ↔ Software: Relação N:M através da tabela computador_software


⚙️ Funcionalidades Desenvolvidas
Lista das funcionalidades implementadas no projeto:

 Ligação à base de dados com PHP (PDO)
 Listagem de computadores por sala
 Visualização das características técnicas de cada computador
 Consulta do software instalado
 Página de detalhes por computador
 Organização do dashboard com estatísticas por sala
 Melhorias visuais no interface (tema cinzento/branco/preto, glassmorphism)
 Sistema de navegação por abas (filtro por salas)
 Design responsivo (adaptado para mobile)
 Animações e efeitos visuais modernos
 Pesquisa por nome de computador (funcionalidade futura)
 Sistema de autenticação (funcionalidade futura)

📸 Capturas de Ecrã
Página Principal (index.php)

Dashboard com estatísticas de computadores por sala
Sistema de navegação por salas
Listagem completa dos equipamentos
Design moderno com tema escuro

Página de Detalhes (detalhe.php)

Especificações técnicas completas do computador
Interface estilo HUD (Heads-Up Display)
Informações organizadas de forma clara


🤖 Utilização da Inteligência Artificial (IA)
🔹 Onde utilizei IA
Durante o desenvolvimento deste projeto, utilizei Inteligência Artificial (Claude AI) nas seguintes áreas:

Apoio na escrita e correção de código PHP

Estruturação das queries SQL com PDO
Implementação de prepared statements para segurança
Organização do código com comentários explicativos


Desenvolvimento da estrutura da base de dados

Sugestões para relacionamentos entre tabelas
Otimização das queries SQL
Normalização da base de dados


Melhoria do interface gráfico (CSS/Layout)

Implementação do design com glassmorphism
Sistema de cores e gradientes
Animações e transições suaves
Responsividade para diferentes dispositivos


Organização do dashboard

Criação das estatísticas por sala
Sistema de navegação por abas
Layout da tabela de listagem


Resolução de erros e problemas técnicos

Debug de problemas de conexão à base de dados
Correção de erros de sintaxe PHP
Otimização do código


Personalização do tema visual

Adaptação do tema de cores original (azul/cyan) para cinzento/branco/preto
Ajuste de contrastes e legibilidade
Remoção de elementos não necessários



🔹 Como utilizei a IA
Metodologia de trabalho:

Análise e Planeamento

Apresentei o objetivo do projeto à IA
Recebi sugestões de estrutura e organização
Validei as propostas e escolhi as mais adequadas


Desenvolvimento Iterativo

A IA forneceu código base funcional
Solicitei ajustes e personalizações específicas
Testei as funcionalidades e reportei problemas
A IA corrigiu e melhorou o código


Refinamento e Personalização

Pedi alterações específicas (cores, layout, funcionalidades)
A IA adaptou o código às minhas necessidades
Implementei as versões finais no servidor


Aprendizagem Contínua

Cada sugestão da IA vinha com explicações
Aprendi através dos comentários no código
Consegui compreender o funcionamento de cada parte



Exemplo concreto:
php// Código sugerido pela IA com explicações detalhadas
$query = $pdo->prepare("SELECT c.*, s.nome_sala 
                        FROM computadores c 
                        JOIN salas s ON c.id_sala = s.id_sala 
                        WHERE c.id_sala = :sala_id");
$query->execute(['sala_id' => $sala_selecionada]);
A IA não apenas forneceu o código, mas explicou:

Porquê usar prepared statements (segurança contra SQL injection)
Como funciona o JOIN entre tabelas
A importância de filtrar por sala


✍️ Trabalho Desenvolvido Manualmente
Apesar do apoio da IA, várias partes do projeto foram desenvolvidas ou adaptadas por mim:
🔧 Adaptações e Personalizações

Configuração do ambiente

Setup do hosting InfinityFree
Configuração da base de dados MySQL
Upload e organização dos ficheiros no servidor


Decisões de design

Escolha do tema de cores (cinzento/branco/preto)
Decisão de remover a secção de software da página de detalhes
Simplificação do texto do botão "VOLTAR"


Testes e validação

Testei todas as funcionalidades no ambiente real
Verifiquei a responsividade em diferentes dispositivos
Validei a ligação à base de dados


Inserção de dados

Populei a base de dados com informações reais dos computadores
Organizei os equipamentos por salas
Registei as especificações técnicas


Ajustes finais

Correção de pequenos bugs visuais
Melhorias de usabilidade
Otimização do carregamento das páginas



💭 Decisões Técnicas

Hosting escolhido: InfinityFree (gratuito, suporta PHP e MySQL)
Framework CSS: Nenhum – CSS puro personalizado
Segurança: Uso de PDO com prepared statements
Organização: Separação clara entre configuração, lógica e apresentação


🚧 Dificuldades Encontradas
Durante o desenvolvimento do projeto, encontrei algumas dificuldades:
1. Configuração inicial do ambiente

Dificuldade: Configurar corretamente as credenciais da base de dados no InfinityFree
Solução: Com ajuda da IA, compreendi a estrutura do ficheiro config.php e ajustei os parâmetros

2. Compreensão das queries SQL com JOIN

Dificuldade: No início, não percebia bem como funcionavam os JOINs entre tabelas
Solução: A IA explicou passo a passo e forneceu exemplos práticos

3. Design responsivo

Dificuldade: Fazer o site funcionar bem em dispositivos móveis
Solução: Aprendi sobre media queries e como adaptar o layout

4. Gestão de sessões e filtros

Dificuldade: Implementar o filtro por salas mantendo o estado selecionado
Solução: Utilizei parâmetros GET no URL e validação com PHP

5. Personalização visual

Dificuldade: Adaptar o código CSS para o tema que queria
Solução: Com orientação da IA, identifiquei todas as variáveis de cor e alterei sistematicamente


📚 Aprendizagens Realizadas
Este projeto foi muito enriquecedor e permitiu-me desenvolver várias competências:
💡 Competências Técnicas

PHP e Bases de Dados

Compreendi como fazer a ligação entre PHP e MySQL usando PDO
Aprendi a importância dos prepared statements para segurança
Percebi como organizar código PHP de forma limpa e legível


SQL

Domínio de queries básicas (SELECT, WHERE, JOIN)
Compreensão de relações entre tabelas (1:N, N:M)
Organização de dados em estruturas relacionais


Frontend

Desenvolvimento de interfaces modernas com CSS puro
Técnicas de glassmorphism e gradientes
Animações e transições CSS
Design responsivo com media queries


Arquitetura Web

Separação de responsabilidades (config, lógica, apresentação)
Fluxo de dados entre páginas
Gestão de estado com GET/POST



🧠 Competências Transversais

Utilização consciente da IA

Aprendi a formular perguntas claras à IA
Compreendi que devo validar e adaptar as sugestões recebidas
Percebi a importância de entender o código, não apenas copiá-lo


Resolução de problemas

Desenvolvimento de pensamento lógico
Capacidade de debug e correção de erros
Persistência na procura de soluções


Documentação

Importância de comentar o código
Criação de documentação clara (este README)
Organização da informação de forma estruturada


Gestão de projeto

Planeamento de funcionalidades
Priorização de tarefas
Iteração e melhoria contínua



🎯 Reflexão Final
Este projeto foi a minha primeira experiência séria com desenvolvimento web full-stack.
O que correu bem:

Consegui criar uma aplicação funcional e visualmente apelativa
A utilização da IA acelerou muito o desenvolvimento
Aprendi conceitos que vou usar em projetos futuros

O que posso melhorar:

Aprofundar conhecimentos de segurança web
Explorar frameworks PHP (Laravel, Symfony)
Implementar funcionalidades mais avançadas (pesquisa, autenticação)

Importância da IA:
A IA foi uma ferramenta essencial, mas percebi que não substitui o conhecimento. É necessário:

Compreender o código gerado
Ser capaz de adaptar e personalizar
Tomar decisões informadas sobre o projeto

Esta experiência preparou-me para projetos futuros mais complexos e deu-me confiança para continuar a aprender programação web.
🔗 Links Úteis

Aplicação Online: https://a14768-oficina.infinityfree.me/m6-inventario/index.php


📄 Licença
Este projeto foi desenvolvido para fins educativos no âmbito da disciplina de REDES do curso GPSI.

👨‍💻 Autor
Afonso Almeida
Turma 2ºI – GPSI
Ano Letivo 2025/2026
