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
        JarvisFiis ativo9 = new JarvisFiis("VGIP11", 99.79, 1.20, 14.11);
        JarvisFiis ativo10 = new JarvisFiis("RECR11", 101.58, 1.20, 13.75);
        JarvisFiis ativo11 = new JarvisFiis("VILG11", 99.15, 0.70, 7.63);

        Scanner scan = new Scanner(System.in);
        double totalGasto;
        double totalDeCotas;
        
        double somaDosYieldsDozeMeses = ativo1.valorDividendoUltimos12Meses + ativo2.valorDividendoUltimos12Meses + ativo3.valorDividendoUltimos12Meses + ativo4.valorDividendoUltimos12Meses + ativo5.valorDividendoUltimos12Meses;
        
        double media = somaDosYieldsDozeMeses / 5;
        
        double somaDeTodosOsDozeMeses = somaDosYieldsDozeMeses + ativo6.valorDividendoUltimos12Meses + ativo7.valorDividendoUltimos12Meses + ativo8.valorDividendoUltimos12Meses;
        
        double mediaOitoFundos = somaDeTodosOsDozeMeses / 8;
        
        double carteiraTeste = (ativo2.valorDividendoUltimos12Meses + ativo9.valorDividendoUltimos12Meses + ativo10.valorDividendoUltimos12Meses) / 3;
        
        double carteiraTeste2 = (ativo2.valorDividendoUltimos12Meses + ativo7.valorDividendoUltimos12Meses + ativo10.valorDividendoUltimos12Meses) / 3;
        
        double carteiraTeste3 = (ativo2.valorDividendoUltimos12Meses + ativo11.valorDividendoUltimos12Meses + ativo10.valorDividendoUltimos12Meses) / 3;
        
        double carteiraMensal = carteiraTeste / 12;
        double carteiraMensa2 = carteiraTeste2 / 12;
        double carteiraMensa3 = carteiraTeste3 / 12;


        System.out.println("------------------------------------------------------------");
        System.out.println("Eu sou Jarvis Bem Vindo!\nEsse é um simulador de fii's.");
        System.out.println("Digite [1] para realizar a simulação apenas com o ativo TORD11.");
        System.out.println("Digite [2] para realizar a simulação apenas com o ativo MXFR11.");
        System.out.println("Digite [3] para realizar a simululação com os ativos MXRF11, RECR11, VGIP11.");
        System.out.println("Digite [4] para realizar a simululação com os ativos MXRF11, RECR11, HGLG11.");
        System.out.println("Digite [5] para realizar a simululação com os ativos MXRF11, RECR11, VILG11.");
        System.out.println("Digite [6] para realizar a simulação com os ativos TORD11, MXFR11, ALRZ11, KNRI11, XPSF11");
        System.out.println("Digite [7] para realizar a simulação com os ativos TORD11, MXFR11, ALRZ11, KNRI11, XPSF11, XPLG11, HGLG11, MALL11");
        System.out.println("------------------------------------------------------------");
        System.out.print("Digite o valor numerico: ");

        int respostaDaPrimeiraOpcao = scan.nextInt();

        switch (respostaDaPrimeiraOpcao) {
        
            case 1:
            
                System.out.println("Seu ativo é " + ativo1.getNomeDoAtivo() + "\nO valor de uma cota está custando R " + ativo1.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                
                double rendaMensalDesejada = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada / (ativo1.valorDividendoUltimos12Meses / 12);
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
                totalDeCotas = rendaMensalDesejada2 / (ativo2.valorDividendoUltimos12Meses / 12);
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
            
                System.out.println("Seu ativo é " + ativo2.getNomeDoAtivo() + "/" + ativo9.getNomeDoAtivo() + "/" + ativo10.getNomeDoAtivo()
                        + "\nO valor de uma cota está custando R " + ativo2.getValorDoAtivo() + "$ /" + ativo9.getValorDoAtivo() +
                        "$ / " + ativo10.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos dessa carteira: ");
                
                double rendaMensalDesejada3 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada3 / carteiraMensal;
                totalGasto = totalDeCotas * (ativo2.valorDoAtivo + ativo9.valorDoAtivo + ativo10.valorDoAtivo);
                
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejada:  %.2f", rendaMensalDesejada3);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
                
            case 4:
            
                System.out.println("Seu ativo é " + ativo2.getNomeDoAtivo() + "/" + ativo10.getNomeDoAtivo() + "/" + ativo7.getNomeDoAtivo()
                        + "\nO valor de uma cota está custando R " + ativo2.getValorDoAtivo() + "$ /" + ativo10.getValorDoAtivo() +
                        "$ / " + ativo7.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos dessa carteira: ");
                
                double rendaMensalDesejada4 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada4 / carteiraMensa2;
                totalGasto = totalDeCotas * (ativo2.valorDoAtivo + ativo10.valorDoAtivo + ativo7.valorDoAtivo);
                
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejada:  %.2f", rendaMensalDesejada4);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
                
            case 5:
            
                System.out.println("Seu ativo é " + ativo2.getNomeDoAtivo() + "/ " + ativo10.getNomeDoAtivo() + "/ " + ativo11.getNomeDoAtivo()
                        + "\nO valor de uma cota está custando R " + ativo2.getValorDoAtivo() + "$ /" + ativo10.getValorDoAtivo() +
                        "$ / " + ativo11.getValorDoAtivo() + "$");
                System.out.print("Digite o valor que gostaria de receber mensalmente dos dividendos dessa carteira: ");
                
                double rendaMensalDesejada5 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada5 / carteiraMensa3;
                totalGasto = totalDeCotas * (ativo2.valorDoAtivo + ativo11.valorDoAtivo + ativo10.valorDoAtivo);
                
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejada:  %.2f", rendaMensalDesejada5);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
                
            case 6:
            
                System.out.println("Sua carteira de ativos é               " + ativo1.getNomeDoAtivo() + " / " + ativo2.getNomeDoAtivo() " / " + ativo3.getNomeDoAtivo() + " / " + ativo4.getNomeDoAtivo() + " / " + ativo5.getNomeDoAtivo() + "\nO valor de uma cota está custando      " + ativo1.getValorDoAtivo() + "$ / " + ativo2.getValorDoAtivo() + "$ / " + ativo3.getValorDoAtivo() + "$ / " + ativo4.getValorDoAtivo() + "$ / " + ativo5.getValorDoAtivo() + "$");
                System.out.print("\nDigite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                
                double rendaMensalDesejada9 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada9 / (media / 12);
                totalGasto = (totalDeCotas / 5) * ativo1.valorDoAtivo + (totalDeCotas / 5) * ativo2.valorDoAtivo + (totalDeCotas / 5) * ativo3.valorDoAtivo + (totalDeCotas / 5) * ativo4.valorDoAtivo + (totalDeCotas / 5) * ativo5.valorDoAtivo;
                
                System.out.println("------------------------------------------------------------");
                System.out.printf("Renda mensal desejável:  %.2f", rendaMensalDesejada9);
                System.out.print("$");
                System.out.printf("\nNumero de cotas necessárias:  %.0f %n", totalDeCotas);
                System.out.printf("Investimento total:  %.2f", totalGasto);
                System.out.print("$");
                System.out.println("\n------------------------------------------------------------");
                break;
                
            case 7:
            
                System.out.println("Sua carteira de ativos é              " + ativo1.getNomeDoAtivo() + " / " + ativo2.getNomeDoAtivo() + " / " + ativo3.getNomeDoAtivo() + " / " + ativo4.getNomeDoAtivo() + " / " + ativo5.getNomeDoAtivo() + " / " + ativo6.getNomeDoAtivo() + " / " + ativo7.getNomeDoAtivo() + " / " + ativo8.getNomeDoAtivo() + "\nO valor de uma cota está custando     " + ativo1.getValorDoAtivo() + "$ / " + ativo2.getValorDoAtivo() + "$ / " + ativo3.getValorDoAtivo() + "$ / " + ativo4.getValorDoAtivo() + "$ / " + ativo5.getValorDoAtivo() + "$ / " + ativo6.getValorDoAtivo() + "$ / " + ativo7.getValorDoAtivo() + "$ / " + ativo8.getValorDoAtivo() + "$");
                System.out.print("\nDigite o valor que gostaria de receber mensalmente dos dividendos desse fundo: ");
                
                double rendaMensalDesejada10 = scan.nextDouble();
                totalDeCotas = rendaMensalDesejada10 / (mediaOitoFundos / 12);
                totalGasto = (totalDeCotas / 8) * ativo1.valorDoAtivo + (totalDeCotas / 8) * ativo2.valorDoAtivo +
(totalDeCotas / 8) * ativo3.valorDoAtivo + (totalDeCotas / 8) * ativo4.valorDoAtivo + (totalDeCotas / 8) *
ativo5.valorDoAtivo + (totalDeCotas / 8) * ativo6.valorDoAtivo + (totalDeCotas / 8) * ativo7.valorDoAtivo +
(totalDeCotas / 8) * ativo8.valorDoAtivo;

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
