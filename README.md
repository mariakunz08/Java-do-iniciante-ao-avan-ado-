# Java-do-iniciante-ao-avançado-
Repositório das minhas aulas de Java - do inicial ao avançado

Inciei no mês de fev. um curso de Java. Estarei disponibilizando aqui meus códigos, tanto para ajudar colegas da área tanto para deixar salvo. 

---------------------------------------------------------------------------------------------------------------------------------------------------
Faça um programa para ler dois valores inteiros, e depois mostrar na tela a soma desses números com uma 
mensagem explicativa, conforme exemplos

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner (System.in);

        int n1, n2;
        double soma;

        n1 = sc.nextInt();
        n2 = sc.nextInt();

        soma = n1+ n2;

        System.out.println("A soma eh: "+soma);

        sc.close();

    }
}

------------------------------------------------------------------------------------------------------------------------------------
Códifo simples usando operadores (&) e condição (if/else)

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        int horas;
        System.out.println("Que horas?");
        horas = sc.nextInt();

        if(horas>=5 && horas <12){
            System.out.println("Bom dia");
        }
        if(horas>=12 && horas<18){
            System.out.println("Boa tarde");
        }
        else{
            System.out.println("Boa noite");}

        sc.close();

    }
}
----------------------------------------------------------------------------------------------------------------------------------

Fazer um programa para ler um número inteiro e dizer se este número é par ou ímpar.

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        int numero;
        System.out.println("Entre com um número: ");
        numero = sc.nextInt();

        if(numero%2==0){
            System.out.println("O numero é par");
        }

        else{
            System.out.println("O número é ímpar!");
        }

        sc.close();

    }
}


----------------------------------------------------------------------------------------------------------------------------------------------------------
Leia a hora inicial e a hora final de um jogo. A seguir calcule a duração do jogo, sabendo que o mesmo pode 
começar em um dia e terminar em outro, tendo uma duração mínima de 1 hora e máxima de 24 horas.


import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        int hora_inicial, hora_final, duracao = 0;
        System.out.println("Entre com a hora inicial: ");
        hora_inicial = sc.nextInt();

        System.out.println("Entre com a hora final: ");
        hora_final = sc.nextInt();

        if(hora_inicial >= 1 && hora_final<=24){
            duracao = hora_final - hora_inicial;
            System.out.println("O jogo durou: " + duracao);
        }

        if(hora_inicial<1){
            System.out.println("O jogo durou menos de 1 hora!");
        }

        if(duracao>24){
            System.out.println("O jogo durou mais de 24 horas!");
        }

        sc.close();

    }

---------------------------------------------------------------------------------------------------------------------------------------------------

Uma empresa de telefoni dá ao seu cliente 100min por R$50,00, porém a cada min. ultrapassado, é cobrado o valor de R$2,00/min. Faça um código:

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        int hora_total, alteracao;

        System.out.println("Entre com a quantidade que ficou em ligacao: ");
        hora_total = sc.nextInt();

        if(hora_total <= 100){
            System.out.println("A conta deu R$50,00");
        }

        if(hora_total > 100){
            alteracao = ((hora_total-100)*2)+50;
            System.out.println("A conta deu " + alteracao);
        }


        sc.close();

    }
}

----------------------------------------------------------------------------------------------------------------------------------------------------------
Fazer um programa utilizando Switch case para identificar o dia da semana quanto entra um n°:

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        int x;
        String dia = "0";

        System.out.println("Entre com o dia da semana (numero 1-7): ");
        x = sc.nextInt();

        switch(x) {
            case 1:
                dia = "Domingo";
                break;
            case 2:
                dia = "Segunda-feira";
                break;
            case 3:
                dia = "Terça-feira";
                break;
            case 4:
                dia = "Quarta-feira";
                break;
            case 5:
                dia = "Quinta-feira";
                break;
            case 6:
                dia = "Sexta-feira";
                break;
            case 7:
                dia = "Sábado";
                break;
            default:
                System.out.println("Opção inválida!");
                break;
        }

        System.out.println("Dia da semana " + dia);
        sc.close();

    }
}

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Fazer um código utilizando o laço de repetição while. Ler vários numeros, mas ao receber o 0 deve terminar o programa e mostrar a soma dos numeros digitados. 

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        int numero = 1, contador = 0;


        while(numero != 0){
            System.out.print("Digite um numero: ");
            numero = sc.nextInt();
            contador = numero + contador;
        }
        System.out.printf("Sai do laço, a soma dos numero digitados é: " + contador);
    sc.close();

    }
}

----------------------------------------------------------------------------------------------------------------------------------

Fazer um código utilizando o laço de repetição FOR para ser executado por n vezes e mostrar no final a soma de todos o n° digitados; 

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner (System.in);

        System.out.print("Digite quantas vezes será executado o laço for: ");
        int n = sc.nextInt();

        int i, soma = 0;

        for(i=0;i<n;i++){
            System.out.print("Digite o " + i + "° número:");
            int x = sc.nextInt();

            soma = soma+x;
        }
         System.out.print("O laço foi repetido " + n + " vezes e a soma de todos os n° digitados é " + soma);

    sc.close();

    }
}


----------------------------------------------------------------------------------------------------------------
fACA UM PROGRMA QUE CONTROLE O ESTOQUE. PEÇA O NOME DO PRODUTO, VALOR E QUANTIDADE EXISTANTE. DEPOIS PEÇA A QUANTIDADE QUE PRECISA ADD E DEPOIS A QUANTIDADE QUE PRECISA REMOVER

import java.util.Scanner;

