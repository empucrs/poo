# Ambiente de trabalho da disciplina de POO

Este documento tem por objetivo descrever os recursos básicos a serem empregados na disciplina de Programação Orientada a Objetos. Além dos recursos, também são detalhadas as atividades a serem desenvolvidas como mecanismo de reforço/revisão do conhecimento esperado para esta primeira etapa.
O restante deste documento apresenta os detalhes citados.

## Ambiente de programação
Há diferentes ambientes (IDEs) que podem ser utilizadas para a codificação. Dentre as possiveis, detaca-se as ferramentas [Microsoft Visual Studio Code (vscode)](https://code.visualstudio.com/download) e a [Eclipse.](https://www.eclipse.org/downloads/). Ambas ferramentas tem como vantagens serem multiplataforma, não terem custo além de permiterem a instalação de plugins que permite sua extensão para uso do git, *synthax highlight*, entre outras características.

Apesar de ter citado estas duas ferramentas, sinta-se livre para escolher a ferramenta que considerar mais adequada para o desenvolvimento do seu trabalho. Durante a realização das atividades em sala de aula, será explorada a ferramenta eclipse, por já estar disponível nas imagens das máquinas do parque computacional da universidade.

## Ambiente de controle de versionamento

  Ao longo do semestre, usaremos uma ferramenta de controle de versão dos códigos elaborados. O objetivo deste tipo de recurso é garantir que tenhamos um controle das modificações que foram realizadas sobre um dado código elaborado. Sendo assim, é importante ter em mente que somente os códigos fonte devem ser armazenados no ambiente de controle de versão.
  
  Há um diferentes recursos que podem ser utilizados para controle de versão, tais como SVN, CVS. Adicionalmente, existe o GIT (em uso neste momento). Por ser uma ferramenta online e disponível de modo gratuito, ele será utilizado nesta disciplina. Sendo assim, será disponbilizado um espaço para experimentação e compartilhamento de usos deste serviço.
  
### Criando uma conta no **GITHUB*

  Como dito, o objetivo é utilizarmos o github como ferramenta de versionamento. Sendo assim, é necessária a criação de uma conta.
  Acesse o [github](http://github.com), e clique no link **sign up**. Preencha os dados básicos solicitados. Sua conta será explorada nas atividades previstas neste docmento.

## Atividades

Na presente seção busca-se explorar assuntos descritos neste documento bem como relembrar atividade de codificação realizada no passado.

### Atividade 1 - Compilação por linha de comando

Copie o trecho de código abaixo e salve em um arquivo de nome **teste.java** em um diretório de sua preferencia. 

```java
public class teste{

  public static void main(String [] args){
  
    System.out.println("Olá mundo maravilhoso da Orientação a Objetos!!!");
  
  }

}
```

Para a compilação via linha de comando, abra um terminal. No Windows, use as teclas "windows+r", digite o *cmd* e tecle *ENTER*. Desloque-se até o diretório onde o arquivo teste.java foi salvo. Lá, digite o comando **javac teste.java**. O javac é o compilador da linguagem java que faz a "tradução" do arquivo .java para o aruqivo .class, que contem o bytecode executável pela máquina virtual java (JVM).

Uma vez obtido o arquivo teste.java, a partir da compilação com o javac, deve-se utiliar o comando java para lançar o programa. Para tanto, digite **_java teste_**.

Como resultado deste último comando, o texto *Olá mundo maravilhoso da Orientação a Objetos!!!* deverá ser apresentado na tela.

### Atividade 2 - Exploração do ambiente de versionamento (ignore esta atividade se não houver um cliente git na sua máquina)

Considere partir de um código disponível no github, elaborado por um terceiro. O Objetivo é que voce assuma este código para um repositório seu e a partir daí tenha controle sobre as modificações que voce desejar.

Para tanto, vamos utilizar o código disponivel no [repositorio Aula01-Atividade02](https://github.com/empucrs/Aula01-Atividade02). Este código deverá ser "assumido" em sua conta, baixado de lá, modificado e posteriormente atualizado no github. Ao "assumir" o repositório, o resultado será a realização de uma cópia do estado atual daquele repositório para a sua conta. Assim, pode-se modificar este repositório "assumido" sem causar danos a versão original. Para "assumir" um repositório, acesse o mesmo e, considerando que voce esteja logado em sua conta do github, clique na opção **fork**. O resultado final é, como dito, uma cópia do repositório desejado em sua conta.

O passo seguinte deve ser a validação do código "assumido". Acesse seu projeto e baixe para o seu computador. Caso voce tenha o cliente git instalado em sua máquina, basta abrir o console e digitar o comando **_git clone http://github.com/<seueEspaço>/nomeDoRepositorio.git**. Será feita uma clonagem do seu código. Avance nas pastas até encontrar os arquivos principal.java e carro.java. Em seguida, digite o seguinte comando no console: **_javac *.java_**. Como resultado, serão criados dois arquivos .class (principal.class e carro.class). Execute o código a partir do comando **_java principal_** e manipule os menus. 

A seguir, modifique os arquivos .java. Crie um método toString para a classe carro, que deve imprimir a quilometragem e a qtde de litros disponivel no carro quanto utilizado o comando de impressão System.out.println. Na classe principal, crie uma entrada no menu que permita a chamada do método toString da classe carro. Valide para garantir que suas modificações estão funcionando corretamente. Uma vez validado, salve tais arquivos no seu repositorio do github. Para isto, os seguintes passos deverão ser realizados:

1. Identifique quem voce é no console
1.1. git config --global user.name "seu nome de usuário"
1.2. git config --global user.email "o mail que cadastrou no seu perfil"
2. Observe o que foi modificado
2.1. git status
3. Salve localmente as modificações
3.1. git commmit -am "insira uma mensagem que deixe claro a modificação que foi realizada nos arquivos que serão salvos"
4. Transfira para o github
4.1. git push
4.1.1. Nesta etapa, será solicitado seu username e senha de acesso ao github
5. Teste se sua modificação no github foi salva
5.1. crie um diretorio tmp em um local a parte
5.2. Execute o comando de clonagem novamente (**_git clone http://github.com/<seueEspaço>/nomeDoRepositorio.git**)
5.3. Abra os arquivos .java e confira se as últimas modificações estão presente.

### Atividade 3 - Modelagem e implementação de software

Desenvolva um programa em java considerando a seguinte descrição:

Elabore um programa que permita o cadastramento de funcionários e departamentos de uma empresa. A empresa deve ter no máximo 5 departamentos. Os funcionários podem ser de 3 tipos: (a) operários, (b) secretário ou (c) Gerente. Cada departamento deve ter exatamente um gerente e um secretário e no máximo 5 funcionários. Para evitar confitos na empresa, a diferença salarial entre os funcionários de um departamento deve ser de no máximo de 20%. Ao final, deve ser possível listar os funcionários, os departamentos e os departamentos e seus funcionários.

Salve seu código no github
