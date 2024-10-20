# Desafio---Modelagem_e_Transforma-o_de_dados
# Power BI: Análise de Vendas e Descontos

Este projeto no Power BI realiza a análise de vendas, descontos e produtos com base em diferentes fontes de dados, organizados em um modelo relacional.

## Modelo de Dados

As tabelas usadas no projeto:

- **F_Vendas**: Fatos de vendas (quantidade, lucro, país, etc.).
- **D_Produtos**: Detalhes de produtos (nome, preço, ID).
- **D_Descontos**: Faixas de descontos aplicados.
- **D_Calendário**: Gerada automaticamente para análise temporal.
- **D_Produtos_Detalhes** e **D_Detalhes**: Informações adicionais sobre produtos.
- **financials**: Dados financeiros como vendas e COGS.


## Principais Cálculos DAX

- **Tabela de Calendário**:
  ```DAX
  D_Calendário = CALENDARAUTO(12)
  Ano = YEAR('D_Calendário'[Data])
  Dia da semana = WEEKDAY('D_Calendário'[Data])
  Dia da semana texto = FORMAT('D_Calendário'[Data], "DDDD")
  Mês número = MONTH('D_Calendário'[Data])
  Semana número = WEEKNUM('D_Calendário'[Data])

### Diagrama do Modelo de Dados

![Diagrama UML](https://github.com/rhuanvictor/Desafio---Modelagem_e_Transforma-o_de_dados/blob/main/UML.jpg)


