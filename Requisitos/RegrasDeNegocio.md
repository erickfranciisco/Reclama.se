# 📃 Requisitos do Sistema

## 🧑‍💼 Regras de Negócio (RN)

## 1. Regras de Usuários

### 1.1. Tipos de Usuário

A plataforma terá três tipos de usuários principais:

- **Cidadão:** Pessoa física ou jurídica que reportará uma denúncia específica.
- **Órgão:** Órgão público ou privado que presta serviços públicos. Aquele que será acionado após a denúncia. 
- **Moderador:** Agente do Reclama.se responsável pela gestão da plataforma.

### 1.2. Cidadão

- RN-001: A autenticação é obrigatória para utilização do sistema.
- RN-002: Cada cidadão deve possuir apenas um único CPF ou CNPJ - no caso de pessoa jurídica - válido cadastrado.
- RN-003: A autenticação deve ser realizada via gov.br

### 1.3. Órgão Responsável

- RN-004: Um órgão só pode ser cadastrado por usuários com perfil de administrador autorizado.
- RN-005: Cada órgão deve possuir um CNPJ válido e único no sistema.
- RN-006:Cada órgão deve possuir os seguintes dados obrigatórios:.
  - Nome da instituição;
  - CNPJ;
  - E-mail institucional;
  - Telefone de contato;
  - Responsável institucional (nome completo e CPF);
  - Setores atendidos (área de atuação);
  - Endereço completo com UF e Município.
- RN-007: Os dados do responsável institucional devem ser protegidos e não devem ser acessíveis.
- RN-008: O órgão será automaticamente notificado sempre que receber uma nova denúncia atribuída a ele.
- RN-009: O órgão deve ser capaz de atualizar suas informações cadastrais, desde que autorizado e com autenticação segura.
- RN-010: O sistema deve manter um histórico versionado das alterações cadastrais dos órgãos responsáveis, com data, autor da alteração e conteúdo antigo/novo.
  
---

## 2. Regras de Denúncia

### 2.1. Registro de Denúncia 

- RN-011: O cidadão só poderá registrar denúncias se estiver autenticado e cadastrado.
- RN-012: Cada denúncia deve conter os seguites dados básicos:.
  - Título;
  - Data/Hora;
  - Descrição (definido pelo cidadão);
  - Tipo;
  - Status;
  - Setores atendidos (área de atuação);
  - Endereço completo com UF e Município.
- RN-013: Após o envio da denúncia realizada pelo cidadão, ela será direcionada para o serviço de moderação da plataforma, na qual será responsável por avaliar se o conteúdo da denúncia está de acordo com as diretrizes.
- RN-014: Uma denúncia só poderá ser respondida pelo Órgão Responsável, se já estiver avaliada positivamente pelo serviço de moderação.   
- RN-015: O sistema deve manter os dados do cidadão (o denunciante) totalmente ocultos - sem exibição para o público ou para os órgãos - tanto na plataforma, quanto nas mídias enviadas por ela, mesmo que a publicação da denúncia seja autorizada após a etapa de moderação mencionado na RN-013.
- RN-016: Após a denúncia, o usuário deve receber uma confirmação automática e um número de protocolo.
- RN-017: Caso as publicações realizadas pelos usuários (cidadãos e/ou órgãos) não estejam de acordo com as diretrizes, o serviço de moderção deve ter a permissão de editar ou excluir as publicações.
- RN-018: Condições que impedem um denúncia de ser cancelada:.
  - Respondida pelo órgão responsável;
  - Status definido como "Em_Solução" ou "Solucionado";
  - Status definido como "Bloqueada", uma vez que sua visibilidade foi reduzida. 

### 2.2. Visibilidade da Denúncia

- RN-019: Denúncias que com o status de "Bloqueada", não devem ser excluídas permanentemente do sistema. Todas as denúncias com esse status devem ter somente sua visibilidade bloqueada para os seguintes usuários: órgãos, cidadãos.
- RN-020: Denúncias que com o status de "Cancelada", não podem ser visíveis por nenhum usuário, a não ser seu autor.

### 2.3. Ciclo de Vida da Denúncia

A denúncia terá os seguintes status:

1.  **Publicada:** Denúncia enviada pelo cidadão. Visível para todos os usuários.
2.  **Aprovada:** A denúncia não infligiu nenhuma diretriz, segundo o processo de aprovação pelo serviço de moderação.
3.  **Editada:** A denúncia não cumpriu alguma(s) das diretrizes, resultando em sua edição pelos moderadores. 
4.  **Bloqueada (Excluída):** A denúncia não cumpriu alguma(s) das diretrizes, resultando no bloqueio da sua visibilidade após a moderação.
5.  **Em Solução:** A denúncia previamente aprovada, está em proceso de solucionamento. 
6.  **Solucionada:** Os parâmetros apontados na denúncia foram corrigidos pelo serviço público.
7.  **Cancelada:** O cidadão cancela a publicação da denúncia.
8.  **Oculta:** O cidadão oculta a visibilidade de uma denúncia.
9.  **Excluída:** A denúncia é excluída do banco de dados.

---

## 3. Regras de Relatório

### 3.1. Formulação do Relatório 

- RN-021: Após a denúncia, o sistema deve gerar um relatório automaticamente com os dados básicos definidos na RN-012. O relatório deve atender a RN-015 de sigilo e proteção ao cidadão, ocultando sua identidade no relatório.  
-RN-022: O relatório deve ser atualizado automaticamente a cada nova movimentação da denúncia.
- RN-023: O sistema deve impedir qualquer tentativa de manipulação indevida do conteúdo do relatório, garantindo sua integridade.
- RN-024: Cada versão do relatório deve ser versionada e armazenada no banco de dados, com controle de data e responsável pela alteração.
- RN-025: O relatório deve ser enviado automaticamente ao órgão responsável assim que ele for atribuído à denúncia, respeitando as regras de privacidade de dados.

---

## 4. Regras de Feedback

### 4.1. Publicação de Feedback

- RN-026: O sistema deve permitir que o cidadão avalie o atendimento prestado pelo órgão após tempo mínimo de 7 dias corridos da data de publicação da denúncia.
- RN-027: O feedback deve estar vinculado à denúncia original e ser permitido apenas uma vez por denúncia registrada, impossibilitando o cidadão de gerar múltiplas avaliações do mesmo caso.
- RN-028: Um feedback já existente, pode ser editado pelo usuário após atualizações do caso.
- RN-029: Os dados do cidadão (denunciante) devem ser totalmente ocultos durante a descrição do feedback.

### 4.2. Formulação do Feedback

- RN-030: O feedback deve conter os seguintes parâmetros obrigatórios:.
  - Nota de 1 a 5 estrelas (avaliação do atendimento);
  - Descrição textual (máximo de 1024 caracteres);
  - Grau de satisfação geral (Muito insatisfeito a Muito satisfeito).

---
