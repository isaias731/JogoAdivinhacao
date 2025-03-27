import java.util.Random;
import java.util.Scanner;

public class JogoAdivinhacao {

    public static void main(String[] args) {
        Random random = new Random();
        int numeroAleatorio = random.nextInt(100) + 1; // Gera um número aleatório entre 1 e 100
        Scanner scanner = new Scanner(System.in);
        int tentativa;
        int tentativas = 0;

        System.out.println("Bem-vindo ao Jogo da Adivinhação!");
        System.out.println("Tente adivinhar o número que estou pensando (entre 1 e 100).");

        while (true) {
            System.out.print("Digite sua tentativa: ");
            tentativa = scanner.nextInt();
            tentativas++;

            if (tentativa == numeroAleatorio) {
                System.out.println("Parabéns! Você acertou o número em " + tentativas + " tentativas.");
                break; // Sai do loop quando o jogador acerta
            } else if (tentativa < numeroAleatorio) {
                System.out.println("O número é maior. Tente novamente.");
            } else {
                System.out.println("O número é menor. Tente novamente.");
            }
        }
        scanner.close();
    }
}
