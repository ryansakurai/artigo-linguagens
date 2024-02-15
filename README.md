<!--
- exemplos reais
    - *c/c++
    - *javascript
    - *python
    - *java
    - go
-->

# Linguagens de Programação

As linguagens de programação são ferramentas que capacitam os programadores a construir programas de computador, indo desde os mais simples, como calculadoras, aos mais complexos, como agentes de inteligência artifical. Analogamente, elas funcionam como uma espécie de língua, permitindo que os seres humanos comuniquem instruções aos computadores e solicitem a execução de tarefas específicas. Este diálogo entre humanos e máquinas é facilitado por diferentes tipos de linguagens, divididas entre aquelas de baixo nível, mais próximas do código binário utilizado pelas máquinas, e as de alto nível, que se assemelham mais às línguas faladas pelos humanos.

Nos primórdios da computação, os programadores trabalhavam predominantemente com linguagens de baixo nível, enquanto, atualmente, a esmagadora maioria deles opta por linguagens de alto nível. Por isso, é sobre essas linguagens que este artigo discorrerá, classificando-as de acordo com suas características, apresentando os paradigmas de programação que influenciam as abordagens de desenvolvimento e oferecendo exemplos concretos de linguagens usadas atualmente para construir ferramentas usadas no nosso dia-a-dia.

## Compilação e Interpretação

Embora comumente rotulemos linguagens como "compiladas" ou "interpretadas", tecnicamente, essa classificação é imprecisa. A natureza compilada ou interpretada de uma linguagem é uma característica da implementação, não da linguagem em si. Na prática, é perfeitamente possível criar um compilador para uma linguagem geralmente considerada interpretada ou desenvolver um interpretador para uma linguagem geralmente vista como compilada.

Mesmo ao desconsiderarmos essa tecnicidade, o título de uma linguagem como "interpretada" ou "compilada" permanece obscuro, com controvérsias em relação a exemplos práticos. Essa ambiguidade é atribuída, em parte, ao fato de que muitas linguagens, especialmente aquelas rotuladas como interpretadas, frequentemente adotam abordagens mistas. Por isso, serão tratadas definições teóricas nesta seção e exemplos particulares mais a frente no artigo.

É considerado que em uma linguagem compilada, o desenvolvedor escreve o código em uma linguagem de programação, e todo o código é convertido integralmente em linguagem de máquina durante o processo de compilação. Esse resultado é um executável independente que pode ser executado sem a necessidade do código-fonte original. Esse método proporciona uma execução rápida, pois a tradução para código de máquina ocorre durante a compilação, otimizando completamente o código para o sistema alvo.

Em contrapartida, linguagens interpretadas não geram um executável. Cada linha do código é convertida em código de máquina em tempo real por um interpretador, que é necessário durante toda a execução do programa. Embora a execução seja mais lenta em comparação com linguagens compiladas, a vantagem está na ausência de uma etapa de compilação, permitindo a execução imediata do código assim que é escrito.

A compilação pode ser um processo demorado, mas oferece benefícios, como a total otimização do código, a ausência da responsabilidade de conversão do código durante execução e a privacidade do código-fonte, já que apenas o executável é distribuído. Por outro lado, em linguagens interpretadas, o próprio código-fonte é executado, proporcionando facilidade de distribuição, mas expondo o código ao ambiente de execução.

No contexto de linguagens compiladas, o executável resultante não é multiplataforma, requerendo recompilação para cada sistema em que será executado. Em contraste, linguagens interpretadas podem ser executadas em qualquer sistema que possua o interpretador correspondente. Contudo, a execução nesse caso fica dependente do interpretador, o que pode ser considerado uma desvantagem.

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
x = "Pinhalzinho - SP" // gera erro de compilação
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

A programação procedural, pertencente à categoria de programação imperativa, é caracterizada pela estruturação do programa em procedimentos. Estes procedimentos consistem em trechos distintos de instruções que se comunicam entre si para alcançar um objetivo específico.

A estruturação por procedimentos confere à programação procedural a vantagem da reusabilidade do código, uma vez que um mesmo procedimento pode ser invocado em diferentes partes do programa. Esta característica promove a modularidade e facilita a manutenção do código, por torná-lo menor e mais legível. Além disso, a atualização de um procedimento reflete automaticamente em todas as chamadas realizadas ao longo do código.

