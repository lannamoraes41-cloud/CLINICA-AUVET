# Autoavaliação -- ISO/IEC 25010

**Projeto:** CLI SISTEMAS -- AUVET\
**Disciplina:** Engenharia de Software\
**Integrantes:**\
Gerson Junior\
Isadora Assis Cardoso\
Cláudio Josimar\
Lanna Moraes

## Ponto forte da qualidade do projeto

Na revisão dos diagramas do processo de agendamento de consulta,
identificamos como ponto forte a organização do fluxo principal. O
diagrama de sequência apresenta a interação entre a recepcionista, a
tela de agendamento, o sistema de controle e o banco de dados. Já o
diagrama de atividades representa as principais etapas, desde a seleção
do cliente e do pet até a confirmação da consulta. Essa organização
ajuda a compreender o funcionamento esperado do processo e contribui
para a comunicação da equipe durante o desenvolvimento.

## Principal risco identificado e mitigação

O principal risco identificado nesta revisão está relacionado à
confiabilidade do agendamento quando o horário escolhido não está
disponível ou deixa de estar disponível antes da confirmação. Nos
diagramas enviados, o caminho principal está representado, mas o
tratamento da situação alternativa ainda precisa ficar mais claro. Para
mitigar esse risco, devemos incluir no diagrama de sequência um
fragmento `alt`, diferenciando o cenário de horário disponível do
cenário de horário indisponível. No diagrama de atividades, também
devemos identificar as saídas da decisão com `[Sim]` e `[Não]` e
conectar o caminho negativo à escolha de outro horário, retornando à
consulta de disponibilidade.

## O que foi avaliado na revisão

Foram avaliados os seguintes artefatos enviados pela equipe:

-   Diagrama de sequência -- Agendar Consulta.
-   Diagrama de atividades -- Agendamento de Consulta.

A análise considerou a clareza do fluxo, a comunicação entre os
participantes, a representação da decisão sobre disponibilidade e o
tratamento de situações alternativas. Os diagramas apresentam o fluxo
principal, mas ainda precisam dos ajustes descritos para representar
melhor os cenários de exceção.

## Ajustes necessários

1.  Adicionar o fragmento `alt` no diagrama de sequência para os
    cenários de horário disponível e indisponível.
2.  Identificar as condições `[Sim]` e `[Não]` na decisão do diagrama de
    atividades.
3.  Conectar a saída `[Não]` à atividade de escolher outro horário e
    fazer o fluxo retornar à consulta de horários disponíveis.
4.  Conferir se o sistema verifica novamente a disponibilidade antes de
    registrar a consulta.

**Observação:** esta autoavaliação foi elaborada com base nos dois
diagramas disponibilizados. Os demais artefatos do projeto, como
diagrama de classes, casos de uso, requisitos, Trello, GitHub e
protótipos, ainda precisam ser revisados separadamente. Os ajustes
listados são recomendações identificadas na análise, não alterações que
já tenham sido realizadas.