public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    Produtc produtc = new Produtc();

    System.out.println("Enter product data");
    System.out.print("Name: ");
    produtc.name = sc.nextLine();

    System.out.print("Price: ");
    produtc.price = sc.nextInt();

    System.out.print("Quantity in stock: ");
    produtc.quantity = sc.nextInt();

    System.out.println(produtc);
    System.out.print("How many quantity do you want add at stock?");
    int quantity = sc.nextInt();
    produtc.addProducts(quantity);

    System.out.println("Uptade date: " + quantity+ " quantity was add at stock");
    System.out.println(produtc);

    System.out.print("How many quantity do you want remove of stock?");
    quantity = sc.nextInt();
    produtc.removeProduct(quantity);

    System.out.println("Uptade date: " + quantity+ " quantity was remove at stock");
    System.out.println(produtc);

    sc.close();
    }

}

public class Produtc{
    public String name;
    public double price;
    public int quantity;

    public double totalValueInStock(){
        return price*quantity;
    }

    public void addProducts(int quantity){
        this.quantity += quantity;
    }

    public void removeProduct(int quantity){
        this.quantity -= quantity;
    }

    public String toString(){
        return name + ", R$" + price + ", " + quantity + " units, total R$" + totalValueInStock();
    }

}


-----------------------------------------------------------------------------------------------------------------------

Fazer um programa que receba o valor do raio, calcula volume e circunferencia. 

public class Produtc{
    public double radious;

    public double valueCircunferencia(){
        return 2 * 3.1415 * radious;
    }

    public double valueVolume(){
        return 3.1415 * radious * radious;
    }

    public String toString(){
        return "Value of circunferencia " + valueCircunferencia() + "Value of volume" + valueVolume();
    }

}

import java.util.Scanner;

public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    Produtc produtc = new Produtc();

    System.out.println("How is the radiuos?");
    produtc.radious = sc.nextDouble();

    System.out.print(produtc);

    sc.close();
    }

}
-----------------------------------------------------------------------------------------------------------------

fazer um programa que receba o valor do dolar e a quantidade que quer comprar, aplicar um taxa e retornar o valor final para o usuario

public class Converter{
    public double valueDolar;
    public double dolarBought;

    public double converter(){
        double totalValue = valueDolar * dolarBought;
        double iof = totalValue * 0.06; // 6% de IOF
        return totalValue + iof;
    }

    public String toString(){
        return "You need to pay in reais: " + String.format("%.2f", converter());
    }

}

import java.util.Scanner;

public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    Converter converter = new Converter();

    System.out.println("How is the value of dolar?");
    converter.valueDolar = sc.nextDouble();

    System.out.println("How many dolar do you want bought?");
    converter.dolarBought = sc.nextDouble();

    System.out.print(converter);

    sc.close();
    }

}

----------------------------------------------------------------------------------------------------------------------------------

Faça um programa que leia um número inteiro positivo N (máximo = 10) e depois N números inteiros 
e armazene-os em um vetor. Em seguida, mostrar na tela todos os números negativos lidos. 

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos numeros voce vai digitar?  ");
    int n = sc.nextInt();

    int [] vect = new int[n];

    for (int i=0; i<vect.length; i++) {
        System.out.print("Digite um numero: ");
        vect [i] = sc.nextInt();
    }

    System.out.println();
    System.out.println("Numeros negativos:");
    for(int i=0; i<vect.length; i++) {
        if(vect[i] < 0) {

            System.out.println(vect[i]);
        }
    }

    sc.close();
    }

}

-------------------------------------------------------------------------------------------------------------------------

Faça um programa que leia N números reais e armazene-os em um vetor. Em seguida: 
- Imprimir todos os elementos do vetor
- - Mostrar na tela a soma e a média dos elementos d

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos numeros voce vai digitar? ");
    int n = sc.nextInt();

    int [] vect = new int[n];

    for (int i=0; i<vect.length; i++) {
        System.out.print("Digite um numero: ");
        vect [i] = sc.nextInt();
    }

    System.out.println();
    int soma = 0, media = 0;
    System.out.println("Valores:");
    for(int i=0; i<vect.length; i++) {
        System.out.println(vect[i]);
        soma = soma + vect[i];
    }
    media = soma/n;
    System.out.println("Soma: " + soma);
    System.out.println("Média: " + media);

    sc.close();
    }

}
--------------------------------------------------------------------------------------------------------------------------------

Fazer um programa para ler nome, idade e altura de N pessoas, conforme exemplo. Depois, mostrar na 
tela a altura média das pessoas, e mostrar também a porcentagem de pessoas com menos de 16 anos, 
bem como os nomes dessas pessoas caso houver. 


import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos pessoas serão digitadas? ");
    int n = sc.nextInt();

    Product[] vect = new Product[n];

    for (int i=0; i<vect.length; i++) {

        System.out.println("Dados da " + (i + 1) + "a pessoa");
        sc.nextLine();
        System.out.print("Nome: ");
        String nome = sc.nextLine();

        System.out.print("Idade: ");
        int idade = sc.nextInt();

        System.out.print("Altura: ");
        double altura = sc.nextDouble();

        vect [i] = new Product(nome, idade, altura);
    }

    System.out.println();

    double soma = 0, media = 0;



    for(int i=0; i<vect.length; i++) {
        soma = soma + vect[i].getAltura();

    }
    media = soma/n;


    int contador = 0;

    System.out.println("Altura média: " + media);

    for(int i=0; i<vect.length; i++) {

        if (vect[i].getIdade() < 16) {
            contador ++;
        }
    }

    double porcentagem = (contador / n) * 100;

    System.out.println("Porcentagem menor de 16 anos: " + porcentagem);

        
    for(int i=0; i<vect.length; i++) {

        if (vect[i].getIdade() < 16) {
           System.out.println("Menores de 16 anos: " + vect[i].getName());
        }
    }
    sc.close();
    }

}


