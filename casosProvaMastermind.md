# Casos de proba 
## Cas 1
### Selecció de menu, sortir, opció valida

|instriucció| menuSelect  | dificultySelect | tries| usedTries | foundCode| 
|:------------- |:---------------:| :-------------:| :----------:|:----------:|:----------:|
|Inici         |     0      | 0       | 0  | 0 | false |
| Entrada Menu |     1      | 0       | 0  | 0 | false |
| final        |     1      | 0       |  0 | 0 |false |
## Cas 2
### Selecció de dificultat, personalitzada

|instriucció| menuSelect  | dificultySelect | tries| usedTries | foundCode| 
|:------------- |:---------------:| :-------------:| :----------:|:----------:|:----------:|
|Inici         |     0      | 0       | 0  | 0 | false |
| Entrada Menu |     0     | 0       | 0  | 0 | false |
| seleccio dificultat      |     5     | 0       |  0 | 0 |false |
| entrada intents      |     5      | 0       |  8 | 0 |false |
| final     |     0     |  5      |  8 | 0 |false |

## Cas 3
### Intent de joc valid, codi corrcte
|instriucció| userInput   | tries| usedTries | foundCode| turnsTaken |
|:------------- |:---------------:| :-------------:| :----------:|:----------:|:----------:|
|Inici         |     0      | 4       | 0  | false | [ ] |
| Entrada intent |     1234     | 4       | 0  | true | ["1 2 3 4"] |
| final     |     1234    |  4      |  1 | true |["1 2 3 4"]  |


## Cas 4
### intent de joc valid, codi no trobat
|instriucció| userInput   | tries| usedTries | foundCode| turnsTaken |
|:------------- |:---------------:| :-------------:| :----------:|:----------:|:----------:|
|Inici         |     0      | 3       | 0  | false | [ ] |
| intent 1 |     2345     | 3       | 1 | false | ["2 3 4 5"] |
| intent2      |    3456     | 3       |  2 | false |["2 3 4 5", "3 4 5 6"] |
| intent3      |     4561      | 3       |  3 | false |["2 3 4 5", "3 4 5 6", "4 5 6 1"] |
| final     |    4561     |  3    |  3 | false |["2 3 4 5", "3 4 5 6", "4 5 6 1"] |

## Cas 5
### Intent invalid inputs incorrecte
|instriucció| userInput   | tries| usedTries | foundCode| turnsTaken |
|:------------- |:---------------:| :-------------:| :----------:|:----------:|:----------:|
|Inici         |     0      | 3       | 0  | false | [ ] |
| intent 1 |     2375     | 3       | 1 | false | [ ] |
| intent2      |    34226     | 3       |  2 | false |[ ] |
| intent3      |     456      | 3       |  3 | false |[ ] |
| final     |    456     |  3    |  3 | false |[ ] |
## Cas 6
### Entrada de dificultat invalida
|instriucció| dificulty   | tries| usedTries | 
|:------------- |:---------------:| :-------------:| :----------:|
|Inici         |     0      | 0       | 0  | 
| selecció dificultat |    7     | 1       | 0 | 
| final     |    7    |  1    |  0 | 
## Cas 7
### Mixte de inputs valids i invalids
|instriucció| userInput   | tries| usedTries | foundCode| turnsTaken |
|:------------- |:---------------:| :-------------:| :----------:|:----------:|:----------:|
|Inici         |     0      | 3       | 0  | false | [ ] |
| intent 1 |     2375     | 3       | 1 | false | [ "2 3 7 5"] |
| intent2      |    1638     | 3       |  2 | false |[ "2 3 7 5"]  |
| intent3      |     1234      | 3       |  3 | true |["2 3 7 5", "1 2 3 4" ] |
| final     |     1234      | 3       |  3 | true |["2 3 7 5", "1 2 3 4" ] |

