# DIO Coin - Blockchain Developer Challenge

Este repositório contém a implementação de um contrato inteligente para um token ERC-20 chamado "DIO Coin". Este projeto foi desenvolvido como parte do desafio "Binance - Blockchain Developer with Solidity" promovido pela DIO.

## Descrição

O contrato `DIOToken` é uma implementação básica do padrão ERC-20, que define um token fungível em uma blockchain. O token tem o símbolo "DIO" e o nome "DIO Coin". Ele suporta operações básicas como transferência de tokens, aprovação de gastos e consulta de saldos.

## Funcionalidades

- **totalSupply**: Retorna a quantidade total de tokens em circulação.
- **balanceOf**: Retorna o saldo de tokens de um endereço específico.
- **transfer**: Permite a transferência de tokens de um endereço para outro.
- **approve**: Permite que um endereço aprove que outro endereço gaste uma quantidade específica de tokens em seu nome.
- **allowance**: Retorna a quantidade de tokens que um endereço aprovado pode gastar em nome do dono do token.
- **transferFrom**: Permite a transferência de tokens de um endereço para outro, de acordo com a quantidade aprovada.

## Contrato

### ERC20Interface

```solidity
interface ERC20Interface {
    function totalSupply() external view returns (uint);
    function balanceOf(address tokenOwner) external view returns (uint balance);
    function allowance(address tokenOwner, address spender) external view returns (uint remaining);
    function transfer(address to, uint tokens) external returns (bool success);
    function approve(address spender, uint tokens) external returns (bool success);
    function transferFrom(address from, address to, uint tokens) external returns (bool success);

    event Transfer(address indexed from, address indexed to, uint tokens);
    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
}
```

## Como Usar

1. **Deploy**: Compile e faça o deploy do contrato `DIOToken` na rede Ethereum de sua escolha (testnet ou mainnet).
2. **Interação**: Utilize uma ferramenta como Remix, Truffle, ou Hardhat para interagir com o contrato e testar suas funcionalidades.

## Requisitos

- [Solidity](https://soliditylang.org/) versão 0.8.7 ou superior.
- [Ethereum](https://ethereum.org/) Testnet ou Mainnet para deploy e testes.

## Licença

Este projeto está licenciado sob a [GPL-3.0](https://opensource.org/licenses/GPL-3.0).
