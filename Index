package sistema;

import java.util.Scanner;

public class Index {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);

		String opcao = "";
		boolean sair = false;
		String[] usuario = new String[4];
		String[][] casa = new String[4][3];
		Integer[] codigo = new Integer[usuario.length];
		
		for (int i = 0; i < casa.length; i++) {
			for (int j = 0; j < casa[i].length; j++) {
				if (j == 0) {
					casa[i][j] = ""+(1+i);
				}
			}
		}

		do {
			System.out.println(" ----------------------------------------------------------------");
			System.out.println("|\t\t\t Menu Principal\t\t\t\t |");
			System.out.println(" ----------------------------------------------------------------");
			System.out.println("|\t\t01 - Cadastrar\t\t\t\t\t |");
			System.out.println("|\t\t02 - Reservar casa\t\t\t\t |");
			System.out.println("|\t\t03 - Visualizar \t\t\t\t |");
			System.out.println("|\t\t05 - Sobre o sistema\t\t\t\t |");
			System.out.println("|\t\t06 - Sobre os desenvolvedores\t\t\t |");
			System.out.println("|\t\t10 - Sair\t\t\t\t\t |");
			System.out.println(" ----------------------------------------------------------------");
			System.out.print(" Informe a opção: ");
			opcao = input.next();
			switch (opcao) {
			case "1":
			case "01":
				String quantidadeUsuarioTemporaria;
				int quantidadeUsuario;
				int contador = 0;
				System.out.println("");
				System.out.println(" ---------------------------------------------------------------");
				System.out.println("| Quantidade máxima de usuário permitido\t|\t"+usuario.length+"\t|");
				System.out.println(" ---------------------------------------------------------------");
				if (true) {
					while (true) {
						System.out.print(" Informe a quantidade de usuário que deseja cadastra: ");
						quantidadeUsuarioTemporaria = input.next();
						for (int i = 0; i < quantidadeUsuarioTemporaria.length(); i++) {
							if (quantidadeUsuarioTemporaria.charAt(i) > 47
									&& quantidadeUsuarioTemporaria.charAt(i) < 58) {
								contador++;
							}
						}
						if (contador == quantidadeUsuarioTemporaria.length()) {
							quantidadeUsuario = Integer.parseInt(quantidadeUsuarioTemporaria);
							break;
						}
						contador = 0;
					}
					contador = 0;
					for (int i = 0; i < usuario.length; i++) {
						if (contador == quantidadeUsuario) {
							break;
						}
						if (usuario[i] == null) {
							input = new Scanner(System.in);
							System.out.print(" Informe o nome do usuário "+(i+1)+": ");
							usuario[i] = input.nextLine();
							codigo[i] = i;
							contador++;
						}					
					}
				}
				System.out.println("");
				break;
			case "2":
			case "02":
				int contadorCadastro = 0;
				String quantidadeUsuarioTemporariaCadastro,nomeBuscarCadasto;
				int quantidadeUsuarioCadastro;
				System.out.println("");
				System.out.println(" -----------------------------------------------------------------------");
				System.out.println("| Quantidade máxima de casa disponível no sistema\t |\t"+casa.length+"\t|");
				System.out.println(" -----------------------------------------------------------------------");
				if (true) {
					while (true) {						
						System.out.print(" Informe o número de qual casa deseja alugar: ");
						quantidadeUsuarioTemporariaCadastro = input.next();
						for (int i = 0; i < quantidadeUsuarioTemporariaCadastro.length(); i++) {
							if (quantidadeUsuarioTemporariaCadastro.charAt(i) > 47
									&& quantidadeUsuarioTemporariaCadastro.charAt(i) < 58) {
								contadorCadastro++;
							}
						}
						if (contadorCadastro == quantidadeUsuarioTemporariaCadastro.length()) {
							quantidadeUsuarioCadastro = Integer.parseInt(quantidadeUsuarioTemporariaCadastro);
							break;
						}
					}
				}
				
				contadorCadastro = -1;
				
				if (quantidadeUsuarioCadastro > casa.length) {
					System.out.println(" Não existem nenhuma casa com este número");	
					System.out.println("");
					break;
				}
				
				if (quantidadeUsuarioCadastro <= 0) {
					System.out.println(" Por favor, informe um número maior que 0");
					System.out.println("");
					break;
				}
				
				System.out.print(" Informe o nome do usuário: ");
				input = new Scanner(System.in);
				nomeBuscarCadasto = input.nextLine();
				for (int i = 0; i < usuario.length; i++) {
					if (nomeBuscarCadasto.equalsIgnoreCase(usuario[i])) {
						contadorCadastro++;
						break;
					}
				}

				quantidadeUsuarioCadastro = quantidadeUsuarioCadastro - 1;
				
				if (contadorCadastro < 0) {
					System.out.println(" Erro, Usuário "+nomeBuscarCadasto+" não foi localizado");
					System.out.println("");
					break;
				}
				
				for (int i = 0; i < usuario.length; i++) {
					if (nomeBuscarCadasto.equalsIgnoreCase(usuario[i])) {
						contadorCadastro = i;
						break;
					}
				}
								
				casa[quantidadeUsuarioCadastro][1] = ""+codigo[contadorCadastro];
				casa[quantidadeUsuarioCadastro][2] = usuario[contadorCadastro];
				System.out.println("");
				break;
			case "3":
			case "03":		
				System.out.println("");
				System.out.println(" ----------------------------------------------------------------");
				System.out.println("|\t\t01 - Mostrar todo os usuários\t\t\t |");
				System.out.println("|\t\t02 - Mostrar toda as vaga\t\t\t |");
				System.out.println(" ----------------------------------------------------------------");
				System.out.print(" Escolha uma opção: ");
				switch (input.next()) {
				case "1":
				case "01":
					boolean controleUsuarioTemp = false;
					System.out.println("");
					System.out.println(" Lista de usuário ");
					System.out.println(" ----------------------- -------------------------------");
					System.out.println("|\tCódigo\t\t|\t\tUsuário\t\t|");
					System.out.println(" ----------------------- -------------------------------");
					for (int i = 0; i < usuario.length; i++) {
						if (usuario[i] != null) {
							System.out.println("\t"+i+"\t\t\t"+usuario[i]+"\t");
							controleUsuarioTemp = true;
						}
					}
					if (controleUsuarioTemp == false) {
						System.out.println(" Não existe usuário cadastrado no sistema");
					}
					System.out.println("");
					break;
				case "2":
				case "02":
					System.out.println("");
					System.out.println(" Mostrar toda as vaga");
					System.out.print(" Número casa\tNúmero usuário\t\tNome usuário");
					System.out.println("");
					for (int i = 0; i < casa.length; i++) {
						for (int j = 0; j < casa[i].length; j++) {
							if (j == 0)
							{
								System.out.print("\t"+casa[i][j]);
							}
							if (j == 1)
							{
								System.out.print("\t\t"+casa[i][j]);
							}
							if (j == 2)
							{
								System.out.print("\t\t\t"+casa[i][j]);
							}
							
						}
						System.out.println("");
					}
					System.out.println("");
					break;
				default:
					System.out.println(" Opção inválida");
					break;
				}
				break;
			case "5":
			case "05":
				System.out.println("");
				System.out.println("\t\t SOBRE O SISTEMA");
				System.out.println("\t Neste sistema você será capaz cadastrar usuários e logo \n "
				    + "\t após o cadastro será possível a reserva de uma casas no\n"
						+ "\t condomínio.");
						
				System.out.println("");
				System.out.println("");
				input.nextLine();
				System.out.println("Aperte \"ENTER\" para voltar ao menu principal ...");
				input.nextLine();
				break;
			case "06":
			case "6":
				System.out.println();
				System.out.println();
				System.out.println("\t\t SOBRE OS DESENVOLVEDORES");
				System.out.println("Anderson Nascimento Correa\t-\tCiência da Computação");
				System.out.println("Pedro Henrique Fernandes\t-\tSistemas de Informação");
				System.out.println("Robert d. S. R. Conceição\t-\tAnálise e Desenvolvimento de Sistemas");
				System.out.println();
				System.out.println();
				System.out.println("Aperte \"ENTER\" para voltar ao menu principal ...");
				input = new Scanner(System.in);
				input.nextLine();
				break;
			case "10":
				sair = true;
				break;
			default:
				System.out.println();
				System.out.println(" Opção inválida, escolha uma do menu abaixo");
				System.out.println();
				break;
			}

			if (sair == true) {
				break;
			}
		} while (true);

		input.close();
	}
}
