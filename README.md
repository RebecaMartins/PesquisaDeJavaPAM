# PesquisaDeJava
 Pesquisa sobre tipos de dados no java.

As estruturas de dados condicionais e de repetição são importantes para a maioria das linguagens de programação. Nesta pesquisa apresentaremos alguns dos tipos de dados primitivos, de referência, estrutura condicional e estrutura de repetição no java.


Dados de referência:

Definição: Os tipos por referência são classes que irão especificar os tipos de Strings, Arrays primitivos e Objetos. Os programas utilizam as variáveis de tipos referência para armazenar a localização de objetos na memória do computador. Para trazer em algum objeto os seus métodos de instância ele precisa ter referência a algum objeto. As variáveis de referência são inicializadas com um valor nulo ("null").

Por exemplo:
ClasseConta acao = new ClasseConta(), cria um objeto de classe ClasseConta e a variável acao contém a tal referência a esse objeto ClasseConta, onde poderá mostrar quais são todos os seus métodos e atributos da classe (todos os dados que se encontram dentro desse atributo/classe). 

OBS:
 As variáveis de tipos por algum valor não se referem a objetos, e não podem ser utilizadas para invocar métodos.
> Lembrando que as variáveis locais não são inicializadas por padrão (variáveis encontradas dentro dos métodos).
 As variáveis de tipo primitivo não podem ser inicializadas com referência a algum objeto (não se aplicam a eles).


OBJETOS - ARRAYS:
Definição: Arrays ou matrizes são conhecidas pelo Java, que fazem parte do pacote java.util na coleção API do Java. Eles são objetos recipientes que contém um número fixos de valores de um único tipo. O comprimentos de um array é definido quando ele é criado, e depois que a criação é oficializada seu comprimento fica fixo. Cada item de um array é chamado elemento e cada elemento é acessado pelo número, chamado índice. A cada acesso de elemento sempre irá começar a numeração com 0.

EX:
3      41       28       79       7
0       1        2        3       4

- um array de 5 elementos.



Declarando ARRAYS:
Para declarar qualquer array, cada elemento irá receber um valor padrão, sendo 0(zero) para os números de classificação primitiva, falso(false) para os elementos de classificação booleana e nulo(null) para os elementos de classificação de referência. O programa que está na primeira listagem (1) cria um array de inteiros, e coloca alguns valores nela para a saída padrão desse valor.

EX de declaração de array:

public class Declaracao_Array {
    public static void main(String[] args) {
        //[] - são inseridos em uma variável que referecia um array
        int[] a = new int[4];
        
EX de declaração de vários arrays:

        int[] r = new int[44], k = new int[23];
        
Ex de iniciação de um array em sua declaração:

        int[] iniciaValores = {12,32,54,6,8,89,64,64,6};

Ex de declaração de um array de inteiros:

        int[] meuArray;
        

Ex de inicialização do primeiro elemento:

       meuArray [0] = 100;
        meuArray [1] = 85;
        meuArray [2] = 88;
        meuArray [3] = 93;
        meuArray [4] = 123;
        meuArray [5] = 952;
        meuArray [6] = 344;
        meuArray [7] = 233;
        meuArray [8] = 622;
        meuArray [9] = 8522;
        //meuArray [10] = 564; //ESTOURA A PILHA POIS NÃO EXISTE O ÍNDICE 10

        System.out.println(meuArray[9]);
        System.out.println(meuArray[2]);
    } 
//essa chave é o fechamento do topo (declaração inicial)//    

ARRAYS MULTIDIMENSIONAIS:
Esse tipo de array é declarado como ele tendo duas dimensões e é usado para representar tabelas de valores que ficam agrupados em linhas e colunas.
Os arrays bidimensionais precisam de dois índices para identificar um elemento em particular. Por exemplo, quando um array é identificado dessa forma “numero[indiceA][indiceB]”, a variável numero é o array, o indiceA é a linha e o indiceB é identificado como a coluna, fazendo uma identificação de cada elemento no array por número de linha e coluna (similar ao funcionamento da formação das próprias matrizes).
EX:
a[m][n] - a[2][0]
m - linha
n - coluna
>>> no exemplo
m = 2
n = 0


ESTRUTURAS CONDICIONAIS:
Definição: O poder de controlar quais serão as tarefas e trechos de códigos a serem digitados em diferentes situações, como os valores de variáveis, sendo assim possivel fazer o programa alterar o fluxo da execução do mesmo baseado nas decisões tomadas. Elas geralmente analisam expressões booleanas e caso elas sejam verdadeiras um trecho do código será executado, no caso contrário (serem falsas) outro trecho será executado.

If/Else:
É uma estrutura de condição em que uma expressão booleana será analisada, quando a condição que estiver dentro do if for verdadeira ela será executada. Já o else tem a função de definir o que é executado quando a condição que foi apresentada no if for falsa. Caso o if for verdadeiro será executado, já o else não precisará ser executado.
O if pode ser executado com o else ou não, se necessário.

EX onde if e else são usados:

public class Exemplo {
	
