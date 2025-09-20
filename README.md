# Projeto de Oficina - Modelo de Banco de Dados

### Descrição do Projeto
Este projeto foi realizado a partir do "**Desafio DIO: Construindo um Esquema Conceitual para Banco De dados**" e consiste em criar um **esquema conceitual de banco de dados para o contexto de uma oficina mecânica** com base na narrativa  fornecida, através do **MySQL Workbench**. O modelo contempla clientes, veículos, ordens de serviço, equipes de mecânicos, serviços, peças, estoque e fornecedores, permitindo o controle de execução, cálculo de valores e acompanhamento do status de cada OS.

### Objetivo 
O objetivo é criar um esquema conceitual para gerenciar o funcionamento de uma oficina mecânica, onde:
- Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
- A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
- O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços
- A mesma equipe avalia e executa os serviços
- Os mecânicos possuem código, nome, endereço e especialidade
- Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

### Refinamento
Algumas decisões de modelagem foram tomadas com base no contexto real de oficinas mecânicas, que não estavam detalhadas na narrativa original.
- A narrativa proposta pelo desafio sugeria designar o veículo diretamente à uma equipe. No entanto, em cenários reais, um veículo pode retornar à oficina e ser atendido por equipes diferentes. Por isso, durante a etapa de refinamento, optei por associar a equipe à Ordem de Serviço e não diretamente ao veículo, garantindo maior flexibilidade.
- Apesar da narrativa proposta não sugerir a criação dessas tabelas, para melhor gerenciamento das peças utilizadas pela oficina, foram adicionadas as tabelas de Estoque e Fornecedor.
