<!--
- paradigmas
    - procedural
    - OO
    - funcional
    - lógica
    - específica de domínio
- exemplos reais
    - *c/c++
    - *python
    - *java
        - kotlin
        - c#
    - *javascript
    - swift
    - php
    - go
-->

# Linguagens de Programação

As linguagens de programação são ferramentas que capacitam os programadores a construir programas de computador, indo desde os mais simples, como calculadoras, aos mais complexos, como agentes de inteligência artifical. Analogamente, elas funcionam como uma espécie de língua, permitindo que os seres humanos comuniquem instruções aos computadores e solicitem a execução de tarefas específicas. Este diálogo entre humanos e máquinas é facilitado por diferentes tipos de linguagens, divididas entre aquelas de baixo nível, mais próximas do código binário utilizado pelas máquinas, e as de alto nível, que se assemelham mais às línguas faladas pelos humanos.

Nos primórdios da computação, os programadores trabalhavam predominantemente com linguagens de baixo nível, enquanto, atualmente, a esmagadora maioria deles opta por linguagens de alto nível. Por isso, é sobre essas linguagens que este artigo discorrerá, classificando-as de acordo com suas características, apresentando os paradigmas de programação que influenciam as abordagens de desenvolvimento e oferecendo exemplos concretos de linguagens usadas atualmente para construir ferramentas usadas no nosso dia-a-dia.

## Compilação e Interpretação

Em uma linguagem compilada, o desenvolvedor escreve o código em uma linguagem de programação, e todo o código é convertido integralmente em linguagem de máquina durante o processo de compilação. Esse resultado é um executável independente que pode ser executado sem a necessidade do código-fonte original. Esse método proporciona uma execução rápida, pois a tradução para código de máquina ocorre durante a compilação, otimizando completamente o código para o sistema alvo.

Em contrapartida, linguagens interpretadas não geram um executável. Cada linha do código é convertida em código de máquina em tempo real por um interpretador, que é necessário durante toda a execução do programa. Embora a execução seja mais lenta em comparação com linguagens compiladas, a vantagem está na ausência de uma etapa de compilação, permitindo a execução imediata do código assim que é escrito.

A compilação pode ser um processo demorado, mas oferece benefícios, como a total otimização do código, a ausência da responsabilidade de conversão do código durante execução e a privacidade do código-fonte, já que apenas o executável é distribuído. Por outro lado, em linguagens interpretadas, o próprio código-fonte é executado, proporcionando facilidade de distribuição, mas expondo o código ao ambiente de execução.

No contexto de linguagens compiladas, o executável resultante não é multiplataforma, requerendo recompilação para cada sistema em que será executado. Em contraste, linguagens interpretadas podem ser executadas em qualquer sistema que possua o interpretador correspondente. Contudo, a execução nesse caso fica dependente do interpretador, o que pode ser considerado uma desvantagem.

É importante notar que existem também linguagens híbridas, que combinam elementos de ambas as abordagens. Essa abordagem será discutida mais a frente no artigo.

## Sistemas de Tipos

O sistema de tipos de uma linguagem é um conjunto de regras em que cada valor ou dado em um programa tem um tipo, sendo que os possíveis tipos variam de acordo com a linguagem. Esses são alguns exemplos de valores e seus tipos: `12` (número inteiro), `12.25` (número de ponto flutuante), `"pirata que estica"` (cadeia de caracteres).

O sistema de tipos de uma linguagem é uma de suas características essenciais, exercendo influência significativa na manipulação de dados durante a programação. Nesse contexto, existem duas distinções fundamentais entre linguagens: a tipagem estática em contraste com a tipagem dinâmica, e a tipagem forte comparada à tipagem fraca. Contudo, é interessante observar que não é raro encontrar, por exemplo, linguagens que, apesar de serem predominantemente de tipagem forte, apresentam algumas características de linguagens de tipagem fraca, evidenciando a complexidade do assunto.

### Tipagem Estática e Tipagem Dinâmica

