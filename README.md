# Agente de Agendamento para Salão de Beleza

Este projeto é um agente automatizado para facilitar o agendamento de serviços em salões de beleza. Ele é integrado à plataforma [cal.com](https://cal.com), permitindo consultas de horários disponíveis e criação de reservas de maneira prática e eficiente.

---

## 📝 Funcionalidades

- **Consulta de horários disponíveis**: Verifica as janelas de tempo disponíveis no sistema para um período especificado.
- **Criação de agendamentos**: Realiza reservas diretamente no sistema, coletando informações como nome, telefone e email do cliente.
- **Interação humanizada**: Respostas diretas, informais e acessíveis para melhorar a experiência do usuário.
- **Validação de dados**: Garante que os dados fornecidos, como email e telefone, estejam em formatos válidos.
- **Consulta de preços**: Busca os valores de serviços em arquivos externos.

---

## 🚀 Como Funciona

### 1. **Início da Conversa**
   O agente se apresenta e pergunta qual serviço o cliente deseja agendar.

### 2. **Consulta de Preço**
   Com base no serviço escolhido, o agente consulta o preço em um arquivo externo (ex.: `preco.pdf`) e informa ao cliente.

### 3. **Coleta de Informações**
   - Nome do cliente.
   - Telefone (formato padrão brasileiro).
   - Email (validado).

### 4. **Consulta de Disponibilidade**
   O cliente informa um período desejado (ex.: "amanhã à tarde") e o agente consulta os horários disponíveis usando a função `pegarslots`.

### 5. **Escolha do Horário**
   O cliente seleciona um dos horários disponíveis.

### 6. **Confirmação do Agendamento**
   O agente cria o agendamento no sistema com a função `criar_agendamento_cal_com` e confirma o sucesso ao cliente.

---

## 🛠️ Endpoints Utilizados

### **Consultar Horários Disponíveis**
**Função**: `pegarslots`  
**Parâmetros**:
- `startTime`: Data e hora inicial no formato UTC-4.
- `endTime`: Data e hora final no formato UTC-4.

### **Criar Agendamento**
**Função**: `criar_agendamento_cal_com`  
**Parâmetros**:
- `startTime`: Data e hora do agendamento (UTC-4).
- `nome`: Nome do cliente.
- `telefone`: Telefone do cliente.
- `email`: Email do cliente.

---

## 🔄 Fluxo de Uso

1. **Entrada do Cliente**: O cliente interage informando o serviço desejado.
2. **Busca de Preço**: O agente encontra e retorna o preço do serviço.
3. **Coleta de Dados**: Informações pessoais e preferências de horário.
4. **Consulta e Confirmação**: O agente verifica horários disponíveis, realiza a reserva e confirma.

---

## 📦 Variáveis de Saída

| Variável      | Descrição                                  |
|---------------|--------------------------------------------|
| `nome`        | Nome do cliente.                          |
| `telefone`    | Telefone validado do cliente.             |
| `email`       | Email validado do cliente.                |
| `dia_horario` | Data e hora escolhida para o agendamento. |
| `servico`     | Serviço desejado pelo cliente.            |
| `preco`       | Preço do serviço escolhido.               |

---

## 🛡️ Pré-requisitos

- Conta ativa na [cal.com](https://cal.com).
- Arquivo com os preços dos serviços (ex.: `preco.pdf`).
- Ambiente configurado para execução do agente.
- possuir o evolution instalado e configurado.

---

## ⚙️ Configuração

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/agendamento-salao-beleza.git
   cd agendamento-salao-beleza


Configure as credenciais para acesso à API do cal.com.

Certifique-se de que o arquivo preco.pdf esteja no diretório correto.

Execute o agente no ambiente desejado.

🤝 Contribuição

Contribuições são bem-vindas! Para sugestões ou melhorias, abra uma issue ou envie um pull request.
📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.