public class Product {

    public String name;
    public int idade;
    public double altura;


    public Product (String name, int idade, double altura){
        this.name = name;
        this.idade = idade;
        this.altura = altura;

    }

    public void setName(String name){
        this.name = name;
    }

    public String getName(){
        return name;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }

    public void setAltura(double altura) {
        this.altura = altura;
    }

    public double getAltura() {
        return altura;
    }

    public double media (double altura){
        return altura;
    }



}

------------------------------------------------------------------------------------------------------------------------------------

Faça um programa que leia N números inteiros e armazene-os em um vetor. Em seguida, mostre na 
tela todos os números pares, e também a quantidade de números pares. 

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos números serão digitadas? ");
    int n = sc.nextInt();

    int contador = 0;

    int [] vect = new int[n];

    for (int i=0; i<vect.length; i++) {

        System.out.print("Digite o " + (i +1) +  "° número: ");
        vect[i] = sc.nextInt();
    }
    System.out.println("Números pares: ");
    for (int i=0; i<vect.length; i++) {
        if (vect[i] % 2 == 0){
            contador ++;
            System.out.println(vect[i]);
        }

    }

    System.out.println("Qauntidade de numeros pares: " + contador);


    sc.close();
    }

}

--------------------------------------------------------------------------------------------------------------------------------

Faça um programa que leia N números reais e armazene-os em um vetor. Em seguida, mostrar na tela 
o maior número do vetor (supor não haver empates). Mostrar também a posição do maior elemento, 
considerando a primeira posição como 0 (zero). 

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos números serão digitadas? ");
    int n = sc.nextInt();

    int contador = 0;

    int [] vect = new int[n];

    for (int i=0; i<vect.length; i++) {

        System.out.print("Digite o " + (i +1) +  "° número: ");
        vect[i] = sc.nextInt();
    }

        double maior = vect[0];
        int posmaior = 0;

        for (int i=1; i<n; i++) {
            if (vect[i] > maior) {
                maior = vect[i];
                posmaior = i;
            }
        }

        System.out.printf("MAIOR VALOR = %.1f\n", maior);
        System.out.printf("POSICAO DO MAIOR VALOR = %d\n", posmaior);
    sc.close();
    }

}
----------------------------------------------------------------------------------------------------------------------------------

Faça um programa para ler dois vetores A e B, contendo N elementos cada. Em seguida, gere um 
terceiro vetor C onde cada elemento de C é a soma dos elementos correspondentes de A e B. Imprima 
o vetor C gerado. 


import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos valores vai ter cada vetor? ");
    int n = sc.nextInt();

    int [] vecta = new int[n];
    int [] vectb = new int[n];
    int [] vectc = new int[n];

    for (int i=0; i<vecta.length; i++) {

        System.out.print("Digite os valores do vetor a: ");
        vecta[i] = sc.nextInt();
    }

    for (int i=0; i<vectb.length; i++) {

        System.out.print("Digite os valores do vetor b: ");
        vectb[i] = sc.nextInt();

    }

    for (int i=0; i<vectc.length; i++) {
        vectc[i] = vecta[i]+vectb[i];
        System.out.printf(" " + vectc[i]);
    }
    sc.close();
    }

}

-----------------------------------------------------------------------------------------------------------------------------------
Fazer um programa para ler um número inteiro N e depois um vetor de N números reais. Em seguida, 
mostrar na tela a média aritmética de todos elementos com três casas decimais. Depois mostrar todos 
os elementos do vetor que estejam abaixo da média, com uma casa decimal cada. 


import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos valores o vetor vai ter? ");
    int n = sc.nextInt();

    int [] vecta = new int[n];


double media=0, soma = 0;
    for (int i=0; i<vecta.length; i++) {

        System.out.print("Digite o " + (i+1) + "° valor: ");
        vecta[i] = sc.nextInt();
        soma = soma + vecta[i];
    }

    media = soma/n;

    System.out.println("Media do vetor: " + media);
    System.out.print("Elementos abaixo da media:");

    for(int i=0; i<vecta.length; i++) {
        if (vecta[i] < media) {
            System.out.print(" " + vecta[i]);
        }
    }

    sc.close();
    }

}
------------------------------------------------------------------------------------------------------------------------------



Fazer um programa para ler um vetor de N números inteiros. Em seguida, mostrar na tela a média 
aritmética somente dos números pares lidos, com uma casa decimal. Se nenhum número par for 
digitado, mostrar a mensagem "NENHUM NUMERO PAR" 

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantos valores o vetor vai ter? ");
    int n = sc.nextInt();

    int [] vecta = new int[n];


double media=0, soma = 0;
    for (int i=0; i<vecta.length; i++) {
        System.out.print("Digite o " + (i+1) + "° valor: ");
        vecta[i] = sc.nextInt();
        if(vecta[i] % 2 == 0){
            soma = soma + vecta[i];
        }
    }

    media = soma/n;

    if(soma > 0){
        System.out.println("Media dos numeros pares digitados: " + media);
    }

    else{
        System.out.println("Nenhum numero par");
    }

    sc.close();
    }

}

-----------------------------------------------------------------------------------------------------------------------------------

