# Engenharia de Requisitos

## Índice

- Conceitos Básicos
- Classificação dos Requisitos
- Técnicas de elicitação de requisitos
- Gerenciamento de requisitos
- Especificação de requisitos
- Técnicas de validação de requisitos
- Prototipação

Sommerville afirma que os requisitos de software são frequentemente classificados como requisitos funcionais e requisitos não funcionais:

**Requisitos funcionais:** _são declarações de serviços que o sistema deve fornecer, de como o sistema deve reagir a entradas específicas e de como o sistema deve se comportar em determinadas situações. Em alguns casos, os requisitos funcionais também podem explicitar o que o sistema não deve fazer_.

**Requisitos não funcionais:** _são restrições aos serviços ou funções oferecidos pelo sistema. Incluem restrições de timing, restrições no processo de desenvolvimento e restrições impostas pelas normas. Ao contrário das características individuais ou serviços do sistema, os requisitos não funcionais, muitas vezes, aplicam-se ao sistema como um todo._

Os requisitos não funcionais podem ser provenientes das características requeridas para o software (requisitos de produto), da organização que desenvolve o software (requisitos organizacionais) ou de fontes externas:

**Requisitos de produto.** Esses requisitos especificam ou restringem o comportamento do software. Exemplos incluem os requisitos de desempenho quanto à rapidez com que o sistema deve executar e quanta memória ele requer, os requisitos de confiabilidade que estabelecem a taxa aceitável de falhas, os requisitos de proteção e os requisitos de usabilidade.

**Requisitos organizacionais.** Esses são os requisitos gerais de sistemas derivados das políticas e procedimentos da organização do cliente e do desenvolvedor. Exemplos incluem os requisitos do processo operacional, que definem como o sistema será usado, os requisitos do processo de desenvolvimento que especificam a linguagem de programação, o ambiente de desenvolvimento ou normas de processo a serem usadas, bem como os requisitos ambientais que especificam o ambiente operacional do sistema.

**Requisitos externos.** Esse tipo abrange todos os requisitos que derivam de fatores externos ao sistema e seu processo de desenvolvimento. Podem incluir requisitos reguladores, que definem o que deve ser feito para que o sistema seja aprovado para uso, por um regulador, tal como um banco central; requisitos legais, que devem ser seguidos para garantir que o sistema opere dentro da lei; e requisitos éticos, que asseguram que o sistema será aceitável para seus usuários e o público em geral.  
 
### Classificação dos Requisitos Não Funcionais

**Requisitos de produtos:** Requisitos que especificam o comportamento do produto.Ex. portabilidade; tempo na execução; confiabilidade, mobilidade, etc.

**Requisitos de usabilidade** (facilidade de uso). Ex.: usuários deverão operar o sistema após um determinado tempo de treinamento.

**Requisitos de eficiência**. Ex.: o sistema deverá processar n requisições por um determinado tempo.

**Requisitos de confiabilidade**. Ex.: o sistema deverá ter alta disponibilidade, p.exemplo, 99% do tempo.

**Requisitos de portabilidade**. Ex.: o sistema deverá executar em qualquer plataforma.

**Requisitos organizacionais**: Requisitos decorrentes de políticas e procedimentos corporativos. Ex. padrões, infraestrutura,etc.

**Requisitos de entrega**. Ex.: um relatório de acompanhamento deverá ser fornecido toda segunda-feira.

**Requisitos de implementação**. Ex.: o sistema deverá ser desenvolvido na linguagem Java.

**Requisitos de padrões**. Ex.: uso de programação orientada a objeto sob a plataforma A.

**Requisitos externos**: Requisitos decorrentes de fatores externos ao sistema e ao processo de desenvolvimento. Ex. requisitos de interoperabilidade, legislação,localização geográfica etc.

**Requisitos de interoperabilidade**. Ex.: o sistema deverá se comunicar com o banco SQL Server. 
_[GABARITO DA QUESTÃO]_

**Requisitos éticos**. Ex.: o sistema não apresentará aos usuários quaisquer dados de cunho privativo.

**Requisitos legais**. Ex.: o sistema deverá atender às normas legais, tais como padrões, leis, etc.

Assim, temos que a interoperabilidade entre um software que esteja em desenvolvimento e outros sistemas existentes é considerada um requisito não funcional.