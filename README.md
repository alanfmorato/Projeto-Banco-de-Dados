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
- [ ] Mapear o modelo conceitual, realizado na parte 1, para o modelo lógico. São 7 passos propostos por Elmasri & Navathe (1994), para o mapeamento do Modelo Entidade Relacionamento para o Modelo Relacional: - Mapear os Conjuntos de Entidades “Fortes” (Regulares), - Mapear Conjuntos de Entidades Fracas,- Mapear Conjuntos de Relacionamento Binário 1:1,-Mapear Conjuntos de Relacionamento Binário 1:N, - Mapear Conjuntos de Relacionamento Binário M:N, -Mapear Conjuntos de Relacionamentos n>2 e - Mapear Atributos Multivalorados.
OBS: - Demonstrar o que ocorre em cada passo de forma textual. (Apenas para os alunos que utilizarem BR Modelo)

![image](https://user-images.githubusercontent.com/102003274/235305578-cd5767b3-5925-49ae-bed3-a9c22a44957a.png)
