# Ambiente de trabalho da disciplina de POO

Este documento tem por objetivo descrever os recursos básicos a serem empregados na disciplina de Programação Orientada a Objetos. Além dos recursos, também são detalhadas as atividades a serem desenvolvidas como mecanismo de reforço/revisão do conhecimento esperado para esta primeira etapa.
O restante deste documento apresenta os detalhes citados.

## Ambiente de programação

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


### Atividade 2 - Exploração do ambiente de versionamento

Considere partir de um código disponível no github, elaborado por um terceiro. O Objetivo é que voce assuma este código para um repositório seu e a partir daí tenha controle sobre as modificações que voce desejar.

Para tanto, vamos utilizar o código disponivel 

### Atividade 3 - Modelagem e implementação de software
