## Habilitações

Para executar as operações envolvendo Títulos Públicos Federais tokenizados (TPFt), é necessário que os participantes efetuem as seguintes habilitações para o contrato TPFtDvP realizar transações com os ativos de sua carteira:

- <span style="text-decoration: underline;">TPFt</span>: deve ser autorizada na carteira do participante ou cliente a manipulação do saldo de TPFt através do método `setApprovalForAll`, herdado do padrão ERC-1155, do contrato TPFt;

- <span style="text-decoration: underline;">RealDigital</span>: deve ser autorizada na carteira do participante uma quantia através do método `approve`, herdado do padrão ERC-20, do contrato RealDigital. Essa quantia poderá ser utilizada em mais de uma operação e é possível autorizar novos valores sempre que necessário; e

- <span style="text-decoration: underline;">RealTokenizado</span>: deve ser autorizada na carteira do participante e do seu cliente uma quantia através do método `approve`, herdado do padrão ERC-20, do contrato RealTokenizado. Essa quantia poderá ser utilizada em mais de uma operação e é possível autorizar novos valores sempre que necessário;

<span style="text-decoration: underline;">Além disso, ao criar novas carteiras na rede, o participante deve informar ao Bacen para que a carteira seja autorizada a ter TPFt.</span> 

O detalhamento das habilitações por operação está representado no quadro abaixo:

<table>
  <tr style="font-weight:bold;">
    <th colspan="7" style="text-align:center;">Habilitações necessárias para operações envolvendo TPFt</th>
  </tr>
  <tr>
    <th rowspan="2" style="text-align:left;">OPERAÇÃO TPFt</th>
    <th colspan="2" style="text-align:center;">realDigital</th>
    <th colspan="2" style="text-align:center;">tpfT</th>
    <th colspan="2" style="text-align:center;">realTokenizado</th>
  </tr>
  <tr>
    <th style="text-align:center;">enableAccount</th>
    <th style="text-align:center;">approve</th>
    <th style="text-align:center;">enableAddress</th>
    <th style="text-align:center;">setApprovalForAll</th>
    <th style="text-align:center;">/:enderecoContrato/enableAccount</th>
    <th style="text-align:center;">/:enderecoContrato/approve</th>
  </tr>
  <tr>
    <td>TPFtOperation1001</td>
    <td></td>
    <td></td>
    <td style="text-align:center;">X*</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>TPFtOperation1002</td>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X*</th>
    <th style="text-align:center;">X</th>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>TPFtOperation1070</td>
    <td></td>
    <td></td>
    <th style="text-align:center;">X*</th>
    <th style="text-align:center;">X</th>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>TPFtOperation1052 (Participante)</td>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X*</th>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X</th>
  </tr>
  <tr>
    <td>TPFtOperation1052 (Cliente)</td>
    <td></td>
    <td></td>
    <th style="text-align:center;">X*</th>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X</th>
    <th style="text-align:center;">X</th>
  </tr>
</table>

| **Habilitações necessárias para operações envolvendo TPFt**                                                                                                                                                            |
|------------------------------------------------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|
|                      **OPERAÇÃO TPFt**                     | **realDigital**   |                   | **tpfT**          |                   | **realTokenizado**|                   |
|                                                            | **enableAccount** | **approve**       | **enableAddress** | **setApprovalForAll** | **/:enderecoContrato/enableAccount** | **/:enderecoContrato/approve** |
| TPFtOperation1001                                          |                   |                   | X*                |                   |                   |                   |
| TPFtOperation1002                                          | X                 | X                 | X*                | X                 |                   |                   |
| TPFtOperation1070                                          |                   |                   | X*                | X                 |                   |                   |
| TPFtOperation1052 (Participante)                           | X                 | X                 | X*                | X                 | X                 | X                 |
| TPFtOperation1052 (Cliente)                                |                   |                   | X*                | X                 | X                 | X                 |



| **DESCRIÇÃO**                                  |
|----------------------------------------------|
| **realDigital/enableAccount:** habilitar a carteira para operar Real Digital. |
| **realDigital/approve:** habilitar o contrato TPFtDvP a realizar transações com Real Digital pela carteira.                                         |
| **tpft/enableAddress:** habilitar a carteira para operar TPFt. _*Somente o Bacen pode habilitar e o participante deve solicitar via e-mail._                                        |
| **tpft/setApprovalForAll:** habilitar o contrato TPFtDvP a realizar transações com TPFt pela carteira.                                         |
| **realTokenizado/:enderecoContrato/enableAccount:** habilitar a carteira para operar Real Tokenizado.                                        |
| **realTokenizado/:enderecoContrato/approve:** habilitar o contrato TPFtDvP a realizar transações com Real Tokenizado pela carteira.                                        |


### **Importante**

### **Habilitação de carteiras para TPFt**

A habilitação das carteiras de participantes e clientes nas operações dos Títulos Públicos Federais tokenizados (TPFt) é diferente da habilitação das carteiras de participantes e clientes no Real Digital. Para a carteira do participante ou do cliente realizar operações no TPFt, é preciso que o participante solicite a habilitação junto ao BACEN.

### **Ações quando houver novo deploy de TPFt**

Sempre que houver deploy de TPFt na rede blockchain todas as habilitações e permissões das carteiras – realizadas antes do deploy – se tornam nulas. Os participantes precisam solicitar ao BACEN as habilitações de suas respectivas carteiras, como também executar as autorizações necessárias para o DvP.

### **Identificação de clientes para o TPFt**

A identificação das carteiras de clientes e participantes nos contratos dos Títulos Públicos Federais tokenizados (TPFt) é feita da seguinte forma: 

1. Carteira de cliente é identificada no cadastro do Key Dictionary. Neste caso, o pagamento do resgate é feito em Real Tokenizado;

2. Carteira do participante é identificada no cadastro do Real Digital e inexistente no Key Dictionary. Neste caso, o pagamento do resgate é feito em Real Digital.

[<<< Voltar](smartcontracts.md)