A programação procedural apresenta o menor nível de abstração entre os três paradigmas sendo apresentados. Em virtude de sua simplicidade e proximidade com o funcionamento interno de um computador, a programação procedural é mais amplamente adotada por linguagens de mais baixo nível, onde é exigido maior controle sobre o hardware e o desempenho é crítico.

```c
// Exemplo de uso do paradigma procedural:

int somar(int a, int b) {
    return a + b;
}

int calcular_media(float numeros[], int qt_numeros) {
    float soma = 0;
    for(int i=0; i < qt_numeros; i = i+=1)
        soma = somar(soma, numeros[i]);
    return soma / qt_numeros;
}

int main() {
    float media = calcular_media(1, 2, 3, 4);

    return 0;
}
```

### Programação Orientada a Objetos

A programação orientada a objetos (POO) é um paradigma imperativo amplamente adotado na atualidade, destacando-se como o mais popular entre os desenvolvedores. Nesse paradigma, um programa é estruturado em torno de objetos, entidades que possuem tanto atributos (dados) quanto métodos (comportamentos).

Em grande parte das linguagens de programação, os objetos são definidos por meio de classes. As classes são essencialmente descrições de quais características um objeto deve possuir e quais ações ele deve ser capaz de realizar. Os objetos são então instâncias concretas dessas classes, moldados conforme as especificações da classe.

Para ilustrar esse conceito, consideremos uma classe que define um cachorro com atributos como raça e nome, juntamente com métodos para latir e correr. Podemos criar diferentes instâncias dessa classe, como um cachorro da raça *Bulldog* Francês chamado Sushi e outro da raça *American Bully* chamado Zara. Além disso, podemos fazer os dois cachorros de fato latirem e até interagir um com outro (por exemplo, correr atrás do outro).

Além disso, o paradigma incorpora conceitos poderosos como a herança, que possibilita o reaproveitamento de código ao permitir que uma classe herde características e comportamentos de outra. Reutilizando o exemplo anterior, podemos ter uma classe Cachorro como base e criar subclasses específicas como *Bulldog* Francês e *American Bully*, herdando as características da classe principal. Isso proporciona uma organização hierárquica que reflete a relação entre diferentes tipos de cachorros.

O polimorfismo é outra característica relevante, permitindo que objetos de diferentes classes sejam tratados de maneira uniforme. No exemplo dos cachorros, podemos ter uma função que aceita qualquer instância de cachorro como parâmetro, independentemente da raça específica. Isso aumenta a flexibilidade e extensibilidade do código.

A POO é considerada a melhor maneira de modelar o mundo por meio de código. Essa metodologia proporciona não apenas reusabilidade de código e modularidade, características já presentes na programação procedural, mas também introduz abstração e encapsulamento. A comunicação com um objeto é realizada exclusivamente através de seus métodos, sem a necessidade de entender detalhes internos, o que favorece a colaboração em equipe e a construção de projetos complexos de maneira mais eficiente. Essa combinação de características faz da programação orientada a objetos uma escolha valiosa para o desenvolvimento de grandes projetos e o trabalho colaborativo entre desenvolvedores.

```python
# Exemplo de uso do paradigma orientado a objetos:

pessoa1 = Pessoa(nome="Edward Newgate")
pessoa2 = Pessoa(nome="Macaco Luffy")
cachorro1 = Cachorro(nome="Terremoto", dono=pessoa1)
cachorro2 = Cachorro(nome="Buda de Ouro Gigante", dono=pessoa2)

cachorro2.morder(cachorro1)
pessoa1.xingar(pessoa2)
pessoa2.pegar_cachorro(cachorro1)
pessoa2.correr()
```

### Programação Funcional

A programação funcional, um tipo de programação declarativa, difere das abordagens imperativas ao estruturar um programa através da declaração de funções, assemelhando-se a funções matemáticas. Essa abordagem possui o mais alto nível de abstração entre as três.

Uma característica fundamental da programação funcional é o tratamento das funções como "cidadãs de primeira classe", o que significa que elas podem ser atribuídas a constantes e variáveis, passadas como parâmetro para outras funções e retornadas por funções, como qualquer outro tipo de dado.