Fazer um programa para ler um conjunto de nomes de pessoas e suas respectivas idades. Os nomes 
devem ser armazenados em um vetor, e as idades em um outro vetor. Depois, mostrar na tela o nome 
da pessoa mais velha. 

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantas pessoas você vai digitar? ");
    int n = sc.nextInt();

    int [] idade = new int[n];
    String [] nomes = new String[n];
    
    for (int i=0; i<n; i++) {
        System.out.println("Dados da " + (i+1) + "° pessoa: ");
        sc.nextLine();
        System.out.print("Entre com o nome ");
        nomes[i] = sc.nextLine();
        System.out.print("Idade ");
        idade[i] = sc.nextInt();

        }
    int maiorIdade = idade[0];
    int posicaoMaior = 0;

    for (int i=1; i<n; i++) {
        if(idade[i] > maiorIdade){
            maiorIdade = idade[i];
            posicaoMaior = i;
        }
    }
    System.out.print("Nome da pessoa com a maior idade: " + nomes[posicaoMaior]);
    sc.close();
    }
}

--------------------------------------------------------------------------------------------------------------------------------

Fazer um programa para ler um conjunto de N nomes de alunos, bem como as notas que eles tiraram 
no 1º e 2º semestres. Cada uma dessas informações deve ser armazenada em um vetor. Depois, imprimir 
os nomes dos alunos aprovados, considerando aprovados aqueles cuja média das notas seja maior ou 
igual a 6.0 (seis).

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantas pessoas você vai digitar? ");
    int n = sc.nextInt();


    String [] nomes = new String[n];
    int [] nota1 = new int[n];
    int [] nota2 = new int[n];

    for (int i=0; i<n; i++) {
        System.out.println("Dados da " + (i+1) + "° aluno: ");
        sc.nextLine();
        System.out.print("Entre com o nome ");
        nomes[i] = sc.nextLine();
        System.out.print("nota 1 ");
        nota1[i] = sc.nextInt();
        System.out.print("nota 1 ");
        nota2[i] = sc.nextInt();

        }
    double media = 0;
    String aprovado = nomes[0];
    int posicao = 0;

    for (int i=1; i<n; i++) {
        media = nota1[i] + nota2[i];
        if(media > 6){
            aprovado = nomes[i];
            posicao = i;
        }
    }
    System.out.print("Aprovados: " + nomes[posicao]);
    sc.close();
    }
}

-------------------------------------------------------------------------------------------------------------------------------
Tem-se um conjunto de dados contendo a altura e o gênero (M, F) de N pessoas. Fazer um programa 
que calcule e escreva a maior e a menor altura do grupo, a média de altura das mulheres, e o número 
de homens. 

import java.util.Scanner;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    System.out.print("Quantas pessoas você vai digitar? ");
    int n = sc.nextInt();


    char [] genero = new char[n];
    double  [] altura = new double[n];


    for (int i=0; i<n; i++) {
        System.out.println("Dados da " + (i+1) + "° pessoa: ");
        sc.nextLine();
        System.out.print("Entre com o genero (f/m) ");
        genero[i] = sc.next().charAt(0);
        System.out.print("Entre com a altura ");
        altura[i] = sc.nextDouble();
        }


    double maiorAltura = altura[0], menorAltura = altura[0], mediaAltura = 0, soma = 0;
    int contadorF = 0, contadorM = 0;

    for (int i=1; i<n; i++) {
        if(altura[i] > maiorAltura){
            maiorAltura = altura[i];
        }
    }

    for (int i=1; i<n; i++) {
        if(altura[i] < menorAltura){
            menorAltura = altura[i];
        }
    }

    for (int i=0; i<n; i++) {
        if(genero[i] == 'f'){
            contadorF++;
            soma = soma + altura[i];
        }
    }
    for (int i=0; i<n; i++) {
        if(genero[i] == 'm'){
            contadorM++;
        }
    }

    mediaAltura = soma/contadorF;

    System.out.println("Maior altura: " + maiorAltura);
    System.out.println("Menor altura: " + menorAltura);
    System.out.printf("Media altura feminina: %.2f\n", mediaAltura);
    System.out.println("Quantidade de homens: " + contadorM);

    sc.close();
    }
}


------------------------------------------------------------------------------------------------------------------------

No código abaixo contém várias operações com LIsta, por exemplo: como adicionar, como adicionar passandou o local, como remover, remover pelo nome, usando uma função lampda para idexar apenas quem começa com x letra ou removendo quem começa com n letra, encontrando posição.......

import java.util.List;
import java.util.ArrayList;
import java.util.Scanner;
import java.util.stream.Collectors;

    public class Main {

    public static void main(String [] args){

    Scanner sc = new Scanner(System.in);

    List<String> list = new ArrayList<>();

    list.add("Maria"); //adiciona Maria
    list.add("Momo"); //adiciona Momo
    list.add("Karina");//adiciona Karina
    list.add("Soph"); //adiciona Soph
    list.add("Suzy"); //adiciona Suzy
    list.add(1, "Paulo");//adiciona Paulo
    list.remove("Suzy"); //remove suzy
    list.remove(4); // remove karina
    list.add("Marilusa");// adiciona Marilusa


    for (String x : list){
        System.out.println(x);
    }

    System.out.println("O tamanho da lista é: " + list.size());
    System.out.println("-------------------------------");

    list.removeIf(x -> x.charAt(0) == 'P');
    for (String x : list){
        System.out.println("Removendo quem começa com a letra P ");
    }
    for (String x : list){
            System.out.println("Ficou na lista: " + x);
    }
    System.out.println("-------------------------------");
    System.out.println("Encontrando Karina na posição: " + list.indexOf("Karina"));

    List<String> result = list.stream().filter(x -> x.charAt(0) == 'M').collect(Collectors.toList());
    for (String y : result){
            System.out.println("Deixando só quem começa com M " + y);
    }

    System.out.println("-------------------------------");
    String name = list.stream().filter(x -> x.charAt(0) == 'M').findFirst().orElse(null);
    System.out.print(name);
    sc.close();
    }
}

