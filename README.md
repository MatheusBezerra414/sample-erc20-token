# ERC20Token - Um Token ERC20 Personalizado

Este repositório contém a implementação de um contrato inteligente ERC20 em Solidity. O contrato inclui as funcionalidades básicas do padrão ERC20, além de algumas medidas de segurança para garantir transações seguras e confiáveis.

## Índice

- [Descrição](#descrição)
- [Funcionalidades](#funcionalidades)
- [Interface](#interface)
- [Instalação](#instalação)
- [Uso](#uso)
- [Testes](#testes)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Descrição

O ERC20Token é um contrato inteligente que segue o padrão ERC20 para tokens fungíveis no blockchain Ethereum. Esta implementação é feita do zero, sem utilizar a biblioteca OpenZeppelin, proporcionando uma visão educacional sobre como construir um token ERC20 do início.

## Funcionalidades

- **Transferência de Tokens**: Permite que usuários transfiram tokens entre si.
- **Aprovação e Transferência Delegada**: Usuários podem aprovar outros para gastar tokens em seu nome.
- **Aumento e Redução de Permissões**: Ajuste dinâmico das permissões de gasto.
- **Eventos**: Emissão de eventos para transferências e aprovações, conforme o padrão ERC20.

## Interface

O contrato implementa a interface `IERC20`, que define os métodos e eventos exigidos pelo padrão ERC20.

### Métodos da Interface `IERC20`

- `totalSupply()`: Retorna o fornecimento total de tokens.
- `balanceOf(address account)`: Retorna o saldo de tokens de um endereço específico.
- `transfer(address recipient, uint256 amount)`: Transfere tokens para um endereço.
- `allowance(address owner, address spender)`: Retorna a quantidade de tokens que um proprietário permitiu a um gastador.
- `approve(address spender, uint256 amount)`: Aprova um gastador para gastar uma quantidade específica de tokens.
- `transferFrom(address sender, address recipient, uint256 amount)`: Transfere tokens de uma conta aprovada.

### Eventos

- `Transfer(address indexed from, address indexed to, uint256 value)`: Emissão quando tokens são transferidos.
- `Approval(address indexed owner, address indexed spender, uint256 value)`: Emissão quando uma aprovação é feita.