Uma característica marcante de linguagens puramente funcionais é a ausência do conceito de atribuição, eliminando a troca de valores de variáveis. Essa escolha é feita devido à complexidade que as atribuições trazem ao código, uma vez que é preciso levar em consideração o momento de execução para saber o valor de uma variável. Por isso, linguagens puramente funcionais evitam o uso de *loops*, recorrendo à recursão e a funções padrão da linguagem como substitutos, uma vez que *loops* necessitam do conceito de atribuição.

Outro aspecto distintivo é a presença de funções puras, que são determinísticas e sempre retornam o mesmo valor para o mesmo conjunto de argumentos. Essa previsibilidade é possível devido à ausência de dependência de fatores externos além dos argumentos, o que torna as funções independentes entre si. Essa independência facilita a programação concorrente, onde funções podem ser executadas simultaneamente sem interferências.

A proximidade da programação funcional com a matemática confere-lhe uma vantagem na redução de bugs e na possibilidade de verificação formal. No entanto, essa proximidade também pode resultar em um nível de abstração que, em conjunto com o distanciamento do real funcionamento de um computador, torna os programas mais difíceis de entender.

Embora linguagens predominantemente funcionais não alcancem a mesma popularidade de outras, é notável que muitos dos conceitos inovadores desse paradigma, quando integrados a abordagens de diferentes paradigmas, revelam-se extremamente poderosos. Essas ideias, combinadas de maneira sinérgica, são amplamente adotadas por linguagens mais difundidas e tem bastante espaço no desenvolvimento moderno.

```haskell
-- Exemplo de uso do paradigma funcional
fatorial :: Integer -> Integer
fatorial 0 = 1
fatorial n = n * fatorial (n - 1)

dobrarNumero :: Int -> Int
dobrarNumero x = 2 * x

main = do
    let x = fatorial 3    -- x = 6

    let y = [1, 2, 3, 4, 5]
    let z = map dobrarNumero y -- z = [2, 4, 6, 8, 10]

```

## Exemplos Reais

### C/C++

A linguagem C é notável por sua posição como uma linguagem de programação de nível mais baixo, destacando-se como uma linguagem procedural amplamente utilizada. Ela desempenha um papel fundamental na construção de sistemas operacionais, drivers, sistemas embarcados e até mesmo na implementação de compiladores e interpretadores para outras linguagens. Grande parte do que é usado hoje no dia a dia foi construído nas bases sólidas dessa linguagem.

