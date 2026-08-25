parâmetros de entrada do pdmax
#Example of usage with hypothetical files
result <- marketmodel(
   arquivo       = "data/demanda_Amazonas.xlsx",
   arquivopib    = "data/pib_Amazonas.xlsx",
   arquivoindice = "data/indice_atividade.csv",
   arquivomarketmodel = "data/mercado_Amazonas.csv",
   nivel_tensao = "138"
   lista_barras = c("CENTRO-AM138")
   ano_mes_inic  = c(2017,1),
   ano_mes_fim  = c(2026,3),
   horizonte     = 120,
   variavel_prevista = c("leve","media","pesada")
   tipo = 1
   grafico = TRUE,
)

# Access monthly forecasts 
result$previsoes

# Access annual forecasts
result$previsoes_anuais

# Access the busbar time series
result$series_barras

# Access the system's maximum demand time series.
result$series_sistema
 
# Access performance metrics.
result$metricas

#' }
#'
