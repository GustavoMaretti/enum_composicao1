# Gerenciamento de Contratos de Trabalho

## Funcionalidades
- Criar e gerenciar um sistema de contratos de trabalho com as seguintes opções:
  - Registro de funcionários com:
    - **Nome**: Nome do funcionário.
    - **Nível**: Classificação do funcionário como Júnior, Pleno ou Sênior.
    - **Salário Base**: Remuneração fixa do funcionário.
    - **Departamento**: Área de atuação do funcionário.
  - Registro de contratos por hora:
    - **Data**: Data de início do contrato.
    - **Valor por Hora**: Remuneração por cada hora trabalhada.
    - **Duração**: Tempo total do contrato em horas.
  - Cálculo da remuneração mensal considerando:
    - Salário base.
    - Valor total dos contratos realizados no mês selecionado.

## Uso
- O programa solicita ao usuário, via console:
  - Nome do departamento.
  - Dados do funcionário (Nome, Nível e Salário Base).
  - Número de contratos a serem adicionados ao funcionário.
  - Dados de cada contrato (Data, Valor por Hora e Duração).
  - Mês e ano para cálculo da remuneração total.
- O programa exibe automaticamente os dados do funcionário e sua remuneração no formato:
  - `Nome, Departamento, Renda Total do Mês`.

## Estrutura

### Classe `Worker`
- **Propriedades**:
  - `Name`: Nome do funcionário.
  - `Level`: Nível do funcionário (Júnior, Pleno ou Sênior).
  - `BaseSalary`: Salário fixo do funcionário.
  - `Department`: Departamento ao qual o funcionário pertence.
  - `Contracts`: Lista de contratos associados ao funcionário.
- **Construtor**:
  - Inicializa as propriedades `Name`, `Level`, `BaseSalary` e `Department`.
- **Métodos**:
  - `AddContract()`: Adiciona um contrato ao funcionário.
  - `RemoveContract()`: Remove um contrato do funcionário.
  - `Income()`: Calcula a remuneração total do funcionário para um mês e ano específicos.

### Classe `HourContract`
- **Propriedades**:
  - `Date`: Data do contrato.
  - `ValuePerHour`: Valor recebido por cada hora trabalhada.
  - `Hours`: Duração do contrato em horas.
- **Métodos**:
  - `TotalValue()`: Calcula o valor total do contrato.

### Classe `Department`
- **Propriedade**:
  - `Name`: Nome do departamento.

### Programa Principal
- **Processos**:
  - Recebe os dados do usuário e cria instâncias das classes `Worker`, `Department` e `HourContract`.
  - Utiliza laços de repetição para adicionar contratos ao funcionário.
  - Realiza cálculos de renda com base nos dados inseridos.
- **Saída**:
  - Exibe os dados atualizados do funcionário e sua renda total para o mês informado.