-------------------------------------------------------------------------------------------------------------------

criando matrizes 

import java.util.ArrayList;
import java.util.List;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite o numero: ");
        int numero = sc.nextInt();

        int [][] matrix = new int [numero][numero];

        for (int i=0; i<numero; i++){
            for(int j =0; j<numero; j++){
                System.out.print("Entre com o valor da linha " + (i+1) + " e coluna " + (j+1) + ": ");
                matrix[i][j] = sc.nextInt();
            }
        }
        System.out.println("Dioagonal principal: ");
        for (int i=0; i<numero; i++){
            System.out.print(matrix[i][i] + " ");
        }
        int contador = 0;
        for (int i=0; i<numero; i++){
            for(int j =0; j<numero; j++){
                if(matrix[i][j] < 0 ){
                    contador++;
                }
            }
        }

        System.out.print("A quantida de numero negativos é: " + contador);



        sc.close();


    }
}


-------------------------------------------------------------------------------------------------------------------------

 Fazerumprogramaparalerdoisnúmeros inteirosMeN,edepois ler
 umamatriz deMlinhas porNcolunas contendonúmeros inteiros,
 podendohaver repetições. Emseguida, lerumnúmero inteiroXque
 pertenceàmatriz. Para cadaocorrênciadeX,mostrar os valores à
 esquerda, acima, àdireitaeabaixodeX, quandohouver, conforme
 exemplo.

import java.util.ArrayList;
import java.util.List;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Digite a qtd de linha: ");
        int linha = sc.nextInt();

        System.out.print("Digite a qtd de coluna: ");
        int coluna = sc.nextInt();

        int [][] matrix = new int [linha][coluna];

        for (int i=0; i<linha; i++){
            for(int j =0; j<coluna; j++){
                System.out.print("Entre com o valor da linha " + (i+1) + " e coluna " + (j+1) + ": ");
                matrix[i][j] = sc.nextInt();
            }
        }
        System.out.println("Entre com um numero : ");
        int x = sc.nextInt();

        for (int i=0; i<linha; i++){
            for(int j =0; j<coluna; j++){
                if(matrix[i][j] == x ){
                    System.out.println("Posição " + i + "," + j + ":");
                    if(j>0) {
                        System.out.println("Esquerda: " + matrix[i][j - 1]);
                    }
                    if(i>0) {
                        System.out.println("Em cima: " + matrix[i-1][j]);
                    }
                    if (j < matrix[i].length-1) {
                        System.out.println("Direita: " + matrix[i][j+1]);
                    }
                    if (i < matrix.length-1) {
                        System.out.println("A baixo: " + matrix[i+1][j]);
                    }
                }
            }
        }





        sc.close();


    }
}


----------------------------------------------------------------------------------------------------------------------------------
public class Departamento{

    private String nome;

    public Departamento(){

    }

    public Departamento(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }
}

import java.util.Date;

public class ContratoHora {

    private Date data;
    public Double valorPorHora;
    private Integer hora;

    public ContratoHora(){
    }

    public ContratoHora(Date data, Double valorPorHora, Integer hora) {
        this.data = data;
        this.valorPorHora = valorPorHora;
        this.hora = hora;
    }

    public Date getData() {
        return data;
    }

    public void setData(Date data) {
        this.data = data;
    }

    public Double getValorPorHora() {
        return valorPorHora;
    }

    public void setValorPorHora(Double valorPorHora) {
        this.valorPorHora = valorPorHora;
    }

    public Integer getHora() {
        return hora;
    }

    public void setHora(Integer hora) {
        this.hora = hora;
    }
    public double valorTotal(){
        return valorPorHora*hora;
    }
}

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Scanner;

public class Main {
    public static void main (String[] args) throws ParseException {
        Scanner sc = new Scanner(System.in);
        SimpleDateFormat sdf = new SimpleDateFormat("dd/MM/yyyy");

        System.out.print("Entre com o nome do departamento(junior/intermediario/senior): ");
        String departamento = sc.nextLine();
        System.out.println("Entre com os dados do trabalhador:");
        sc.nextLine();
        System.out.print("Nome: ");
        String nome = sc.nextLine();
        System.out.print("Cargo: ");
        String cargo = sc.nextLine();
        System.out.print("Salario base: ");
        double salarioBase = sc.nextInt();
        sc.nextLine();

        Trabalhador trabalhador = new Trabalhador(nome, Cargo.valueOf(cargo), salarioBase, new Departamento(departamento));

        System.out.print("Quantos contratos esse trabalhador tem: ");
        int numeroContratos = sc.nextInt();
        sc.nextLine();

        for(int i=0; i<numeroContratos;i++){
            System.out.print("Entre com o contrato numero " + (i+1) + ": ");

            System.out.print("Entre com a data (DD/MM/AAAA): ");
            Date contratoData = sdf.parse(sc.next());

            System.out.print("Valor por hora: ");
            double valorPorHora = sc.nextDouble();

            System.out.print("Duração(horas): ");
            int hora = sc.nextInt();
            sc.nextLine();

            ContratoHora contratoHora = new ContratoHora(contratoData, valorPorHora, hora);
            trabalhador.addContratos(contratoHora);
        }

        System.out.println();
        sc.nextLine();
        System.out.print("Entre com o mes e ano para calcular o quanto recebeu (mm/yyyy): ");
        String mesAno = sc.nextLine();
        int mes = Integer.parseInt(mesAno.substring(0,2));
        int ano = Integer.parseInt(mesAno.substring(3));
        System.out.print("NoME: " + trabalhador.getName());
        System.out.print("Departamento: " + trabalhador.getDepartamento().getNome());
        System.out.print("Recebido: " + mesAno + " " + String.format("%.2f", trabalhador.income(ano, mes)));
        sc.close();

    }
}
import java.util.ArrayList;
import java.util.Calendar;
import java.util.List;

