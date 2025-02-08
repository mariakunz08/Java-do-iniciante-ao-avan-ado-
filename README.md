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
