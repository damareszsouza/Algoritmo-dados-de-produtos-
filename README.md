# Algoritmo-dados-de-produtos-

Considere o seguinte problema:

Faça um algoritmo que leia o nome, o custo e o preço de 20 produtos. Ao final deverá relacionar os produtos que:

Tem lucro menor que 10%;
Tem lucro entre 10% e 30%;
Tem lucro maior que 30%.
Complete o programa abaixo, arrastando e soltando os trechos de código nos espaços em branco, de forma que o problema acima seja corretamente implementado.

public class VerificaLucros {
	public static void main(String[] args) {
		String[] nomes = new String[20];
		double[] custos = new double[20];
		double[] precos = new double[20];
		
		// Leitura
		for(int cont = 0; cont < [nomes.length]; cont++) {
			System.out.printf("-------------------------- PRODUTO %02d --------------------------\n", cont+1);
			System.out.print("Nome: ");
			nomes[cont] = System.console().readLine();
			System.out.print("Custo: ");
			custos[cont] = Double.parseDouble(System.console().readLine());
			System.out.print("Preco: ");
			[precos[cont] = Double.parseDouble(System.console().readLine());]
		}
		
		// Processamento e Saída (produtos com lucro menor do que 10%)
		System.out.println("Produtos com menos de 10% de lucro:");
		for(int cont = 0; cont < nomes.length; cont++) {
			double lucro = precos[cont] - custos[cont];
			[if(lucro < precos[cont] * 0.10)]
				System.out.println(nomes[cont]);
		}
		
		// Processamento e Saída (produtos com lucro entre 10% e 30%)
		System.out.println("Produtos com lucro entre 10% e 30%:");
		for(int cont = 0; cont < nomes.length; cont++) {
			double lucro = precos[cont] - custos[cont];
			[if(lucro <= precos[cont] * 0.30 && lucro >= precos[cont] * 0.10)]
				System.out.println(nomes[cont]);
		}
		
		// Processamento e Saída (produtos com lucro maior do que 30%)
		System.out.println("Produtos com lucro maior que 30%:");
		for(int cont = 0; cont < nomes.length; cont++) {
			double lucro = precos[cont] - custos[cont];
			[if(lucro > precos[cont] * 0.30)]
				System.out.println(nomes[cont]);
		}
	}
}