Seu impacto não se limita apenas à sua aplicação direta, pois influenciou a criação de várias outras linguagens populares, como [JavaScript](#javascript) e [Java](#java). A simplicidade inerente à linguagem C é evidente em seu reduzido conjunto de palavras reservadas, tornando-a uma escolha simples para muitos desenvolvedores.

No entanto, sua simplicidade também se reflete em características que podem desafiar desenvolvedores, como o gerenciamento manual de memória, utilizando ponteiros para referenciar posições de memória. Essa abordagem pode levar a códigos mais propensos a erros de segurança. Dentre os exemplos presentes nesta seção, C e C++ são as únicas linguagens que não usam coletor de lixo para a desalocação automática de memória inutilizada.

Outro aspecto peculiar é a falta de estruturas de dados mais complexas, e a inexistência de um tipo de dado dedicado para strings, que são representadas como simples vetores de caracteres. A tipagem estática e fraca da linguagem C significa que, embora o compilador faça verificações de tipo, a primitividade dos tipos permite conversões implícitas. Caracteres, booleanos e ponteiros são representados como inteiros, proporcionando facilidade de conversão entre eles.

C++ surge como um superconjunto de C, acrescentando suporte à Programação Orientada a Objetos (POO). Apesar de compartilhar muitas características com C, como sua aplicação, a curva de aprendizado íngreme e uma tipagem mais forte também a diferenciam de seu subconjunto. Enquanto C é venerada por sua velocidade, C++ expande suas capacidades, especialmente em domínios onde a POO é essencial.

```c
// C:

#include <stdio.h>

int main() {
    int num1, num2;
    printf("Digite o primeiro numero: ");
    scanf("%d", &num1);

    printf("Digite o segundo numero: ");
    scanf("%d", &num2);

    int soma = num1 + num2;
    printf("A soma de %d com %d e: %d\n", num1, num2, soma);

    return 0;
}
```

```c++
// C++:

#include <iostream>

int main() {
    int num1, num2;
    std::cout << "Digite o primeiro numero: ";
    std::cin >> num1;

    std::cout << "Digite o segundo numero: ";
    std::cin >> num2;

    int soma = num1 + num2;
    std::cout << "A soma de " << num1 << " com " << num2 << " e: " << soma << std::endl;

    return 0;
}
```

### Javascript

JavaScript (JS) é uma linguagem de alto nível, reconhecida como uma das, se não a linguagem mais popular do mundo. Sua popularidade é impulsionada pelo fato de ser uma tecnologia fundamental na *World Wide Web*, com mais de 98% dos sites utilizando JS no *front-end*. Todos os navegadores mais utilizados possuem uma engine dedicada à execução de código JS.

Esta linguagem é conhecida por sua tipagem dinâmica e extremamente fraca, resultando em comportamentos por vezes bizarros e inconsistentes. Além disso, JS é multiparadigma, oferecendo suporte à orientação a objetos baseada em protótipo, uma alternativa às classes que dá dinamismo e flexibilidade ao código, e à programação funcional, incluindo, inclusive, o uso de funções de primeira classe. JS brilha especialmente na programação orientada a eventos, fazendo uso de sua capacidade para assincronicidade e manipulação do HTML através do DOM.

Apesar de fazer parte da especificação da linguagem (ECMAScript), muitos recursos importantes são fornecidos pelo sistema de execução, como no caso do browser. O loop de eventos não bloqueante, por exemplo, permite que, mesmo usando uma única thread, o JS trate de outras tarefas enquanto espera a resposta de APIs, bancos de dados ou outros agentes assíncronos.

O ecossistema do JavaScript é vasto, incluindo frameworks como Next.js, Angular e Vue.js, que são amplamente utilizados no desenvolvimento front-end. Outro destaque é a popularização do formato JSON, derivado do JS, mas adotado como padrão de mercado por inúmeras linguagens.

JavaScript é considerada uma linguagem interpretada, embora a realidade seja mais complexa hoje em dia. No motor V8, presente nos navegadores baseados em Chromium, o código é convertido em bytecode, que é interpretado inicialmente. À medida que o programa é executado, partes frequentemente usadas são convertidas para código de máquina nativo, garantindo maior rapidez na execução. Isso é chamado de compilação *Just-in-time*(JIT). Apesar disso, a execução de um programa JS ainda é feito a partir do código-fonte.

O motor V8, sendo independente de um navegador, possibilitou a expansão do uso do JavaScript para o back-end, através de ambientes como o Node.js. No back-end, JS também possui um amplo ecossistema, com o npm registrando o maior número de pacotes do mundo. Frameworks notáveis incluem Express, Fastify e Nest.js.

Assim como C, JavaScript também possui um superconjunto: TypeScript. TypeScript adiciona segurança e robustez da tipagem estática ao JavaScript, gerando código JS após a compilação. Essa evolução torna JS uma linguagem mais versátil, pois seu uso em sistemas de grande porte é favorecido.

```js
// JS no Front-End:

document.getElementById('botaoMudarTexto').addEventListener('click', function() {
  const elementoDeOutput = document.getElementById('output')
  elementoDeOutput.innerText = 'Texto mudado!'
})
```

```js
// JS no Back-End:

const http = require('http')

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' })
  res.end('Massa, meu irmão\n')
})

const port = 3000
server.listen(port, () => {
  console.log(`Servidor rodando em http://localhost:${port}/`)
})
```

```ts
// TypeScript:

function addNumbers(a: number, b: number): number {
  return a + b;
}

