# 📃 Requisitos do Sistema

## ✅ Requisitos Funcionais (RF)

## 1. Gerenciamento de Contas 

### 1.1. Cadastro de Cidadãos

- **RF-001:** O sistema deve permitir o cadastro de um novo usuário.
- **RF-002:** O sistema deve validar as entradas do cadastro, segundo a **RN-003** e a **RN-004**, informando ao usuário todos os erros de entrada. Qualquer qubra dessas regras deve ipossibilitar o cadastro do usuário.
- **RF-003:** O sistema deve confirmar a veracidade das informações do usuário com um código de validação enviado via email e/ou SMS. Caso o código de validação não seja equivalente ao enviado, o sistema deve impossibilitar o cadastro, informando ao usuário.

#### 1.2. Cadastro de Órgãos
- **RF-004:** O sistema deve permitir o cadastro de um novo Órgão público ou privado.
- **RF-005:** 
- **RF-006:** 

### 1.3. Autenticação

- **RF-007:** O sistema deve permitir que o usuário faça login utilizando a conta do gov.br.
- **RF-008:** O sistema deve encerrar automaticamente sessões inativas após 15 minutos de inatividade.
- **RF-010:** O sistema deve permitir login simultâneo em no máximo um dispositivo por vez para cidadãos.
- **RF-011:** O sistema deve bloquear tentativas de login após 5 falhas consecutivas por 15 minutos.
- **RF-012:** O sistema deve enviar uma mensagem ao email cadastrado após 5 tentativas falhas.
- **RF-013:** O sistema deve registrar logs de autenticação com data, hora e IP de origem.

### 1.4. Gerenciamento de Perfil

- **RF-009:** O sistema deve permitir a edição dos dados de qualquer usuário, somente pelo próprio usuário autenticado, desde que não infrinja a regra de negócio **RN-005**.
- **RF-010:** O sistema deve permitir a desativação de órgãos - tanto pelo administrador, quanto pelo próprio órgão, desde que siga a **RN-011** -, impedindo o recebimento de novas denúncias.
- **RF-011:** O sistema deve permitir a redefinição de senha para usuários com e-mail cadastrado, segundo a **RN-006**.
- **RF-012:** 



## 2. Denúncia

### 2.1. 

### 2.2. 


## 3. Relatório


## 4. Feedback


## 5. 

### 5.1.

### 5.2. 
