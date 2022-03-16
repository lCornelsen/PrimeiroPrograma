# PrimeiroPrograma 

package Lucas.Autonomo.financeiro.Chapa;

import java.util.Scanner;

public class JarvisFiis extends FundoImobiliarioDominio {
    public JarvisFiis(String nomeDoAtivo, Double valorDoAtivo, Double valorDividendoUltimoMes, Double valorDividendoUltimos12Meses) {
        super(nomeDoAtivo, valorDoAtivo, valorDividendoUltimoMes, valorDividendoUltimos12Meses);
    }

    public static void main(String[] args) {

        JarvisFiis ativo1 = new JarvisFiis("TORD11", 9.28, 0.08, 1.11);
        JarvisFiis ativo2 = new JarvisFiis("MXFR11", 9.12, 0.09, 0.97);
        JarvisFiis ativo3 = new JarvisFiis("ALZR11", 110.12, 0.72, 7.94);
        JarvisFiis ativo4 = new JarvisFiis("KNRI11", 131.97, 0.81, 8.99);
        JarvisFiis ativo5 = new JarvisFiis("XPSF11", 69.83, 0.66, 8.66);
        JarvisFiis ativo6 = new JarvisFiis("XPLG11", 97.25, 0.66, 7.49);
        JarvisFiis ativo7 = new JarvisFiis("HGLG11", 164.12, 1.10, 14.21);
        JarvisFiis ativo8 = new JarvisFiis("MALL11", 99.39, 0.72, 6.76);

        Scanner scan = new Scanner(System.in);
        double totalGasto;
        double totalDeCotas;
        double somaDosYieldsDozeMeses = ativo1.valorDividendoUltimos12Meses + ativo2.valorDividendoUltimos12Meses + ativo3.valorDividendoUltimos12Meses + ativo4.valorDividendoUltimos12Meses + ativo5.valorDividendoUltimos12Meses;
        double media = somaDosYieldsDozeMeses / 5;
        double somaDeTodosOsDozeMeses = somaDosYieldsDozeMeses + ativo6.valorDividendoUltimos12Meses + ativo7.valorDividendoUltimos12Meses + ativo8.valorDividendoUltimos12Meses;
        double mediaOitoFundos = somaDeTodosOsDozeMeses / 8;

        System.out.println("------------------------------------------------------------");
        System.out.println("Eu sou Jarvis Bem Vindo!\nEsse é um simulador de fii's.");
        System.out.println("Digite [1] para realizar a simulação apenas com o ativo TORD11.");
        System.out.println("Digite [2] para realizar a simulação apenas com o ativo MXFR11.");
        System.out.println("Digite [3] para realizar a simulação apenas com o ativo ALRZ11.");
        System.out.println("Digite [4] para realizar a simulação apenas com o ativo KNRI11.");
        System.out.println("Digite [5] para realizar a simulação apenas com o ativo XPSF11.");
        System.out.println("Digite [6] para realizar a simulação apenas com o ativo XPLG11.");
        System.out.println("Digite [7] para realizar a simulação apenas com o ativo HGLG11.");
        System.out.println("Digite [8] para realizar a simulação apenas com o ativo MALL11.");
        System.out.println("Digite [9] para realizar a simulação com os ativos TORD11, MXFR11, ALRZ11, KNRI11, XPSF11");
        System.out.println("Digite [10] para realizar a simulação com os ativos TORD11, MXFR11, ALRZ11, KNRI11, XPSF11, XPLG11, HGLG11, MALL11");
        System.out.println("------------------------------------------------------------");
        System.out.print("Digite o valor numerico: ");

        int respostaDaPrimeiraOpcao = scan.nextInt();

        switch (respostaDaPrimeiraOpcao) {
            case 1:
                System.out.println("Seu ativo é " + ativo1.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo1.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada / ativo1.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo1.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 2:
                System.out.println("Seu ativo é " + ativo2.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo2.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada2 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada2 / ativo2.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo2.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada2);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 3:
                System.out.println("Seu ativo é " + ativo3.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo3.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada3 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada3 / ativo3.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo3.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada3);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 4:
                System.out.println("Seu ativo é " + ativo4.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo4.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada4 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada4 / ativo4.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo4.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada4);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 5:
                System.out.println("Seu ativo é " + ativo5.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo5.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada5 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada5 / ativo5.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo5.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada5);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 6:
                System.out.println("Seu ativo é " + ativo6.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo6.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada6 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada6 / ativo6.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo6.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada6);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 7:
                System.out.println("Seu ativo é " + ativo7.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo7.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada7 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada7 / ativo7.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo7.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada7);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 8:
                System.out.println("Seu ativo é " + ativo8.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo8.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada8 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada8 / ativo8.valorDividendoUltimos12Meses;
                totalGasto = totalDeCotas * ativo8.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada8);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 9:
                System.out.println("Sua carteira de ativos é               " + ativo1.getNomeDoAtivo() + " / " + ativo2.getNomeDoAtivo() + " / " + ativo3.getNomeDoAtivo() + " / " + ativo4.getNomeDoAtivo() + " / " + ativo5.getNomeDoAtivo() +
                        "\nO valor de uma cota está custando      " + ativo1.getValorDoAtivo() + "$ / " + ativo2.getValorDoAtivo() + "$ / " + ativo3.getValorDoAtivo() + "$ / " + ativo4.getValorDoAtivo() + "$ / " + ativo5.getValorDoAtivo() + "$");
                System.out.print("\nDigite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada9 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada9 / media;
                totalGasto = (totalDeCotas / 5) * ativo1.valorDoAtivo + (totalDeCotas / 5) * ativo2.valorDoAtivo + (totalDeCotas / 5) * ativo3.valorDoAtivo + (totalDeCotas / 5) * ativo4.valorDoAtivo + (totalDeCotas / 5) * ativo5.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada9);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            case 10:
                System.out.println("Sua carteira de ativos é              " + ativo1.getNomeDoAtivo() + " / " + ativo2.getNomeDoAtivo() + " / " + ativo3.getNomeDoAtivo() + " / " + ativo4.getNomeDoAtivo() + " / " + ativo5.getNomeDoAtivo() + " / " + ativo6.getNomeDoAtivo() + " / " + ativo7.getNomeDoAtivo() + " / " + ativo8.getNomeDoAtivo() +
                        "\nO valor de uma cota está custando     " + ativo1.getValorDoAtivo() + "$ / " + ativo2.getValorDoAtivo() + "$ / " + ativo3.getValorDoAtivo() + "$ / " + ativo4.getValorDoAtivo() + "$ / " + ativo5.getValorDoAtivo() + "$ / " + ativo6.getValorDoAtivo() + "$ / " + ativo7.getValorDoAtivo() + "$ / " + ativo8.getValorDoAtivo() + "$");
                System.out.print("\nDigite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                double rendaMensalDesejada10 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada10 / mediaOitoFundos;
                totalGasto = (totalDeCotas / 8) * ativo1.valorDoAtivo + (totalDeCotas / 8) * ativo2.valorDoAtivo + (totalDeCotas / 8) * ativo3.valorDoAtivo + (totalDeCotas / 8) * ativo4.valorDoAtivo + (totalDeCotas / 8) * ativo5.valorDoAtivo + (totalDeCotas / 8) * ativo6.valorDoAtivo + (totalDeCotas / 8) * ativo7.valorDoAtivo + (totalDeCotas / 8) * ativo8.valorDoAtivo;
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada10);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
            default:
                System.out.println("--------------------------------------------------------");
                System.out.println("---------------APAGANDO TODOS OS DADOS------------------");
                System.out.println("--------------------------------------------------------");
                break;
        }
    }
}