public class Trabalhador {
  private String nome;
  private Cargo cargo;
  private Double salarioBase;

  private Departamento departamento;
  private List<ContratoHora> contratos = new ArrayList<>();

  public Trabalhador(){

  }

  public Trabalhador(String nome, Cargo cargo, Double salarioBase, Departamento departamento) {
      this.nome = nome;
      this.cargo = cargo;
      this.salarioBase = salarioBase;
      this.departamento = departamento;
  }


    public String getName() {
        return nome;
    }

    public void setName(String nome) {
        this.nome = nome;
    }

    public Cargo getCargo() {
        return cargo;
    }

    public void setCargo(Cargo cargo) {
        this.cargo = cargo;
    }

    public Double getSalarioBase() {
        return salarioBase;
    }

    public void setSalarioBase(Double salarioBase) {
        this.salarioBase = salarioBase;
    }

    public Departamento getDepartamento() {
        return departamento;
    }

    public void setDepartamento(Departamento departamento) {
        this.departamento = departamento;
    }

    public List<ContratoHora> getContratos() {
        return contratos;
    }

    public void  addContratos(ContratoHora contrato){
        contratos.add(contrato);
    }

    public void removeContrato( ContratoHora contrato){
        contratos.remove(contrato);
    }

    public double income(int ano, int mes){
      double soma = salarioBase;
      Calendar cal = Calendar.getInstance();
      for(ContratoHora c : contratos){
          cal.setTime(c.getData());
          int c_ano = cal.get(Calendar.YEAR);
          int c_mes = cal.get(Calendar.MONTH);
          if(c_ano == ano && c_mes == mes){
              soma += c.valorTotal();
          }
      }
      return soma;
    }
}

---------------------------------------------------------------------------------------------------------------------------------------
Código mostrando o uso da superclasse/subclasse, herança 

import java.util.Scanner;

public class Main {
    public static void main (String[] args){
        Scanner sc = new Scanner(System.in);

        Account acc = new Account(0052, "Maria", 2200.00 );
        BusinessAccount bacc = new BusinessAccount(0001, "Stella Iluminação", 500.00, 100.00);
        System.out.println("Dados da conta BACC");
        System.out.println("Número: " + bacc.getNumero() + " Holder: "
                + bacc.getHolder()
                + " Balence: " + bacc.getBalence()
                + " Loan limited: " + bacc.getLoanLimit());

        //UPCASTING
        // superclasse recebe subclasse
        Account acc1 = bacc;
        Account acc2 = new BusinessAccount(1003, "Matheus", 20.50, 500.000);

        //DONWCASTING

        BusinessAccount acc3 = (BusinessAccount) acc2;
        acc3.loan(100.00);


        System.out.println("Dados da conta ACC");
        System.out.println("Número: " + acc.getNumero() + " Holder: " + acc.getHolder() + " j'777Balence: " + acc.getBalence());
        acc.withDraw(20.00);
        System.out.println("-------------------------------------------");
        System.out.println("UPTADE! Saque de 20 realizado. Amount: " + acc.getBalence());


        sc.close();


    }
}

public class Account {
  private Integer numero;
  private String holder;
  protected Double balence;

  public Account(){
  }

  public Account(Integer numero, String holder, Double balence) {
        this.numero = numero;
        this.holder = holder;
        this.balence = balence;
  }

  public Integer getNumero() {
        return numero;
  }

   public void setNumero(Integer numero) {
        this.numero = numero;
  }

  public String getHolder() {
        return holder;
  }

  public void setHolder(String holder) {
        this.holder = holder;
  }

  public Double getBalence() {
        return balence;
  }

  public void deposit(Double amount){
        balence = balence+amount;
  }

    public void withDraw( Double amount){
        balence = balence - amount;
    }


}


public class BusinessAccount extends Account{

    private Double loanLimit;

    public BusinessAccount(){
        super();
    }

    public BusinessAccount(Double loanLimit) {
        this.loanLimit = loanLimit;
    }

    public BusinessAccount(Integer numero, String holder, Double balence, Double loanLimit) {
        super(numero, holder, balence);
        this.loanLimit = loanLimit;
    }

    public Double getLoanLimit() {
        return loanLimit;
    }

    public void setLoanLimit(Double loanLimit) {
        this.loanLimit = loanLimit;
    }

    public void loan(double amount) {

        if (amount <= loanLimit) {
            balence += amount - 10;
        }
    }
}


public class SavingAccount extends Account{

    private Double interestRate;

    public SavingAccount() {
        super();
    }

    public SavingAccount(Integer numero, String holder, Double balence, Double interestRate) {
        super(numero, holder, balence);
        this.interestRate = interestRate;
    }

    public Double getInterestRate() {
        return interestRate;
    }

