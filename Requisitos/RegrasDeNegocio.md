# 📃 Requisitos do Sistema

## 🧑‍💼 Regras de Negócio (RN)

## 1. Regras de Usuários

### 1.1. Tipos de Usuário

A plataforma terá três tipos de usuários principais:

- **Cidadão:** Pessoa física ou jurídica que reportará uma denúncia específica.
- **Órgão:** Órgão público ou privado que presta serviços públicos. Aquele que será acionado após a denúncia. 
- **Moderador:** Agente do Reclama.se responsável pela gestão da plataforma.

### 1.2 Cadastro 
- **RN-001:** Somente usuários cadastrados devem possuir acesso as funcionalidades do sistema. 
- **RN-002:** Todo cidadão, para realizar seu cadastro, deve informar obrigatoriamente os seguintes critérios informados:.
  - Nome Completo;
  - CPF ou CNPJ;
  - Email;
  - Telefone;
  - CEP;
  - Senha;
- **RN-003:** Somente email, CPF/CNPJ, CEP e telefone válidos devem ser aceitos e registrados pelo sistema. 
- **RN-004:** CPF/CNPJ devem ser únicos por usuário. 
- **RN-005:** Somente usuários cadastrados e autenticados devem ter permissão para editar/excluir qualquer conteúdo informado ou publicado no sistema.
- **RN-006:** A redefinição de senha só deve ser possível através de uma conta cadastrada e autenticada. Posteriormente, deve-se enviar um emial de alteração de senha para o endereço cadastrado.   

### 1.3. Órgão Responsável

- **RN-007:** Um órgão só pode ser cadastrado por usuários com perfil de administrador autorizado.
- **RN-008:** Cada órgão deve possuir um CNPJ válido e único no sistema.
- **RN-009:** Cada órgão deve possuir os seguintes dados obrigatórios:.
  - Nome da instituição;
  - CNPJ;
  - E-mail institucional;
  - Telefone de contato;
  - Responsável institucional (nome completo e CPF);
  - Setores atendidos (área de atuação);
  - Endereço completo com UF e Município.
- **RN-010:** Os dados do responsável institucional devem ser protegidos e não devem ser acessíveis.
- **RN-011:** O órgão será automaticamente notificado sempre que receber uma nova denúncia atribuída a ele.
- **RN-012:** O órgão deve ser capaz de atualizar suas informações cadastrais, desde que autorizado e com autenticação segura.
- **RN-013:** O sistema deve manter um histórico versionado das alterações cadastrais dos órgãos responsáveis, com data, autor da alteração e conteúdo antigo/novo.
- **RN-014:** O órgão pode requerir sua desativação de conta, o que será encaminhado para o serviço de moderação.
  
---

## 2. Regras de Denúncia

### 2.1. Registro de Denúncia 

- **RN-015:** O cidadão só poderá registrar denúncias se estiver autenticado e cadastrado.
- **RN-016:** Cada denúncia deve conter os seguites dados básicos:.
  - Título;
  - Data/Hora;
  - Descrição definida pelo cidadão (máximo de 1024 caracteres);
  - Evidências (arquivos de mídia diversas);
  - Tipo;
  - Status;
  - Setores atendidos (área de atuação);
  - Endereço completo com UF e Município;
- **RN-017:** Após o envio da denúncia realizada pelo cidadão, ela será direcionada para o serviço de moderação da plataforma, na qual será responsável por avaliar se o conteúdo da denúncia está de acordo com as diretrizes.
- **RN-018:** Uma denúncia só poderá ser respondida pelo Órgão Responsável, se já estiver avaliada positivamente pelo serviço de moderação.   
- **RN-019:** O sistema deve manter os dados do cidadão (o denunciante) totalmente ocultos - sem exibição para o público ou para os órgãos - tanto na plataforma, quanto nas mídias enviadas por ela, mesmo que a publicação da denúncia seja autorizada após a etapa de moderação mencionado na **RN-017**.
- **RN-020:** Após a denúncia, o usuário deve receber uma confirmação automática e um número de protocolo.
- **RN-021:** Caso as publicações realizadas pelos usuários (cidadãos e/ou órgãos) não estejam de acordo com as diretrizes, o serviço de moderção deve ter a permissão de editar ou excluir as publicações.
- **RN-022:** Condições que impedem um denúncia de ser cancelada:.
  - Respondida pelo órgão responsável;
  - Status definido como "Em_Solução" ou "Solucionado";
  - Status definido como "Bloqueada", uma vez que sua visibilidade foi reduzida. 

### 2.2. Visibilidade da Denúncia

- **RN-023:** Denúncias que com o status de "Bloqueada", não devem ser excluídas permanentemente do sistema. Todas as denúncias com esse status devem ter somente sua visibilidade bloqueada para os seguintes usuários: órgãos, cidadãos.
- **RN-024:** Denúncias que com o status de "Cancelada", não podem ser visíveis por nenhum usuário, a não ser seu autor.

