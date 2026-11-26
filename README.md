# Task Manager

> 📌 **Meu primeiro projeto em Java**, desenvolvido no início da graduação em
> Engenharia de Software (Univates), na disciplina de Programação de
> Aplicações, quando eu ainda não trabalhava na área.

<div align="center">

![gif1](info/gif1.gif)
![gif2](info/gif2.gif)
![gif3](info/gif3.gif)
![gif4](info/gif4.gif)

</div>

## Sobre

O desafio da disciplina era simular um software comercial em Java Swing,
com telas de cadastro e relatórios em JasperReports. O tema era livre;
escolhi um sistema de gestão de tarefas (tickets) para empresas, com
usuários, departamentos, setores, funções e tarefas com fluxo de situação.

## Swing feito à mão

O NetBeans propunha montar as telas arrastando componentes. Testei, não
gostei do resultado e decidi escrever a interface direto no código.

O ponto de partida foi um detalhe visual: eu queria bordas arredondadas
(como o `border-radius` do CSS), e o Swing não oferecia isso de forma
simples. As tentativas rápidas "vazavam" e ficavam estranhas. A solução
foi criar meus próprios componentes, como `RoundedPanel`, `ButtonSTM`,
`FieldSTM` e `DialogSTM`.

Estudar o código da própria biblioteca, bem mais complexo do que eu
estava acostumado, me mostrou na prática a importância de uma boa
abstração.

## Como foi construído

- **Interface:** Java Swing com componentes próprios, sem editor visual
- **Arquitetura:** MVC com DAOs
- **Dados:** JDBC puro com PostgreSQL
- **Segurança:** senhas com hash SHA-512
- **Relatórios:** 4 relatórios em JasperReports (situação das tarefas,
  tarefas por responsável, usuários por departamento e vínculos de usuário)

## O que esse projeto me ensinou

Passei muito tempo querendo entender e construir tudo do meu jeito, e o
prazo apertou. Precisei correr para fazer o fluxo completo funcionar no
final, e alguns conceitos ficaram sem ser explorados como eu queria.

A lição ficou: **primeiro um fluxo completo funcionando, depois a
evolução**.

## Como executar

- JDK 8+ e PostgreSQL
- Criar o banco de dados manualmente
- Criar as tabelas com o script `src/model/DB/tablesDB.sql`
- (Opcional) carga inicial de dados com `src/model/DB/loadDB.sql`
- Configurar a conexão na classe `ConnectionDB`
- Build com Ant; as dependências estão na pasta `files/`