    public static void main(String[] args) {
        int resposta = 10;
        if (resposta == 10) {
            // Se a variável for igual a 10, a frase abaixo será escrita
            System.out.println(“Você acertou!”); //aqui é definida a mensagem
        } else { // aqui a condição é fechada
            // Caso contrário, a frase abaixo será escrita
            System.out.println(“Você errou!”);
        }
    }
	}

Ex só com o if:
 
public class Exemplo {
	
    public static void main(String[] args) {
        int resposta = 10;
        if (resposta == 10) { 
            // Se a variável for igual a 10, a frase abaixo será escrita
            System.out.println(“Você acertou!”);
        }
        // Se a variável não for igual a 10, nenhuma frase será exibida pois não usamos o else, então o programa fecha sem apresentar nada
    }
	}
 
EX encadeado: 

public class Exemplo {
	
    public static void main(String[] args) {
        int resposta = 10;
        if (resposta == 10) { 
            System.out.println(“A resposta é exatamente 10!”);
        } else if (resposta > 10) {
            System.out.println(“A resposta é maior que 10!”);
        } else { // aqui temos duas opções de resultado a ser apresentado
            System.out.println(“A resposta é menor que 10!”);
        }
    }
}  


Switch/Case:
Definição: servem de alternativa quando precisamos usa múltiplos ifs no código.
Muitos if/else encadeados (ligados) deixam o código muito extenso (longo e complicado), pouco legível e com baixo índice de manutenção. Outra principal função do switch/case é testar o valor que está contido em uma variável e realizar cada uma das opções (etapas). Cada uma das possíveis opções é delimitada (marcada) pela instrução case. Podemos ter diversos casos a serem análisados que forem necessários, e quando um dos valores for correspondente ao valor da variável, o código do case será executado. Já se a variável não corresponder a nenhum dos casos testaos o último bloco será executado, chamado default (padrão).

EX usando switch/case:

public class Exemplo {
	
    public static void main(String[] args) {
        int mes = 2; //valores a serem calculados
        switch (mes) {
            case 1:
                System.out.println(“O mês é janeiro”);
                break; 
            case 2:
                System.out.println(“O mês é fevereiro”);
                break;
            case 3:
                System.out.println(“O mês é março”);
                break;
            case 4:
                System.out.println(“O mês é abril”);
                break;
            case 5:
                System.out.println(“O mês é maio”);
                break;
            case 6:
                System.out.println(“O mês é junho”);
                break;
            case 7:
                System.out.println(“O mês é julho”);
                break;
            case 8:
                System.out.println(“O mês é agosto”);
                break;
            case 9:
                System.out.println(“O mês é setembro”);
                break;
            case 10:
                System.out.println(“O mês é outubro”);
                break;
            case 11:
                System.out.println(“O mês é novembro”);
                break;
            case 12:
                System.out.println(“O mês é dezembro”);
                break;
            default:
                System.out.println(“Mês inválido”);
                break;
        }
    }
	
}


REFERÊNCIAS:
https://www.devmedia.com.br/tipos-de-dados-por-valor-e-por-referencia-em-java/25293
https://www.devmedia.com.br/trabalhando-com-arrays-em-java/25530
https://www.treinaweb.com.br/blog/estruturas-condicionais-e-estruturas-de-repeticao-em-java
