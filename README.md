Documentação do Projeto: Cadastro e Catálogo de Livros
1. Introdução

O projeto Cadastro e Catálogo de Livros foi desenvolvido em Python com o objetivo de criar uma estrutura simples para cadastrar, armazenar e visualizar livros em um catálogo.

A aplicação utiliza conceitos de Programação Orientada a Objetos (POO), funções, listas e estruturas de repetição. Cada livro cadastrado possui informações como título, autor, quantidade disponível e gênero.

O projeto foi desenvolvido como uma atividade acadêmica para aplicar na prática conceitos fundamentais da linguagem Python e da organização de dados.

2. Objetivo

O principal objetivo do projeto é permitir o cadastro de livros e a organização dessas informações em um catálogo.

O sistema permite:

Criar objetos que representam livros;
Armazenar informações sobre cada livro;
Adicionar novos livros ao catálogo;
Registrar o gênero dos livros;
Listar todos os livros cadastrados;
Exibir a quantidade disponível de cada livro.
3. Tecnologias utilizadas

A principal linguagem utilizada no desenvolvimento foi:

Python — utilizada para desenvolver toda a lógica do sistema.

Também foi utilizada a biblioteca:

Matplotlib — importada no projeto para possibilitar a criação de representações gráficas dos dados, embora não seja utilizada na versão atual do código.
4. Estrutura do projeto

O projeto é dividido principalmente em três partes:

Classe livro — responsável por definir as características de cada livro.
Função adicionar_livro() — responsável por criar e cadastrar novos livros.
Função listar_catalogo() — responsável por exibir os livros cadastrados.

Além disso, são utilizadas as listas catalogo e generos para armazenar os dados.

5. Classe Livro

A classe livro funciona como um modelo para os objetos que serão criados no sistema.

Ela recebe quatro informações:

titulo — nome do livro;
autor — autor da obra;
quantidade_disponivel — quantidade disponível;
genero — gênero do livro.

O método __init__ é responsável por receber essas informações e armazená-las no objeto.

Exemplo:

class livro:
    def __init__(self, titulo, autor, quantidade_disponivel, genero):
        self.titulo = titulo
        self.autor = autor
        self.quantidade_disponivel = quantidade_disponivel
        self.genero = genero

Dessa maneira, cada livro criado possui seus próprios valores para título, autor, quantidade e gênero.

6. Representação dos livros

O método __str__ foi utilizado para definir como as informações do livro serão apresentadas quando o objeto for exibido.

def __str__(self):
    return (
        f"Título: {self.titulo} | "
        f"Autor: {self.autor}, "
        f"Quantidade Disponível: {self.quantidade_disponivel}, "
        f"Gênero: {self.genero}"
    )

Isso permite que o programa apresente os dados de cada livro de maneira organizada, facilitando a leitura do catálogo.

7. Armazenamento dos dados

Foram criadas duas listas:

catalogo = []
generos = []

A lista catalogo armazena os objetos de livros cadastrados.

Já a lista generos armazena os gêneros informados durante o cadastro.

A utilização de listas permite que novos elementos sejam adicionados durante a execução do programa.

8. Função adicionar_livro()

A função adicionar_livro() é responsável pelo cadastro dos livros.

def adicionar_livro(titulo, autor, quantidade_disponivel, genero):
    novo_livro = livro(titulo, autor, quantidade_disponivel, genero)
    catalogo.append(novo_livro)
    generos.append(genero)
    print(f"Livro '{titulo}' adicionado com sucesso!")

O funcionamento ocorre da seguinte maneira:

A função recebe os dados do livro;
Um novo objeto da classe livro é criado;
O objeto é adicionado à lista catalogo;
O gênero é armazenado na lista generos;
O sistema informa que o cadastro foi realizado com sucesso.
9. Função listar_catalogo()

A função listar_catalogo() é responsável por apresentar todos os livros armazenados no catálogo.

def listar_catalogo():
    print("\n--- Catálogo de Livros ---")
    for livro in catalogo:
        print(livro)

Foi utilizada uma estrutura for para percorrer todos os elementos da lista catalogo.

A cada repetição, um livro é exibido utilizando o método __str__.

10. Cadastro dos livros

Na execução inicial foram cadastrados quatro livros:

adicionar_livro("Boa noite punpun", "Oyasumi Punpun", 1, "Slice of life")

adicionar_livro("Dragon ball Z", "Akira Toriyama", 2, "Ação")

