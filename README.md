# ES3A3 
Repositório dedicado ao aprendizado da disciplina de Engenharia III com o professor Leonardo Bertholdo. 

<h2>Conceitos</h2>

* <strong>Projeto de Software</strong>: é o processo de desenvolvimento da aplicação como um todo.
* <strong>Modelo de Software</strong>: é uma representação abstrata do software que será desenvolvido,  incluindo componentes, métodos, classes e etc.
* <strong>Modelo de Projeto</strong>: é a representação de “como” o software será desenvolvido, incluindo arquitetura utilizada, componentes e interface e etc. 
* <strong>Modelo de Desenvolvimento de Software</strong>: é uma abordagem utilizada para a construção do software, definindo cronograma, atividades e etapas. Podendo utilizar o modelos como : cascata, RAD, XP e ágil. 
* <strong>Arquitetura de software</strong>: é a forma ou organização dos componentes dentro do software, e a maneira que eles interagem entre si. Um exemplo, é a arquitetura MVC, SOA, Repositório e etc.

<Strong><h2>Design Patterns (Padrões de Projeto):</h2></strong> 
Padrão de Projeto: descreve uma abordagem de sucesso, amplamente testada, para um determinado problema. Possibilitando o reúso desse padrão em outros projetos. Afinal, na maioria dos casos, não é necessário “reinventar a roda”. Segundo o livro "Design Patters" da GOF (Gang of Four), há 23 padrões de projeto (Design patters). Os mais conhecidos são :
- Padrões de Comportamento: Observer
- Padrões de Criação: Singleton e Factory
- Padrões Estruturais: Facade e Adapter

<strong><h2> IHC (Interação Humano-Computador)</h2></strong>
<p>IHC é uma disciplina interessada no projeto, implementação e avaliação de sistemas computacionais interativos para uso humano, juntamente com os fenômenos relacionados a esse uso.</p>

<p>IHC é uma área multidisciplinar que se beneficia de conhecimentos e métodos de outras áreas, fora da Computação, para conhecer melhor os fenômenos que envolvem o uso de sistemas interativos. Áreas como psicologia, semiótica, sociologia, antropologia, constribuem para a aquisição de conhecimento sobre a cultura dos usuários</p>



<h2>Relacionamentos entre objetos</h2>
	
	
* <strong>Associação:</strong> É uma forma de relacionamento entre objetos em que o objeto (todo) pode estar apenas associado a um objeto (parte), segundo a definição do professor : "Na associação, o objeto (todo) só pode estar associado a um único objeto (parte)". Além disso, esses objetos também são independentes entre si. Por exempo, duas classes : Pessoa e Cidade. Nesse cenário, uma pessoa (todo) pode ter residência em APENAS UMA cidade. Se, porventura, uma pessoa tiver residência em mais de uma cidade, esse relacionamento se torna uma agregação, não mais uma associação. 
* <strong>Composição:</strong> é uma forma de relacionamento entre objetos em que um objeto é composto por outros. Esses objetos componentes são partes essenciais do objeto todo e não existem de forma independente. Em outras palavras, o objeto todo é responsável pela criação (via construtor) e destruição dos objetos parte. Se o objeto (todo) for excluído, os objetos (parte) também serão. Vale ressaltar que esse tipo de relacionamento é, geralmente, 1 -> N, sendo o objeto (parte) um arraylist do tipo especificado. Por exemplo, duas classes : Funcionário(todo) e Dependentes(parte). Nesse cenário, teremos um atributo chamado dependentes, sendo um arraylist do tipo Dependentes, dentro da classe Funcionário. Se o todo (funcionário) for excluído, as partes (dependentes) também serão.
* <strong>Agregação:</strong> Na agregação, você tem um objeto (todo) que contém outros objetos (parte) como atributos, mas esses objetos (parte) podem existir de forma independente do objeto (todo). Em outras palavras, o objeto (parte) pode pertencer a vários objetos todo ao mesmo tempo e não é destruído quando um objeto (todo) é excluído. Vale ressaltar, assim como na composição, que esse tipo de relacionamento é, geralmente, 1 -> N, sendo o objeto (parte) um arraylist do tipo especificado. Porém, diferente da composição, ao excluir o objeto (todo), as (partes) permancem existindo. Por exemplo, duas classes : Cesta de Produtos(todo) e Produtos(parte). Uma cesta de produto é, geralmente, constituida de 1 -> N produtos. No entanto, ambas funcionam como entidades autônomas. Logo, um produto pode existir em diversas cestas e, se eu excluir o mesmo da Cesta de Produto, ele apenas será removido; não será uma exclusão do objeto em si. 
Observação: o produto será adicionado por métodos específicos (add) dentro da classe Cesta de Produtos, já que o mesmo não é criado no momento da instanciação (via construtor) da classe Cesta, mas feito à parte.

Associação:

* Relação genérica entre objetos de classes diferentes.
* Indica uma conexão ou interação entre os objetos.
* Os objetos associados são independentes e podem existir separadamente.
* Não implica uma dependência forte entre os objetos.
* Exemplo: uma pessoa possui um carro, mas o carro pode pertencer a diferentes pessoas.

Composição:

* Relação de "todo-parte" entre objetos, em que um objeto todo é composto por objetos parte.
* Os objetos parte são componentes essenciais do objeto todo.
* Existe uma dependência forte, em que a existência do objeto parte está intimamente ligada ao objeto todo.
* Se o objeto todo for excluído, os objetos parte também serão.
* Exemplo: um computador possui uma CPU, memória e disco rígido, e esses componentes são partes essenciais do computador.

Agregação:

* Uma forma específica de associação que também envolve uma relação de "todo-parte".
* O objeto todo é composto por objetos parte, mas estes podem existir independentemente do objeto todo.
* Os objetos parte podem estar associados a outros objetos além do objeto todo.
* Existe uma dependência mais fraca em comparação com a composição.
* Exemplo: uma universidade possui estudantes, mas os estudantes podem existir fora do contexto da universidade e podem ser associados a * outras instituições de ensino.

Diferenças:

<p align="justify">Na associação, os objetos são independentes e podem existir separadamente, enquanto na composição os objetos parte são componentes essenciais do objeto todo e na agregação os objetos parte podem existir independentemente do objeto todo.
Na composição, a existência do objeto parte está fortemente ligada ao objeto todo, e se o objeto todo for excluído, os objetos parte também serão. Na agregação, os objetos parte podem existir independentemente do objeto todo e não são excluídos quando o objeto todo é excluído.
Na composição, a criação e gerenciamento dos objetos parte são responsabilidade do objeto todo. Na agregação, os objetos parte podem ser criados separadamente e associados ao objeto todo por meio de métodos específicos. A composição é uma relação mais forte e mais restritiva do que a agregação.</p>

