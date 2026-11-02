# DIO - Trilha .NET: Explorando a Linguagem C# | Sistema de Hospedagem de Hotel

Este projeto foi desenvolvido como parte de um desafio de código da trilha .NET da [DIO (Digital Innovation One)](https://www.dio.me/), com o objetivo de colocar em prática os conceitos aprendidos em C#.

---

## Sobre o projeto

A proposta foi desenvolver um sistema simples para gerenciar reservas de um hotel, trabalhando com hóspedes, suítes e cálculos de hospedagem.

Durante o desenvolvimento, foram implementadas algumas funcionalidades:

- Cadastro de hóspedes e suítes.
- Verificação da capacidade máxima de hóspedes por suíte.
- Contagem dos hóspedes cadastrados na reserva.
- Cálculo do valor total da hospedagem de acordo com a diária e a quantidade de dias.
- Aplicação de 10% de desconto para reservas com 10 dias ou mais.

Caso a quantidade de hóspedes ultrapasse a capacidade da suíte, o sistema retorna uma exceção.

---

## Diagrama de Classes

![Diagrama de classe hotel](diagrama_classe_hotel.png)

### Classes do projeto

O projeto foi dividido em três classes principais:

- **Pessoa:** contém as informações dos hóspedes, como nome, sobrenome e nome completo.
- **Suite:** armazena as informações da suíte, incluindo tipo, capacidade e valor da diária.
- **Reserva:** responsável por reunir os hóspedes e a suíte, além de realizar as validações e os cálculos da hospedagem.

Na classe `Reserva`, foram utilizados os seguintes métodos:

- `CadastrarHospedes(List<Pessoa>)`: adiciona os hóspedes, verificando a capacidade da suíte.
- `CadastrarSuite(Suite)`: associa uma suíte à reserva.
- `ObterQuantidadeHospedes()`: informa quantos hóspedes estão cadastrados.
- `CalcularValorDiaria()`: calcula o valor da hospedagem e aplica o desconto quando necessário.

---

## Tecnologias utilizadas

- C#
- .NET 8
- Git e GitHub

---

## Estrutura do projeto

```text
trilha-net-explorando-desafio/
├── Models/
│   ├── Pessoa.cs
│   ├── Reserva.cs
│   └── Suite.cs
├── DesafioProjetoHospedagem.csproj
├── Program.cs
├── diagrama_classe_hotel.png
└── README.md
```

---

## Como executar

Para executar o projeto, é necessário ter o [.NET SDK](https://dotnet.microsoft.com/download) instalado.

1. Clone o repositório ou abra a pasta do projeto no terminal.
2. Execute o comando:

```bash
dotnet run
```

Após a execução, o console exibirá as informações da reserva, incluindo a quantidade de hóspedes e o valor total da hospedagem.