adicionar_livro("Berserker", "Kentaro Miura", 1, "Fantasia")

adicionar_livro("Look Back", "Tatsuki Fujimoto", 1, "Coming of Age")

Após o cadastro, a função listar_catalogo() apresenta os livros registrados.

11. Exemplo de resultado

A execução do programa apresenta uma saída semelhante a:

Livro 'Boa noite punpun' adicionado com sucesso!
Livro 'Dragon ball Z' adicionado com sucesso!
Livro 'Berserker' adicionado com sucesso!
Livro 'Look Back' adicionado com sucesso!

--- Catálogo de Livros ---

Título: Boa noite punpun | Autor: Oyasumi Punpun,
Quantidade Disponível: 1, Gênero: Slice of life

Título: Dragon ball Z | Autor: Akira Toriyama,
Quantidade Disponível: 2, Gênero: Ação

Título: Berserker | Autor: Kentaro Miura,
Quantidade Disponível: 1, Gênero: Fantasia

Título: Look Back | Autor: Tatsuki Fujimoto,
Quantidade Disponível: 1, Gênero: Coming of Age

Também é possível adicionar novos livros após a criação do catálogo. Por exemplo:

adicionar_livro(
    "Blue Lock",
    "Muneyuki Kaneshiro",
    4,
    "Futebol"
)

O sistema então apresenta:

Livro 'Blue Lock' adicionado com sucesso!

O novo livro passa a fazer parte do catálogo e será exibido na próxima execução da função listar_catalogo().

12. Lógica utilizada

A lógica principal do projeto consiste em criar uma classe para representar os livros e utilizar funções para controlar o cadastro e a exibição dessas informações.

Primeiramente, o programa define quais características um livro possui. Depois, a função adicionar_livro() cria um novo objeto e armazena esse objeto na lista catalogo.

Por fim, a função listar_catalogo() percorre a lista utilizando um laço for e apresenta cada livro cadastrado.

Dessa forma, o projeto demonstra a utilização conjunta de classes, objetos, funções, listas e estruturas de repetição.

13. Fluxo de funcionamento

O funcionamento pode ser representado pelo seguinte fluxo:

Início
   ↓
Definição da classe Livro
   ↓
Criação das listas de armazenamento
   ↓
Cadastro de um livro
   ↓
Criação do objeto Livro
   ↓
Armazenamento no catálogo
   ↓
Cadastro dos demais livros
   ↓
Listagem do catálogo
   ↓
Exibição dos livros cadastrados
   ↓
Fim
14. Conceitos de programação utilizados

O projeto permitiu aplicar diversos conceitos estudados em Python:

Classes e objetos

A classe livro define um modelo para a criação dos objetos que representam cada livro.

Funções

As funções adicionar_livro() e listar_catalogo() organizam as principais operações do sistema.

Listas

As listas catalogo e generos são utilizadas para armazenar informações durante a execução.

Laço de repetição

O for da função listar_catalogo() percorre todos os livros cadastrados.

Encapsulamento de informações

Cada objeto possui suas próprias informações, como título, autor, quantidade e gênero, permitindo organizar os dados de cada livro separadamente.

15. Possíveis melhorias

Apesar de cumprir o objetivo inicial da atividade, o projeto pode ser expandido futuramente.

Algumas melhorias possíveis seriam:

Criar uma opção para o usuário cadastrar os livros pelo teclado;
Criar uma função para remover livros;
Criar uma função para pesquisar livros pelo título ou autor;
Permitir alterar a quantidade disponível;
Criar filtros por gênero;
Evitar o cadastro de livros com informações inválidas;
Criar uma interface gráfica;
Utilizar a biblioteca Matplotlib para gerar gráficos com a quantidade de livros por gênero;
Utilizar um banco de dados para manter os livros salvos mesmo depois que o programa for encerrado.
16. Conclusão

O projeto Cadastro e Catálogo de Livros possibilitou a aplicação prática de conceitos fundamentais da programação em Python.

A utilização de uma classe para representar os livros tornou possível organizar as informações de cada item de maneira estruturada. As funções desenvolvidas também ajudaram a separar as responsabilidades do programa, tornando o código mais organizado.

Além disso, o projeto serviu para praticar conceitos como Programação Orientada a Objetos, funções, listas, objetos e estruturas de repetição, criando uma base para o desenvolvimento de sistemas mais completos no futuro.
