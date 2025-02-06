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
