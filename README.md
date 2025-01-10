# Comparação e Atualização de Dados de Franquias

Este projeto tem como objetivo comparar as informações em duas planilhas, uma com o dado atualizado e a outra com o dado desatualizado, e gerar uma planilha contendo os dados que estão presentes apenas na planilha desatualizada. Este processo é util para identificar dados desatualizados e auxiliar na manutenção e atualização das informações. 

# Como Funciona

O codigo realizada as seguintes etapas:

1. Upload das planilhas: Duas planilhas de formato xlsx são carregadas, sendo uma versão desatualizada e uma versão atualizada dos dados.

2. Mesclagem das planilhas: As duas planilhas são combinadas com base em uma coluna comum presente nas duas planilhas.

3. Filtragem de dados desatualizados: Apos a mesclagem, o codigo identifica quais franquias estão presentes apenas na planilha desatualizada.

4. Exportação do resultado: Uma nova planilha é gerada contendo as franquias desatualizadas, para facilitar o processo de atualização.


# Pré requisitos

Este projeto foi desenvolvido em Python, utilizando a biblioteca pandas para manipulação de dados e a funcionalidade de upload de arquivos do Google Colab.

Certifique-se de ter as seguintes bibliotecas instaladas:

pip install pandas

OBS: Se você for usar o Google Colab, não é necessário instalar as bibliotecas, pois elas já estão disponíveis.

# Estrutura do Código 

Bibliotecas:

1. Import files: Específico para ambientes do Google Colab e permite que você faça upload de arquivos para seu notebook.
2. Import io: Fornece ferramentas para trabalhar com fluxos de entrada e saída.io
3. Uploaded: Permite selecionar os arquivos do Excel com os quais deseja trabalhar.
4. Import Pandas as pd: Biblioteca para manipulação e análise de dados, principalmente com dados tabulares, como planilhas do Excel.

Funcionamento do codigo:

1. Carrega as bibliotecas necessarias para realizar as operações. O codigo usa biblioteca pandas para manipulação de dados e files para upload de arquivos no ambiente colab.

2. O codigo solicita o upload de dois arquivos excel, as planilhas atualizadas e não atualizadas.

3. É asuumido que a coluna "NomeUnidade" é a chave comum entre as duas planilhas, ou seja, essa coluna sera usada para comparar os dois arquivos.

4. É utilizado o metodo pd.merge para mesclar as duas planilhas com base na coluna comum.

5. A opção how="left" indica que a mesclagem será feita de forma que todos os dados da planilha desatualizada sejam mantidos e os dados da planilha atualizada serão adicionados onde houver correspondencia na coluna comum.

6. Já o indicator=True adiciona uma coluna extra chamada "_merge" que informa se uma linha esta presente em ambas as planilhas ou apenas em uma delas.

7. Após a mesclagem, o codigo filtra as linhas onde a coluna "_merge" tem o valor "left_only". Essas linhas representam entradas que estão apenas em uma planilha desatualizada.

8. A coluna "_merge" é removida, já que não mais necessaria apos a filtragem.

9. O codigo imprime as primeiras linhas do dataframe resultante, mostrando as entradas que não foram atualizadas.

# Como usar

Faça o upload das duas planilhas (desatualizada e atualizada) para o ambiente.
Execute o código.
O código irá gerar uma nova planilha Excel com as franquias desatualizadas, salva como dados_desatualizadas_com_status.xlsx.


ACESSE O CODIGO FONTE NAS PASTAS DESTE REPOSITORIO