Em geral, em linguagens com tipagem estática, o tipo de uma variável é determinado durante o tempo de compilação e permanece constante ao longo do código. Essas linguagens são comumente compiladas, pois essa abordagem é eficaz para lidar com a tipagem estática.

Por outro lado, em linguagens com tipagem dinâmica, o tipo de uma variável só é conhecido durante a execução do programa, podendo variar dependendo do ponto em que a execução está sendo analisada. Linguagens com essa característica geralmente são interpretadas, pois a tipagem dinâmica e a interpretação se complementam.

Em outras palavras, o que diferencia esses dois grupos é o momento em que acontecem as checagens de tipo. Em linguagens dinâmicas, ela acontece em tempo de execução, enquanto em linguagens estáticas ela acontece em tempo de compilação, antes da execução.

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

### Tipagem Forte e Tipagem Fraca

Na subseção anterior, delineamos a distinção entre linguagens com base no momento da realização da checagem de tipos. Agora, voltamos nossa atenção para a rigidez dessa checagem, sendo que a natureza desta diferenciação é menos clara, uma vez que se trata de um espectro contínuo.

A tipagem de uma linguagem, quando mais fraca, amplia a probabilidade de ocorrerem conversões implícitas de tipo. Em outras palavras, a frequência dessas conversões está intrinsecamente ligada ao grau de permissividade concedido pela linguagem na manipulação de tipos de dados. Como mostrado a seguir, ainda mais que a tipagem dinâmica, uma tipagem mais fraca pode comprometer a segurança e a previsibilidade de uma linguagem:

```java
// Característica de Tipagem Forte:

int a = 10;
String b = "2";
a = a + b;  // Gera erro de tipo
```

```js
// Característica de Tipagem Fraca:

let a = 10
const b = "2"
a = a + b   // a = "102"
```

## Paradigmas de Programação

Paradigmas de programação referem-se a maneiras de estruturar e conceber código, essencialmente representando abordagens distintas para resolver problemas por meio da programação. São, portanto, maneiras de programar.

A categorização dos paradigmas divide-se principalmente em dois tipos: programação imperativa e programação declarativa. A programação imperativa envolve a explicitação passo a passo de ações a serem executadas, baseando-se na mudança de estado do programa e no controle do fluxo de execução, refletindo de perto o funcionamento interno de um computador.

Por outro lado, a programação declarativa concentra-se apenas na declaração do problema e na especificação do resultado desejado, sem prescrever a sequência exata de passos para atingir esse resultado. Essa abordagem é mais abstrata, distanciando-se do nível de detalhes da implementação.

Linguagens de programação podem adotar exclusivamente um paradigma, mas é mais comum que uma linguagem ofereça suporte a vários paradigmas, mesmo que um deles seja predominante. Nesta seção, apresentaremos os paradigmas mais amplamente utilizados: programação procedural, programação orientada a objetos e programação funcional.

### Programação Procedural



### Programação Orientada a Objetos



### Programação Funcional



## Fontes

[Compiled vs Interpreted Programming Languages | What’s the Difference?](https://youtu.be/F64_bwahaWQ?si=231_k91GpdvCPmJk)

[Static vs Dynamic Typing | Which languages are better?](https://youtu.be/GqXpFycPWLE?si=vXei9EWiijcXiTaQ)

[Static VS Dynamic Programming Languages 🤔 | WHAT'S THE DIFFERENCE?](https://youtu.be/bCIFTWQorL0?si=eHUNDQtGOmKLAial)

[Typing: Static vs Dynamic, Weak vs. Strong / Intro to JavaScript ES6 programming, lesson 16](https://youtu.be/C5fr0LZLMAs?si=wLLbSbyw4SrbX5ia)

[Programming paradigm - Wikipedia](https://en.wikipedia.org/wiki/Programming_paradigm)

[Introduction of Programming Paradigms - GeeksforGeeks](https://www.geeksforgeeks.org/introduction-of-programming-paradigms/)
