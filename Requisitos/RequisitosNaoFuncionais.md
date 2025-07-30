# 📃 Requisitos do Sistema

## :ballot_box_with_check: Requisitos Não Funcionais (RNF)

# 1. Usabilidade
   
## 1.1. Acessibilidade

- RNF-001: O sistema deve ser compatível com tecnologias assistivas, como leitores de tela, e estar em conformidade com as diretrizes WCAG 2.1.
- RNF-002: O sistema deve oferecer configurações de acessibilidade ajustáveis pelo usuário, como aumento de fonte, contraste de cores e ativação de leitura de texto.
- RNF-003: O sistema deve suportar navegação apenas por teclado, sem dependência de mouse ou toques em tela.

## 1.2. Facilidade de Uso

- RNF-004: A interface do sistema deve ser intuitiva, com menus e ações organizados de forma a facilitar o uso por qualquer perfil de cidadão.
- RNF-005: As instruções de uso e feedbacks do sistema devem ser claros e objetivos, sem uso de linguagem técnica.

## 1.3. Responsividade

- RNF-006: O sistema deve funcionar corretamente em diferentes dispositivos (computadores, tablets e smartphones), com layout responsivo adaptado para cada resolução.
- RNF-007: A interface deve ser testada e validada nos navegadores mais utilizados (Chrome, Firefox, Edge e Safari).

## 1.4. Internacionalização

- RNF-008: O sistema deve oferecer suporte multilíngue, inicialmente em português e inglês, com possibilidade de expansão para outros idiomas.

# 2. Segurança

## 2.1. Segurança da Informação

-RNF-009: Todos os dados sensíveis devem ser criptografados em repouso utilizando algoritmos fortes como AES-256.
- RNF-010: A comunicação entre cliente e servidor deve utilizar criptografia de ponta a ponta, com protocolo TLS 1.3 ou superior.
- RNF-011: O sistema deve realizar verificação de integridade e validade dos dados transmitidos.

## 2.2. Confiabilidade e Disponibilidade

- RNF-012: O sistema deve ter disponibilidade mínima de 99,5%, com suporte a recuperação rápida em caso de falha.
- RNF-013: O sistema deve estar preparado para operar com, no mínimo, 1000 denúncias simultâneas, sem perda de desempenho ou consistência.
- RNF-014: A autenticação dos usuários deve ser realizada por meio da plataforma gov.br, com garantia de segurança e conformidade com as normas do governo federal.

## 2.3. Auditabilidade

-RNF-015: Todas as ações sensíveis (denúncia, edição, exclusão, atribuição de protocolo, etc.) devem ser registradas em logs auditáveis com data, hora, IP e usuário.
- RNF-016: Os logs do sistema devem ser armazenados de forma segura e protegidos contra alterações.

# 3. Desempenho e Escalabilidade

## 3.1. Tempo de Resposta

- RNF-017: O sistema deve apresentar tempo de resposta inferior a 2 segundos para as principais funcionalidades (envio de denúncia, consulta, resposta).
- RNF-018: Operações de leitura e escrita em banco de dados devem ser otimizadas para alto volume de acesso simultâneo.

## 3.2. Capacidade de Processamento

- RNF-019: O sistema deve permitir, no mínimo, o envio simultâneo de 1000 denúncias sem comprometer a integridade ou disponibilidade dos dados.
- RNF-020: O sistema deve passar por testes de carga e stress periodicamente, garantindo sua escalabilidade horizontal quando necessário.

# 4. Manutenibilidade

## 4.1. Reusabilidade

- RNF-021: O código do sistema deve ser estruturado em componentes reutilizáveis, facilitando a replicação de funcionalidades comuns.

## 4.2. Modificabilidade

- RNF-022: A arquitetura deve permitir atualizações independentes por módulo, com mínimo impacto em outras funcionalidades.
- RNF-023: Toda modificação no sistema deve ser documentada, versionada e validada com testes.

## 4.3. Testabilidade

- RNF-024: O sistema deve conter cobertura mínima de 80% de testes automatizados (unitários e de integração).
- RNF-025: As funcionalidades críticas devem possuir testes de regressão para evitar falhas recorrentes.

# 5. Portabilidade

## 5.1. Compatibilidade com Ambientes

- RNF-026: O sistema deve ser compatível com os principais sistemas operacionais (Windows, Linux, Android e iOS).
- RNF-027: O sistema deve ser capaz de ser executado em ambientes de nuvem, servidores on-premise ou híbridos.

## 5.2. Adaptabilidade

- RNF-028: O sistema deve oferecer recursos para ser configurado em diferentes contextos, como municípios, órgãos públicos ou empresas privadas.

## 5.3. Tolerância a Formatos Diversos

- RNF-029: O sistema deve aceitar o anexo de arquivos nas denúncias, suportando extensões como: .pdf, .png, .jpg, .docx, .mp4 e outros formatos amplamente utilizados.

- RNF-030: O limite de tamanho de arquivos anexados deve ser parametrizável e o usuário deve ser informado ao ultrapassá-lo.

# 6. Pesquisa e Filtros

## 6.1. Funcionalidade de Pesquisa

- RNF-031: O sistema deve permitir a aplicação de filtros nas denúncias por: data de criação, tipo de denúncia, órgão responsável e localidade.

- RNF-032: Os filtros devem retornar os resultados em até 2 segundos para conjuntos com até 1000 registros.

- RNF-033: O sistema deve permitir a combinação de filtros de forma intuitiva, com possibilidade de limpeza rápida dos mesmos.
