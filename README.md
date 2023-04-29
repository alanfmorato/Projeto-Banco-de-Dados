# Projeto-Banco-de-Dados

## Contexto
Fazer um sistema para auxiliar no monitoramento dos equipamentos de cada ambiente e funcionário. As
instituições possuem equipamentos patrimoniados, tais como, computadores, monitores e impressoras. Cada
equipamento precisa estar registrado para um funcionário responsável – se o equipamento sumir o funcionário
responsável deverá ressarcir a instituição. Cada equipamento precisa ter a localização, ou seja, o equipamento
precisa estar registrado em algum ambiente (sala).

---

## Requisitos

- [ ] Usuários devem fazer login usando e-mail e senha;
- [ ] Usuários devem ter perfis diferentes: administrador e funcionário;
- [ ] Usuários administrador podem criar, editar e excluir equipamentos, ambientes e funcionários;
- [ ] Usuários administrador podem atribuir equipamentos para funcionários;
- [ ] Usuários administrador podem alterar a localização do equipamento;
- [ ] Usuários funcionário podem apenas consultar os equipamentos de sua responsabilidade;
- [ ] Usuários administrador devem registrar a data de entrada e saída do equipamento em cada ambiente;
- [ ] Usuários administrador podem dar baixa do equipamento. Ao dar baixa, o equipamento deixa de existir fisicamente na instituição, porém ele continuará existindo na base de dados;
- [ ] Gerar relatório de equipamentos por tipo (computador, impressora etc.) e por ambiente

---

## 01 - Modelo Conceitual
- [x] Analisar os requisitos funcionais e criar o modelo conceitual, utilizar a Ferramenta BRModelo. Esse modelo deve apresentar os conceitos vistos em aula.
OBS: Poderá ser utilizado o mesmo tema utilizado em outra disciplina ou escolher e levantar os requisitos para um novo sistema de software.

![image](https://user-images.githubusercontent.com/102003274/235305634-e8e3cc98-387c-4723-ab33-fcff5a3b46a6.png)


## 02 - Modelo Lógico Relacional
- [x] Mapear o modelo conceitual, realizado na parte 1, para o modelo lógico. São 7 passos propostos por Elmasri & Navathe (1994), para o mapeamento do Modelo Entidade Relacionamento para o Modelo Relacional: - Mapear os Conjuntos de Entidades “Fortes” (Regulares), - Mapear Conjuntos de Entidades Fracas,- Mapear Conjuntos de Relacionamento Binário 1:1,-Mapear Conjuntos de Relacionamento Binário 1:N, - Mapear Conjuntos de Relacionamento Binário M:N, -Mapear Conjuntos de Relacionamentos n>2 e - Mapear Atributos Multivalorados.
OBS: - Demonstrar o que ocorre em cada passo de forma textual. (Apenas para os alunos que utilizarem BR Modelo)

- [x]  Mapear os Conjuntos de Entidades “Fortes” (Regulares): Entidade "usuario" e "ambiente" é forte, pois podem existir independente de outras condições
- [x]  Mapear Conjuntos de Entidades Fracas: Entidade "Equipamento" é fraca, pois depende exclusivamente estar registrado por um funcionário e em um ambiente. Ela é o elo de ligação entre as outras entidades.
- [x]  Mapear Conjuntos de Relacionamento Binário 1:1 : usuario(1,1) - (0,n)equipamento -> Ou seja, 1 funcionário pode ou não ter um equipamento registrado em seu nome, porém um equipamento sempre estará registrado no nome de um funcionário. equipamento (1,1) - (0,n) datas, 1 equipamento sempre estara registrado em um ambiente com data de entrada e saida, equipamento (0,n) - (1,n) ambiente, 1 equipamento sempre estara registrado em um ambiente, e um ambiente pode ter nenhum ou n equipamentos.
- [x]  Mapear Conjuntos de Relacionamento Binário 1:N: usuario(1,1) - (0,n)equipamento -> Ou seja, 1 funcionário pode ou não ter um equipamento registrado em seu nome, porém um equipamento sempre estará registrado no nome de um funcionário. equipamento (1,1) - (0,n) datas, 1 equipamento sempre estara registrado em um ambiente com data de entrada e saida, equipamento (0,n) - (1,n) ambiente, 1 equipamento sempre estara registrado em um ambiente, e um ambiente pode ter nenhum ou n equipamentos.
- [x]   Mapear Conjuntos de Relacionamento Binário M:N: Não existem conjuntos M:N
- [x]  Mapear Conjuntos de Relacionamentos n>2: Podem haver mais de 2 registros na entidade ambiente para a mesma sala.
- [x]  Mapear Atributos Multivalorados: 

![image](https://user-images.githubusercontent.com/102003274/235305578-cd5767b3-5925-49ae-bed3-a9c22a44957a.png)


## 03 - Normalização

A normalização de tabelas é um processo utilizado no projeto de bancos de dados relacionais para reduzir a redundância de dados e evitar anomalias de atualização. Ele envolve dividir uma tabela grande em duas ou mais tabelas menores e relacioná-las por meio de chaves estrangeiras.

O objetivo da normalização de tabelas é tornar o banco de dados mais eficiente e fácil de manter, garantindo que cada tabela armazene informações sobre uma única entidade ou assunto e que os dados estejam organizados de forma lógica e consistente. A normalização de tabelas é baseada em um conjunto de regras e formas normais que definem como os dados devem ser estruturados para evitar problemas comuns, como redundância de dados, inconsistências e conflitos de atualização.

### Primeira Forma Normal (1FN)

Requisitos para a tabela estar na 1FN
* Valores atoômicos e indivisiveis
* Sem duplicidade de valores
* Tem uma PK
* Decomposta

Todas as tabelas do sistema estão na 1FN e atendem todos os requisitos acima

### Segunda Forma Normal (2FN)

* Estar na 1FN
* Todos os atributos não-chave são dependentes de todas as partes da PK
* Não tem atributo dependente de parte da PK - Composta (Se tiver quebra em nova tabela)

Todas as tabelas do sistema est~;ao na 1FN, todas os atributos que não são chaves dependem da chave