const num1: number = 5;
const num2: number = 10;
const result: number = addNumbers(num1, num2);
```

### Python

Python é uma linguagem de alto nível, multiparadigma e extremamente versátil, destacando-se em diversas áreas de aplicação. Ao lado de JavaScript, tornou-se uma das linguagens mais populares no cenário da programação moderna.

Uma característica marcante do Python é o seu foco na legibilidade e simplicidade do código. Para alcançar esse objetivo, a linguagem utiliza a identação como delimitador de bloco, em contraste com o uso de chaves em outras linguagens. Além disso, o uso de parênteses é minimizado, e muitos símbolos presentes em outras linguagens são substituídos por palavras do inglês, facilitando a compreensão do código.

Apesar de ser uma linguagem de tipagem dinâmica, o Python permite a utilização de anotações de tipo. Essas anotações servem não apenas para documentação, mas também para a verificação de tipos por meio de ferramentas externas, proporcionando um ambiente mais robusto para o desenvolvimento.

Embora Python seja majoritariamente uma linguagem de tipagem forte, é importante notar que ela realiza conversões implícitas de outros tipos para booleano, demonstrando uma flexibilidade que pode ser explorada de maneira estratégica.

Na implementação mais difundida, CPython, o código fonte é compilado para bytecode e, após isso, interpretado. Apesar desse processo, a execução de um programa ocorre a partir do código-fonte, com ambas as etapas sendo realizadas atomicamente.

Python é amplamente reconhecido por sua riqueza em recursos e pela presença de uma vasta biblioteca padrão. Além disso, a instalação de pacotes externos é facilitada pelo gerenciador de pacotes pip, e esses pacotes são hospedados no registro PyPI, que conta com os pacotes feitos por uma das maiores comunidades na esfera do desenvolvimento.

A linguagem é amplamente utilizada no desenvolvimento web back end, sendo suportada por frameworks como Django e Flask. Além disso, Python desempenha um papel crucial em campos como inteligência artificial e aprendizado de máquina, contando com bibliotecas renomadas como TensorFlow, Keras e PyTorch.

Na área de ciência de dados, Python é uma escolha popular, impulsionada por bibliotecas como NumPy, Pandas e Matplotlib, que oferecem ferramentas poderosas para análise e visualização de dados, além das bibliotecas de IA citadas. Adicionalmente, Python é frequentemente empregado na automação, onde uma variedade de bibliotecas pode ser explorada para simplificar e otimizar tarefas automatizadas em diferentes contextos.

```python
# Python:

def soma_quadrados_se_par(lista):
    return sum(x**2 for x in lista if x % 2 == 0)

numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
resultado = soma_quadrados_se_par(numeros)
print(f"A soma dos quadrados dos números pares em {numeros} é: {resultado}")

```

### Java



## Fontes

[Compiled vs Interpreted Programming Languages | What’s the Difference? - YouTube](https://youtu.be/F64_bwahaWQ?si=231_k91GpdvCPmJk)

[Static vs Dynamic Typing | Which languages are better? - YouTube](https://youtu.be/GqXpFycPWLE?si=vXei9EWiijcXiTaQ)

[Static VS Dynamic Programming Languages 🤔 | WHAT'S THE DIFFERENCE? - YouTube](https://youtu.be/bCIFTWQorL0?si=eHUNDQtGOmKLAial)

[Typing: Static vs Dynamic, Weak vs. Strong / Intro to JavaScript ES6 programming, lesson 16 - YouTube](https://youtu.be/C5fr0LZLMAs?si=wLLbSbyw4SrbX5ia)

[Programming paradigm - Wikipedia](https://en.wikipedia.org/wiki/Programming_paradigm)

[Introduction of Programming Paradigms - GeeksforGeeks](https://www.geeksforgeeks.org/introduction-of-programming-paradigms/)

[Dear Functional Bros - YouTube](https://youtu.be/nuML9SmdbJ4?si=DT0aT1OfnTfsfvaJ)

[Functional programming - A general introduction - YouTube](https://youtu.be/8z_bUIl_uPo?si=ER_PFJvuvp8Gdv2Y)

[C (programming language) - Wikipedia](https://en.wikipedia.org/wiki/C_(programming_language))

[C++ - Wikipedia](https://en.wikipedia.org/wiki/C%2B%2B)

[JavaScript - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

[Usage Statistics of JavaScript as Client-side Programming Language on Websites, February 2024](https://w3techs.com/technologies/details/cp-javascript)

[Understanding the V8 JavaScript Engine - YouTube](https://youtu.be/xckH5s3UuX4?si=ox4aZI4zr6tA2tJM)

[Franziska Hinkelmann: JavaScript engines - how do they even? | JSConf EU - YouTube](https://youtu.be/p-iiEDtpy6I?si=FqMWP5J8KeWzs4Xx)

[TypeScript - Wikipedia](https://en.wikipedia.org/wiki/TypeScript)

[Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

[Python Data Science Handbook | Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)

[Python in 100 Seconds - YouTube](https://youtu.be/x7X9w_GIm1s?si=GlIHBCQoMrM9nR66)
