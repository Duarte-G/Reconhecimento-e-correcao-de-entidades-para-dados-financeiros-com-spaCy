# Reconhecimento-e-correcao-de-entidades-para-dados-financeiros-com-spaCy
Este repositório demonstra o uso da biblioteca spaCy para a identificação e correção de entidades em textos financeiros. O código carrega dados de símbolos de ações, índices e bolsas de valores e utiliza o EntityRuler do spaCy para definir padrões e melhorar a precisão do reconhecimento de entidades.

O script inclui a criação de padrões específicos para índices financeiros, símbolos de índices e bolsas de valores. Além disso, ajusta a classificação de entidades para evitar erros comuns, como classificar "Nasdaq" como uma empresa. A correção e aplicação desses padrões são exemplificadas com um texto de notícias financeiras, onde o código identifica corretamente entidades como "S&P 500", "Dow Jones" e "Nasdaq". Este projeto é uma aplicação prática que exemplifica como o spaCy pode ser útil para processar e analisar grandes volumes de texto financeiro com precisão.

<p align="center">
  <img src="https://github.com/user-attachments/assets/259a1b95-1c97-4ed1-9f07-d452415a7da9">
</p>

- **Correção do índice "S&P 500" para "S&P":** Para padronizar a entidade, foi transformado todas as ocorrências de "S&P 500 INDEX" em "S&P INDEX", removendo o número "500" para simplificar o reconhecimento do índice.
- **Correção de "Nasdaq":** O modelo inicialmente classificava "Nasdaq" como uma entidade do tipo COMPANY. Como "Nasdaq" refere-se a uma bolsa de valores, foi implementado uma lógica para garantir que ela fosse corretamente classificada como STOCK_EXCHANGE.
- **Simplificação de "Dow Jones Industrial Average" para "Dow Jones":** Foi reduzido o nome completo do índice "Dow Jones Industrial Average" para "Dow Jones", mantendo sua classificação correta como INDEX.

## Como Usar
 - Clone o repositório para sua máquina local.
 - Instale as bibliotecas necessárias no código.
 - Execute o .ipynb para explorar o código e resultados.
 - Sinta-se à vontade para modificar a base de dados e ajustar o código para analisar diferentes conjuntos de dados e aplicar o reconhecimento de entidades em outros contextos.
