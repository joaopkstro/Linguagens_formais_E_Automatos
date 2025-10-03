- - -
### Questões sobre o Processo de Compilação em Java

1. Qual é a principal diferença entre o processo de compilação em Java e o de linguagens C++?
	- A principal diferença é que a compilação em Java é um processo de duas etapas que produz um código intermediário chamado **bytecode**. Esse bytecode é então interpretado pela **Máquina Virtual Java (JVM)**. Já em C++, a compilação é um processo de etapa única que gera um **código de máquina nativo** executável diretamente pelo sistema operacional.
2. Explique o que acontece em cada uma das três fases de análise do compilador javac: Análise Léxica, Análise Sintática e Análise Semântica.
	- No compilador **javac**:
		- **Análise Léxica:** O código-fonte é lido e dividido em pequenas unidades chamadas **tokens** (palavras-chave, identificadores, operadores, etc.).
		- **Análise Sintática:** A sequência de tokens é verificada para garantir que segue a **gramática** da linguagem Java. Se a sintaxe estiver correta, uma Árvore Sintática Abstrata (AST) é construída.
		- **Análise Semântica:** A lógica do código é checada. O compilador verifica se as variáveis foram declaradas e se os tipos de dados são compatíveis, por exemplo.
3. O que é o bytecode e qual é a sua principal função no processo de compilação do Java?
	- O **bytecode** é um código intermediário gerado pelo compilador `javac`. Sua principal função é atuar como uma "linguagem" universal que pode ser entendida por qualquer **JVM**, independentemente do sistema operacional. Isso torna o Java portátil, permitindo que o mesmo arquivo `.class` seja executado em diferentes plataformas (Windows, Linux, macOS).
4. Qual é o papel da Máquina Virtual Java (JVM) na execução de um programa Java, e por que o arquivo ".class" não é executado diretamente pelo sistema operacional?
	- A **Máquina Virtual Java (JVM)** é a "máquina" que executa o bytecode. 
	- O arquivo `.class` não é executado diretamente pelo sistema operacional porque ele não contém instruções nativas para o processador do seu computador. A JVM traduz as instruções do bytecode para o código de máquina específico do sistema operacional em que está rodando.
5. O que é o compilador JIT e como ele melhora o desempenho dos programas em Java?
	- O compilador **JIT** (**Just-In-Time**) é um otimizador da JVM. Ele monitora o programa em execução e identifica as partes do código ==que são usadas com mais frequência==. O JIT, então, compila essas partes para código de máquina nativo, que é mais rápido, melhorando significativamente o desempenho do programa.

### Questões sobre Linguagens Formais em Java

6. Qual é a aplicação mais comum e direta das linguagens formais em Java,  e para que ela é utilizada?
	- A aplicação mais comum e direta das linguagens formais em Java são as **Expressões Regulares (Regex)**, usadas para buscar e substituir padrões de texto e para **validação de entrada**, como verificar se um e-mail ou CPF tem um formato válido.
7. No processo de compilação de um código Java, como as linguagens formais são usadas nas fases de Análise Léxica e Análise Sintática?
	- No processo de compilação, as linguagens formais são usadas de duas formas principais:
		- **Análise Léxica:** A linguagem dos tokens de Java é uma **linguagem regular**, reconhecida por um **Autômato Finito (AF)**.
		- **Análise Sintática:** A sintaxe do Java é uma **linguagem livre de contexto**, que é analisada por um **autômato de pilha**, verificando se a estrutura do código está correta.
8. O que é uma Máquina de Estado Finito (FSM) e como ela pode ser usada em Java?
	- Uma **Máquina de Estado Finito (FSM)** é um modelo computacional que pode reconhecer linguagens regulares. Em Java, ela pode ser usada para modelar sistemas que mudam de estado com base em eventos, como o exemplo do semáforo, onde a classe `Semafaro` com seus estados e transições é uma FSM.
9. Como as linguagens formais se relacionam com os schemas de validação de documentos, como os usados para XML e JSON?
	- As linguagens formais se relacionam com os schemas de validação de XML e JSON porque esses schemas atuam como **gramáticas formais**. Eles definem a estrutura e os tipos de dados que um documento deve seguir para ser considerado válido. O programa que valida o documento contra o schema age como um **autômato**, decidindo se o documento pertence à linguagem definida pelo schema.
10. De acordo com o texto, qual é a principal utilidade de ferramentas como o ANTLR no contexto de linguagens formais em Java?
	- De acordo com o texto, a principal utilidade de ferramentas como o **ANTLR** é automatizar a criação de **analisadores (parsers)**. Isso permite que um desenvolvedor defina a gramática de uma linguagem e o ANTLR gere o código Java para reconhecê-la, simplificando o processo de criação de compiladores e interpretadores.
