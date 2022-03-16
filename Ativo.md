# PrimeiroPrograma

package Lucas.Autonomo.financeiro.Chapa;

public class FundoImobiliarioDominio {
    String nomeDoAtivo;
    Double valorDoAtivo;
    Double valorDividendoUltimoMes;
    Double valorDividendoUltimos12Meses;

    public FundoImobiliarioDominio(String nomeDoAtivo, Double valorDoAtivo, Double valorDividendoUltimoMes, Double valorDividendoUltimos12Meses) {
        this.nomeDoAtivo = nomeDoAtivo;
        this.valorDoAtivo = valorDoAtivo;
        this.valorDividendoUltimoMes = valorDividendoUltimoMes;
        this.valorDividendoUltimos12Meses = valorDividendoUltimos12Meses;
    }

    public String getNomeDoAtivo() {
        return nomeDoAtivo;
    }

    public void setNomeDoAtivo(String nomeDoAtivo) {
        this.nomeDoAtivo = nomeDoAtivo;
    }

    public Double getValorDoAtivo() {
        return valorDoAtivo;
    }

    public void setValorDoAtivo(Double valorDoAtivo) {
        this.valorDoAtivo = valorDoAtivo;
    }

    public Double getValorDividendoUltimoMes() {
        return valorDividendoUltimoMes;
    }

    public void setValorDividendoUltimoMes(Double valorDividendoUltimoMes) {
        this.valorDividendoUltimoMes = valorDividendoUltimoMes;
    }

    public Double getValorDividendoUltimos12Meses() {
        return valorDividendoUltimos12Meses;
    }

    public void setValorDividendoUltimos12Meses(Double valorDividendoUltimos12Meses) {
        this.valorDividendoUltimos12Meses = valorDividendoUltimos12Meses;
    }
}