### 2.3. Crédito de Denúncia (Abaixo-Assinado)

- **RN-025:** Apenas cidadãos autenticados podem assinar/creditar uma denúncia.
- **RN-026:** O crédito deve ser único, a denúncia só pode ser creditada uma vez por usuário. 
- **RN-027:** O cidadão não pode assinar denúncias de sua própria autoria.
- **RN-028:** As denúncias que possuem os seguintes status **não** devem possuir a opção de crédito: **Oculta**, **Cancelada**, **Excluída**, **Bloqueada**.

### 2.4. Ciclo de Vida da Denúncia

A denúncia terá os seguintes status:

1.  **Publicada:** Denúncia enviada pelo cidadão. Visível para todos os usuários.
2.  **Em Solução:** A denúncia previamente aprovada, está em proceso de solucionamento. 
3.  **Solucionada:** Os parâmetros apontados na denúncia foram corrigidos pelo serviço público.
4.  **Cancelada:** O cidadão cancela a publicação da denúncia.
5.  **Oculta:** O cidadão oculta a visibilidade de uma denúncia.
6.  **Excluída:** A denúncia é excluída do banco de dados.

### 2.5. Status de Avaliação de Denúncia

A avaliação deve seguir os seguintes estados:

1.  **Aprovada:** A denúncia não infligiu nenhuma diretriz, segundo o processo de aprovação pelo serviço de moderação.
2. **Editada:** A denúncia foi aprovada, porém não cumpriu alguma(s) das diretrizes, resultando em sua edição pelos moderadores. 
3. **Bloqueada:** A denúncia não cumpriu alguma(s) das diretrizes, resultando no bloqueio da sua visibilidade após a moderação.

---

## 3. Regras de Relatório

### 3.1. Formulação do Relatório 

- **RN-029:** Após a denúncia, o sistema deve gerar um relatório automaticamente com os dados básicos definidos na **RN-016**. O relatório deve atender a **RN-019** de sigilo e proteção ao cidadão, ocultando sua identidade no relatório.  
- **RN-030:** O relatório deve ser atualizado automaticamente a cada nova movimentação da denúncia.
- **RN-031:** O sistema deve impedir qualquer tentativa de manipulação indevida do conteúdo do relatório, garantindo sua integridade.
- **RN-032:** Cada versão do relatório deve ser versionada e armazenada no banco de dados, com controle de data e responsável pela alteração.
- **RN-033:** O relatório deve ser enviado automaticamente ao órgão responsável assim que ele for atribuído à denúncia, respeitando as regras de privacidade de dados.
- **RN-034:** Caso a denúncia não seja aprovada na avaliação de moderação, o relatório não deve ser exibido ao órgão responsável, além disso deve ser enviado uma notificação de bloqueio de denúncia.
  
---

## 4. Regras de Feedback

### 4.1. Publicação de Feedback

- **RN-035:** O sistema deve permitir que o cidadão avalie o atendimento prestado pelo órgão após tempo mínimo de 7 dias corridos da data de publicação da denúncia.
- **RN-036:** O feedback deve estar vinculado à denúncia original e ser permitido apenas uma vez por denúncia registrada, impossibilitando o cidadão de gerar múltiplas avaliações do mesmo caso.
- **RN-037:** Um feedback já existente, pode ser editado pelo usuário após atualizações do caso.
- **RN-038:** Os dados do cidadão (denunciante) devem ser totalmente ocultos durante a descrição do feedback.

### 4.2. Funcionalidade do Feedback

- **RN-039:** O feedback deve conter os seguintes parâmetros obrigatórios:.
  - Nota de 1 a 5 estrelas (avaliação do atendimento);
  - Descrição textual (máximo de 1024 caracteres);
  - Grau de satisfação geral (Muito insatisfeito a Muito satisfeito).

---

## 5. Pesquisa e Navegação

### 5.1 Denúncias

- **RN-040:** A exibição de outras denúncias publicadas deve priorizar denúncias da mesma localidade (e proximidades) e/ou do mesmo tipo da denúncia visualizada pelo cidadão, em ordem de data/hora mais recente.
- **RN-041:** A pesquisa textual por título deve ser feita com correspondência parcial (contendo as palavras), sem diferenciação de maiúsculas e minúsculas.
- **RN-042:** Filtros de pesquisa ou exibição de denúncias devem possuir no mínimo um dos seguintes parâmetros:.
  - Localidade (UF, cidade ou CEP);
  - Data de Registro;
  - Status;
  - Tipo;
  - Setor Responsável;
  - Órgão;
  - Título;

---

## 6. Regras de Notificação e Comunicação
