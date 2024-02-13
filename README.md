<!--
- tipagem
    - estática x dinamica
    - forte x fraca
- compilada x interpretada
- paradigmas
    - procedural
    - OO
    - funcional
    - lógica
    - específica de domínio
- exemplos reais
    - *c/c++
    - *java
        - kotlin
    - *python
    - *javascript
    - swift
    - php
    - go
-->

# Linguagens de Programação

As linguagens de programação são ferramentas que capacitam os programadores a construir programas de computador, indo desde os mais simples, como calculadores, aos mais complexos, como agentes de inteligência artifical. Analogamente, elas funcionam como uma espécie de língua, permitindo que os seres humanos comuniquem instruções aos computadores e solicitem a execução de tarefas específicas. Este diálogo entre humanos e máquinas é facilitado por diferentes tipos de linguagens, divididas entre aquelas de baixo nível, mais próximas do código binário utilizado pelas máquinas, e as de alto nível, que se assemelham mais às línguas faladas pelos humanos.

Nos primórdios da computação, os programadores trabalhavam predominantemente com linguagens de baixo nível, enquanto, atualmente, a esmagadora maioria deles opta por linguagens de alto nível. Por isso, é sobre essas linguagens que este artigo discorrerá, classificando-as de acordo com suas características, apresentando os paradigmas de programação que influenciam as abordagens de desenvolvimento e oferecendo exemplos concretos de linguagens usadas atualmente para construir ferramentas usadas no nosso dia-a-dia.

## Sistemas de Tipos

O sistema de tipos de uma linguagem é um conjunto de regras em que cada valor ou dado em um programa tem um tipo, sendo que os possíveis tipos variam de acordo com a linguagem. Esses são alguns exemplos de valores e seus tipos: `12` (número inteiro), `12.25` (número de ponto flutuante), `"pirata que estica"` (cadeia de caracteres).

O sistema de tipos de uma linguagem é uma de suas características essenciais, exercendo influência significativa na manipulação de dados durante a programação. Nesse contexto, existem duas distinções fundamentais entre linguagens: a tipagem estática em contraste com a tipagem dinâmica, e a tipagem forte comparada à tipagem fraca. Contudo, é interessante observar que não é raro encontrar, por exemplo, linguagens que, apesar de serem predominantemente de tipagem forte, apresentam algumas características de linguagens de tipagem fraca, evidenciando a complexidade do assunto.

### Tipagem Estática vs Tipagem Dinâmica

Em geral, em linguagens com tipagem estática, o tipo de uma variável é determinado durante o tempo de compilação e permanece constante ao longo do código. Essas linguagens são comumente compiladas, pois essa abordagem é eficaz para lidar com a tipagem estática.

Por outro lado, em linguagens com tipagem dinâmica, o tipo de uma variável só é conhecido durante a execução do programa, podendo variar dependendo do ponto em que a execução está sendo analisada. Linguagens com essa característica geralmente são interpretadas, pois a tipagem dinâmica e a interpretação se complementam.

Ao comparar os dois estilos de tipagem, as vantagens de um geralmente coincidem com as desvantagens do outro. Linguagens dinâmicas oferecem maior flexibilidade, dinamicidade e exigem menos código, porém, em troca, podem sacrificar robustez, previsibilidade, desempenho e proteção contra bugs, características presentes em linguagens estáticas.

Por outro lado, linguagens estáticas são conhecidas por sua robustez, segurança, maior desempenho e previsibilidade. No entanto, podem ser consideradas mais rígidas e verbosas em comparação com as linguagens dinâmicas.

Na prática, as linguagens geralmente não se enquadram puramente em um desses paradigmas, mas incorporam características de ambos. Essas particularidades serão exemplificadas mais adiante neste artigo.

```java
// Tipagem Estática:

Integer x = 420;
x = "AAAAAAAAAAAAAAAAAAAAAAA" // gera erro de compilação
```

```python
# Tipagem Dinâmica:

x = 69
x = "antes sofria, hoje sou fria" # permitido
```

### Tipagem Forte vs Tipagem Fraca