    public void setInterestRate(Double interestRate) {
        this.interestRate = interestRate;
    }

    public void updateBalence(){

        balence = balence * interestRate;
    }
}

------------------------------------------------------------------------------------------------------------------------------

Fazer um programa que crie uma lista com a quantidade de funcionarios, aloque em uma lista. Em seguida entre com os dados e mostre o resultado dependendo se o funcionario for 3° ou não. Uso de @override e herança e polimorfismo. 


import java.util.List;
import java.util.Scanner;
import java.util.List;
import java.util.ArrayList;

public class Main {
    public static void main (String[] args){
        Scanner sc = new Scanner(System.in);

        System.out.print("Quantos funcionarios?");
        int n = sc.nextInt();

        List<Employee> list = new ArrayList<>();
    for(int i = 0; i<n;i++){
        System.out.println("O funcionario é terceirizado? (y/n) ");
        char resposta = sc.next().charAt(0);

        sc.nextLine();

        System.out.print("Nome: ");
        String nome = sc.nextLine();

        System.out.print("Hora: ");
        int hora = sc.nextInt();

        System.out.print("Valor por hora: ");
        double valorPorHora = sc.nextDouble();

        if(resposta == 'y'){
            System.out.print("digite: ");
            double additionalCharge = sc.nextDouble();
            OutSourceEmployee terceirizado = new OutSourceEmployee(nome, hora, valorPorHora, additionalCharge);
            list.add(terceirizado);
        }

        else{
            Employee employee = new Employee(nome, hora, valorPorHora);
            list.add(employee);
        }

    }

    System.out.println("Pagamento: ");
    for(Employee employee : list){
        System.out.print(employee.getNome() + " - R$" + employee.payment() + "\n");
    }

        sc.close();


    }
}


public class Employee {

  private String nome;
  private Integer hora;
  private Double valorPorHora;

  public Employee(){
  }

  public Employee(String nome, Integer hora, Double valorPorHora) {
      this.nome = nome;
      this.hora = hora;
      this.valorPorHora = valorPorHora;
  }

  public String getNome() {
      return nome;
  }

  public void setNome(String nome) {
      this.nome = nome;
  }

  public Integer getHora() {
      return hora;
  }

  public void setHora(Integer hora) {
      this.hora = hora;
  }

  public Double getValorPorHora() {
      return valorPorHora;
  }

  public void setValorPorHora(Double valorPorHora) {
      this.valorPorHora = valorPorHora;
  }

  public double payment(){
      return  valorPorHora*hora;
  }
}



public class Employee {

  private String nome;
  private Integer hora;
  private Double valorPorHora;

  public Employee(){
  }

  public Employee(String nome, Integer hora, Double valorPorHora) {
      this.nome = nome;
      this.hora = hora;
      this.valorPorHora = valorPorHora;
  }

  public String getNome() {
      return nome;
  }

  public void setNome(String nome) {
      this.nome = nome;
  }

  public Integer getHora() {
      return hora;
  }

  public void setHora(Integer hora) {
      this.hora = hora;
  }

  public Double getValorPorHora() {
      return valorPorHora;
  }

  public void setValorPorHora(Double valorPorHora) {
      this.valorPorHora = valorPorHora;
  }

  public double payment(){
      return  valorPorHora*hora;
  }
}



public class Employee {

  private String nome;
  private Integer hora;
  private Double valorPorHora;

  public Employee(){
  }

  public Employee(String nome, Integer hora, Double valorPorHora) {
      this.nome = nome;
      this.hora = hora;
      this.valorPorHora = valorPorHora;
  }

  public String getNome() {
      return nome;
  }

  public void setNome(String nome) {
      this.nome = nome;
  }

  public Integer getHora() {
      return hora;
  }

  public void setHora(Integer hora) {
      this.hora = hora;
  }

  public Double getValorPorHora() {
      return valorPorHora;
  }

  public void setValorPorHora(Double valorPorHora) {
      this.valorPorHora = valorPorHora;
  }

  public double payment(){
      return  valorPorHora*hora;
  }
}

public class OutSourceEmployee extends Employee{

    private Double additionalCharge;

    public OutSourceEmployee(){
        super();
    }
    public OutSourceEmployee(String nome, Integer hora, Double valorPorHora, Double additionalCharge) {
        super(nome, hora, valorPorHora);
        this.additionalCharge = additionalCharge;
    }

    public Double getAdditionalCharge() {
        return additionalCharge;
    }

    public void setAdditionalCharge(Double additionalCharge) {
        this.additionalCharge = additionalCharge;
    }

    @Override
    public double payment(){
        return  super.payment() + additionalCharge*1.1;
    }

}

----------------------------------------------------------------------------------------------------------------------
Programa com polimorfismo e sobrecarga 

import java.time.LocalDate;
import java.time.format.DateTimeFormatter;
import java.util.List;
import java.util.Scanner;
import java.util.List;
import java.util.ArrayList;

