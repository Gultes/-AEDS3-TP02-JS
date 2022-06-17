# Problema de alocação em redes - Algoritmos e Estruturas de Dados III

## Participantes
- [Filipe Augusto Santos de Moura (Aluno)](https://github.com/Filipey)
- [Gustavo Estevam Sena (Aluno)](https://github.com/Gultes)
- [George Henrique Godim da Fonseca (Orientador)](https://github.com/georgehgfonseca)

## Objetivos
- Aplicar os conhecimentos em algoritmos para resolver um problema real.
- Aprimorar a habilidade de programação de algoritmos em grafos.
- Reforçar o aprendizado sobre os algoritmos de fluxo em redes.

## Sobre
O trabalho consiste em resolver o problema da alocação de professores às disciplinas do DECSI/UFOP
através de algoritmos de fluxo em redes. Cada professor leciona duas ou três disciplinas
e define, a cada semestre quais disciplinas tem preferência por lecionar dentre as que são ofertadas
pelo DECSI. Uma solução para esse problema consiste em uma atribuição de disciplinas aos professores
de modo a maximizar o atendimento de suas preferências. A entrada serão dois arquivos no formato
.csv (separado por vírgulas), um de professores e outro de disciplinas conforme o exemplo:

**professores.csv**

|   Professor    | Disciplinas | Preferência 1 | Preferência 2 | Preferência 3 |
|:--------------:|:-----------:|:-------------:|:-------------:|:-------------:|
| George Fonseca |      2      |    CSI105     |    CSI466     |    CSI601     |
| Bruno Monteiro |      3      |    CSI601     |    CSI602     |    CSI466     |

**disciplinas.csv**

| Disciplina |             Nome              | Turmas |
|:----------:|:-----------------------------:|:------:|
|   CSI105   | Alg. e Estrutura de Dados III |   1    |
|   CSI466   |       Teoria dos Grafos       |   1    |
|   CSI601   |       Banco de Dados I        |   2    |
|   CSI602   |       Banco de Dados II       |   1    |

O programa irá ler
esses arquivos de entrada e criar a rede de fluxo correspondente ao problema de alocação. A rede
de fluxo terá quatro camadas, um com o nó de super oferta, outra com nós representado os professores, outra
representando as disciplinas e, por fim, o nó de super demanda. Com relação às preferências, os seguintes
custos incorrem:

| Preferência |  1  |  2  |  3  |  4  |  5  |
|:-----------:|:---:|:---:|:---:|:---:|:---:|
|    Custo    |  0  |  3  |  5  |  8  | 10  |

## Run 🏃‍

```bash
# Clone este repositório
$ git clone https://github.com/gultes/AEDS3-TP02-JS.git

$Com nodejs instalado na máquina

# Acesse o diretório do projeto pelo Visual Studio Code por exemplo
$ cd AEDS3-TP02-JS

# Digite no terminal
$ yarn

# Clique em Run/Run Without Debugging [CTRL + F5]

$Alternativamente você pode:

$Instalar a extensão Code Runner no vscode
$Pressionar CTRL + Alt + N para executar: Nesse caso o resultado também será exibido na guia Output
````

````
A execução irá retornar em Debug Console a seguinte resposta:


Teacher:     

             #Diego Garcia,
             #Subject: CSI450,
             #Name: Interacao Humano-Computador,
             #Classes: 1 
             #Cost: 0

The total cost was 116
Total classes allocated: 72
This teachers dont offer any subject: Bruno Hott,Elton Cardoso
Ended.
````
