# DIO - Trilha .NET - Explorando a Linguagem C#: Sistema de Hospedagem de Hotel

Projeto desenvolvido como parte do desafio de código do módulo **Explorando a Linguagem C#** da trilha .NET da [DIO (Digital Innovation One)](https://www.dio.me/).

---

## 📌 Contexto e Proposta

O objetivo do projeto é construir um sistema de hospedagem para gerenciar reservas de um hotel, integrando hóspedes, suítes e regras de negócio:
- Cadastro de hóspedes e suítes.
- Validação de capacidade da suíte (não permite mais hóspedes do que a capacidade suportada, disparando uma exceção).
- Retorno da quantidade total de hóspedes na reserva.
- Cálculo do valor total da hospedagem com base na diária da suíte e dias reservados.
- **Regra de desconto**: Reservas iguais ou superiores a **10 dias** recebem **10% de desconto** no valor total.

---

## 📐 Diagrama de Classes

![Diagrama de classe hotel](diagrama_classe_hotel.png)

### Principais Classes e Responsabilidades:
- **`Pessoa`**: Representa os dados do hóspede (`Nome`, `Sobrenome`, `NomeCompleto`).
- **`Suite`**: Representa a acomodação (`TipoSuite`, `Capacidade`, `ValorDiaria`).
- **`Reserva`**: Relaciona a suíte e a lista de hóspedes:
  - `CadastrarHospedes(List<Pessoa>)`: Valida se a capacidade é suficiente antes de cadastrar.
  - `CadastrarSuite(Suite)`: Associa a suíte à reserva.
  - `ObterQuantidadeHospedes()`: Retorna o número de hóspedes vinculados.
  - `CalcularValorDiaria()`: Calcula o valor total com aplicação do desconto de 10% para períodos de 10 dias ou mais.

---

## 🛠️ Tecnologias Utilizadas

- **C# / .NET 8**
- **Git & GitHub**

---

## 📂 Estrutura do Projeto

```
trilha-net-explorando-desafio/
├── Models/
│   ├── Pessoa.cs                 # Modelo do hóspede
│   ├── Reserva.cs                # Lógica da reserva, validação e cálculos
│   └── Suite.cs                  # Modelo da suíte
├── DesafioProjetoHospedagem.csproj # Configuração do projeto .NET
├── Program.cs                    # Testes e execução do fluxo de hospedagem
├── diagrama_classe_hotel.png
└── README.md
```

---

## 🚀 Como Executar

### Pré-requisitos
- [.NET SDK](https://dotnet.microsoft.com/download) instalado.

### Passo a passo
1. Clone o repositório ou abra a pasta no terminal:
   ```bash
   dotnet run
   ```
2. O console exibirá a quantidade de hóspedes cadastrados e o valor final calculado com o desconto aplicado.
