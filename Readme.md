import java.util.Scanner;

//Criar um Programa que preencha um vetor de 10 de números inteiros e imprima os números pares e ímpares!
//Para isso:
// a) Criar uma sub-rotina que recebe, como parâmetro, o vetor de inteiros, e preencher cada posição utilizando entrada padrão (Scanner);
// b) Deverá implementar uma sub-rotina (método) que receba um vetor como parâmetro, verifique se cada um dos valores é ímpar e imprima este valor;
// c) Deverá implementar uma sub-rotina (método) que possua a mesma regra anterior, porém, para valores pares;
// d) No método principal (main) deverá ser criado um vetor de 10 posições, e utilizar as sub-rotinas criadas para efetuar o preenchimento 
// e imprimir os valores pares e ímpares.

public class exercicios04 {

	public static void main(String[] args) {
		
		int numeros[] = new int[10];
		
		preencherVetor(numeros);
		
		System.out.println();
		
		printImpar(numeros);
		
		System.out.println();
		
		printPar(numeros);
		
	}
	
	public static void preencherVetor(int v[]) {
		Scanner leitor = new Scanner(System.in);
		
		for (int i = 0; i < v.length; i ++) {
			System.out.printf("v[%d] = ", i);
			v[i] = leitor.nextInt();
			
		}
		
		leitor.close();
				
	}
	
	public static void printImpar(int v[]) {
		for (int i = 0; i < v.length; i ++) {
			if (v[i] % 2 != 0) {
				System.out.print
				(v[i]);
			}
		}
	}
	
	public static void printPar(int v[]) {
		for (int i = 0; i < v.length; i ++) {
			if (v[i] % 2 == 0)  {
				System.out.print( v[i]);
			}	
		}
	}
}
