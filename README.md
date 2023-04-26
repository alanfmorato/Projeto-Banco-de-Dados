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
- [ ] Analisar os requisitos funcionais e criar o modelo conceitual, utilizar a Ferramenta BRModelo. Esse modelo deve apresentar os conceitos vistos em aula.
OBS: Poderá ser utilizado o mesmo tema utilizado em outra disciplina ou escolher e levantar os requisitos para um novo sistema de software.

- [x] Requisito 01 - Usuários devem fazer login usando e-mail e senha: Nesta entidade criei o e-mail e senha do usuário, sendo que o e-mail é a PK da entidade


![image](https://user-images.githubusercontent.com/102003274/234447430-59421d41-919b-4bfb-8dee-e4d3a7e27c48.png)

- [x] Requisito 02 - Usuários devem ter perfis diferentes: administrador e funcionário: Nesta entidade adicionei o tipo de usuário (admnistrador ou funcionário) assim saberemos qual permissão cada um deles possui.


![image](https://user-images.githubusercontent.com/102003274/234447936-ef8d4d15-88e0-4165-8054-ece2d7d0fa2a.png)

