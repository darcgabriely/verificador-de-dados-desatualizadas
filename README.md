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

# Como usar

Faça o upload das duas planilhas (desatualizada e atualizada) para o ambiente.
Execute o código.
O código irá gerar uma nova planilha Excel com as franquias desatualizadas, salva como dados_desatualizadas_com_status.xlsx.


ACESSE O CODIGO FONTE NAS PASTAS DESTE REPOSITORIO