public class Main {
    public static void main (String[] args){
        Scanner sc = new Scanner(System.in);

        System.out.print("Quantos produtos?");
        int n = sc.nextInt();

        List<Product> list = new ArrayList<>();
    for(int i = 0; i<n;i++){
        System.out.println("Entre com os dados do produto " + (i+1) + " :");
        System.out.println("O produto é comum, usado ou importado? ");
        char resposta = sc.next().charAt(0);

        sc.nextLine();

        System.out.print("Nome: ");
        String nome = sc.nextLine();

        System.out.print("Preço: ");
        double preco = sc.nextDouble();

        if(resposta == 'c') {
            Product product = new Product(nome, preco);
            list.add(product);
        }

        else if(resposta == 'i'){
            System.out.print("Custom fee: ");
            double customFee = sc.nextDouble();
            ImportedProduct importedProduct = new ImportedProduct(nome, preco, customFee);
            list.add(importedProduct);

        }

        else{
            System.out.print("Entre com a data de fabricação: ");
            LocalDate manufactureDate = LocalDate.parse(sc.next(), DateTimeFormatter.ofPattern("dd/MM/yyyy"));
            UsedProduct usedProduct = new UsedProduct(nome, preco, manufactureDate);
            list.add(usedProduct);
        }

    }

    System.out.println("PRICE TAGS: ");
    for(Product x : list){
        System.out.print(x.priceTag() + "\n");
    }

        sc.close();


    }
}


public class Product {

  private String nome;
  private Double preco;

  public Product(){
  }

  public Product(String nome, Double preco) {
    this.nome = nome;
    this.preco = preco;
  }

  public String getNome() {
    return nome;
  }

  public void setNome(String nome) {
    this.nome = nome;
  }

  public Double getPreco() {
    return preco;
  }

  public void setPreco(Double preco) {
    this.preco = preco;
  }

  public String priceTag(){
      return "produto: " + nome + " Preço: " + preco;
  }
}



import java.time.LocalDate;
import java.time.format.DateTimeFormatter;
import java.util.Date;

public class UsedProduct extends Product{

    private LocalDate manufactureDate;

    public UsedProduct() {
    }

    public UsedProduct(String nome, Double preco, LocalDate manufactureDate) {
        super(nome, preco);
        this.manufactureDate = manufactureDate;
    }

    public LocalDate getManufactureDate() {
        return manufactureDate;
    }

    public void setManufactureDate(LocalDate manufactureDate) {
        this.manufactureDate = manufactureDate;
    }

    @Override
    public String priceTag() {
        return super.priceTag() + " (Data de fabricação: " + manufactureDate.format(DateTimeFormatter.ofPattern("dd/MM/yyyy")) + ")";
    }

}

public class ImportedProduct extends Product {

    private Double customFee;

    public ImportedProduct() {
    }

    public ImportedProduct(String nome, Double preco, Double customFee) {
        super(nome, preco);
        this.customFee = customFee;
    }

    public Double getCustomFee() {
        return customFee;
    }

    public void setCustomFee(Double customFee) {
        this.customFee = customFee;
    }

    @Override
    public String priceTag() {
        return super.priceTag() + " " + customFee;
    }
}

---------------------------------------------------------------------------------------------------------------------------------------usando polimorfismo e enum
import java.util.List;
import java.util.Scanner;
import java.util.ArrayList;

public class Main {
    public static void main (String[] args){
        Scanner sc = new Scanner(System.in);

        System.out.print("Quantos formas? ");
        int n = sc.nextInt();

        List<Shape> list = new ArrayList<>();

    for(int i = 0; i<n;i++) {
        System.out.println("Entre com os dados do produto " + (i + 1) + ":");
        System.out.print("Ratangulo ou circulo (r/c)? ");
        char resposta = sc.next().charAt(0);

        System.out.print("Preto, azul ou vermelho? ");
        Color color = Color.valueOf(sc.next().toUpperCase());

        if (resposta == 'r') {
            System.out.print("Entre com a comprimento: ");
            double width = sc.nextDouble();

            System.out.print("Entre com a altura: ");
            double height = sc.nextDouble();

            MyRectangle rectangle = new MyRectangle(color, width, height);
            list.add(rectangle);
        } else {
            System.out.print("Digite o raio: ");
            double raio = sc.nextDouble();
            Circle circle = new Circle(color, raio);
            list.add(circle);

        }
    }

    System.out.println("Infomações das formas: ");
    for(Shape shape : list){
        System.out.print("Cor: " + shape.getColor() + ", Area " + String.format("%.2f", shape.area()));
    }

    sc.close();


    }
}
public abstract class Shape {

  private Color color;

  public Shape(){
  }

  public Shape(Color color) {
    this.color = color;
  }

  public Color getColor() {
    return color;
  }

  public void setColor(Color color) {
    this.color = color;
  }

  public abstract double area();
}



public class MyRectangle extends Shape {

    private double width;
    private double height;

    public MyRectangle(Color color, double width, double height) {
        super(color);
        this.width = width;
        this.height = height;
    }

    @Override
    public double area() {
        return width*height;
    }
}
public class Circle extends Shape{

    private double radious;

    public Circle() {
        super();
    }

    public Circle(double radious) {
        this.radious = radious;
    }

    public Circle(Color color, double radious) {
        super(color);
        this.radious = radious;
    }

    public double getRadious() {
        return radious;
    }

    public void setRadious(double radious) {
        this.radious = radious;
    }

    @Override
    public double area() {
        return Math.PI*radious*radious;
    }
}

public enum Color {
    PRETO,
    AZUL,
    VERMELHO
}
-------------------------------------------------------------------------------------------------------------------------------------


recursividade - codigo basico 

public class MetodoRecursivo {
    public static double metodo(double a, double b) {
        if (b <= 1) {
            return a;
        } else {
            return metodo(b, a / b);
        }
    }

    public static void main(String[] args) {
        System.out.println("metodo(5, 3) = " + metodo(5, 3));
        System.out.println("metodo(15, 3) = " + metodo(15, 3));
        System.out.println("metodo(28, -45) = " + metodo(28, -45));
    }
}








