# Miniguia de Estudos: Programação Orientada a Objetos em Python com NotebookLM

## Contexto e Objetivos
Este repositório foi criado para o desafio Treinando uma IA de Aprendizagem: Explore o Poder do NotebookLM para o Bootcamp Afya - Automação de Dados com IA.

Com o objetivo de ser uma fonte de aprendizado ativa. O assunto escolhido foi **Programação Orientada a Objetos (POO) em Python**. Procuro consolidar conceitos que considero fundamentais e que muitas vezes geram dúvidas em desenvolvedores iniciantes e intermediários, transformando documentação em um guia de estudo prático e visual.

## Curadoria de Fontes
Para servir como base de  dados do NotebookLM e garantir respostas precisas e fundamentadas (como um RAG), foram selecionadas as seguintes fontes abertas e oficiais:

1. **Documentação Oficial do Python (Tutorial - Classes):** [docs.python.org/3/tutorial/classes.html](https://docs.python.org/3/tutorial/classes.html) - Fonte primária para sintaxe e comportamento oficial.
2. **PEP 8 – Style Guide for Python Code:** [peps.python.org/pep-0008/](https://peps.python.org/pep-0008/) - Para garantir que os exemplos gerados sigam as boas práticas de formatação da comunidade.
3. ** Python Full Course For Beginners (Learn How To Code in 2025) - PORTUGUESE:** [https://www.youtube.com/watch?v=Lc5LKDqhyzs.]
4. ** Como Funcionam Classes e Programação Orientada a Objetos em Python - Aprenda em 10 Minutos!:** [https://www.youtube.com/watch?v=97A_Cyyh-eU]

## Engenharia de Prompts e "Cicatrizes"

### Prompt 1: Tentativa Inicial com foco amplo
* **O que perguntei:** *"Me explica POO em Python."*
* **Resultado:** A IA trouxe uma resposta genérica, com muito texto e um exemplo básico de uma classe `Pessoa` que não aprofundava nos pilares do paradigma.
* **Cicatrização:** Percebi que precisava restringir o escopo e pedir um formato específico para facilitar o estudo.

### Prompt 2: Refinado com foco em cenário prático
* **O que perguntei:** *"Com base nas fontes fornecidas, explique o conceito de Herança e Polimorfismo em Python. Crie um cenário prático do mundo real (como um sistema de RPG) e mostre o código aplicando a convenção da PEP 8. Separe a explicação teórica do código."*
* **Resultado:** Excelente. A IA utilizou as fontes para explicar como uma classe `ClasseMae` passa atributos para a `ClasseFilha` e gerou um exemplo limpo.
* **Dificuldade Encontrada:** O NotebookLM inicialmente esqueceu de aplicar o método `super()` da forma correta no exemplo. Tive que corrigi-lo com um prompt de acompanhamento: *"No código anterior, a inicialização da classe filha não usou o super(). Corrija isso aplicando as melhores práticas."*

* ## Miniguia de Estudo (Entrega Final)

### Resumo Estruturado: Os 4 Pilares de POO em Python

1. **Abstração:** Isolamento de um objeto do mundo real para o cenário do sistema, focando apenas nos atributos e métodos que importam para o contexto.
2. **Encapsulamento:** Proteção dos dados internos de uma classe. Em Python, usamos o prefixo de um underline `_` (protegido) ou dois underlines `__` (privado/name mangling) para indicar restrição de acesso.
3. **Herança:** Capacidade de uma classe herdar características e comportamentos de outra (reutilização de código). `class Carro(Veiculo):`.
4. **Polimorfismo:** Capacidade de subclasses redefinirem métodos de uma classe super (métodos com assinaturas iguais, mas comportamentos diferentes).

### Glossário com os Principais Conceitos
* **Classe:** O "molde" ou "planta baixa" para a criação de objetos.
* **Objeto:** A instância real e tangível baseada em uma classe.
* **Método Construtor (`__init__`):** O método especial executado automaticamente quando um novo objeto é criado, usado para inicializar os atributos.
* **`self`:** Representa a própria instância do objeto que está chamando o método, permitindo acessar os atributos e métodos da classe.

### Prompts Reutilizáveis
Você pode copiar e colar estes prompts no seu NotebookLM para revisar a matéria:

* *Prompt de Simulado:* `"Com base no caderno de estudos de POO, aja como um entrevistador técnico de Python. Me faça 3 perguntas teóricas de nível intermediário, uma por vez, e aguarde minha resposta para me dar um feedback."`
* *Prompt de Refatoração:* `"Aqui está um bloco de código procedural [inserir código]. Com base nos conceitos de POO das nossas fontes, reescreva este código utilizando classes e aplicando o pilar do Encapsulamento."`
