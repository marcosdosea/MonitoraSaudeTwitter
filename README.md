
# UFS - Universidade Federal de Sergipe
Bacharelando em Sistemas de Informação (2022) 👨🏽‍🎓💻  

# TRABALHO DE CONCLUSÃO DE CURSO
Título: Avaliação de Sentimentos em Mensagens da Rede Social Twitter para Apoiar Decisões de Gestão em Saúde Pública

ALUNO: Wagner Santos Prata
ORIENTADOR: Dr. Marcos Barbosa Dósea

# RESUMO
As plataformas de mídia social fornecem uma forma de obter informações por meio de interações em postagens. A realização de análises que envolvam informações da geolocalização e do sentimento das postagens podem auxiliar gestores no processo de tomada de decisão. Dessa forma, este trabalho propõe avaliar a correlação entre o sentimento de mensagens extraídas na rede social Twitter e os dados oficiais da cobertura vacinal das cidades do estado de Sergipe. Os resultados quantitativos levando em consideração os sentimentos extraídos dos textos, e classificados de acordo com a sua polaridade como positivos ou negativos, não permitiram ser generalizados devido aos custos envolvidos para obter uma quantidade significativa de dados. Entretanto, o processo proposto pode ser replicado por trabalhos futuros com capacidade de ampliar o número de mensagens analisadas e permitir incrementar o nível de evidência dos resultados.

# ORIENTAÇÕES
Este notebook foi desenvolvido usando a ferramenta Google Colab.
Para ter acesso as permissões é necessário criar uma conta na rede social Twitter e em seguida deve-se escrever na plataforma de desenvolvedor para configurar o projeto de pesquisa e obter as chaves token.

## FLUXO DE EXECUÇÃO DO CÓDIGO

### Instalações das Bibliotecas
Nessa etapa são instaladas as principais bibliotecas que serão usadas para execução do programa e a declaração das chaves de acesso disponibilizadas pela APIs (application programming interfaces) Twitter.

### Extração de dados Twitter
Essa etapa caracteriza a extração de dados na rede social twitter para isso é necessário informar corretamente os atributos da pesquisa.
Definir as coordenadas geográficas, o período de 7 dias, as palavras relacionadas a pesquisa, a linguagem e a quantidade de tweets a serem colhidos. Além disso, essa etapa gerar um arquivo json e csv que serão trabalhados nas próximas etapas.

### Limpeza de Dados
Essa etapa tem a função de remover alguns ruídos da base de dados dentre deles, podemos destacar arrobas (@), hashtags (#), hyperlink, marcações HTML e conversão de letras maiúsculas para minúsculo.

### Preparando para a análise sentimento
Nessa etapa de execução do código foi necessário realizar a tradução de texto, uma vez que, a biblioteca TextBlob que usaremos a seguir na análise sentimento, possui a restrição de que os textos a serem analisados estejam na língua inglesa. Para realizar a tradução das mensagens para a língua inglesa foi utilizada a biblioteca Translate. Vale ressaltar que o uso dessa biblioteca impôs uma restrição em relação ao número de mensagens analisadas, uma vez que só é permitido uma quantidade de caracteres para efetivar a tradução. Esse limite explica o motivo pelo qual apenas 59 tweets foram analisados.

### Análise de Twiiter Negativos de Positivos
Nessa etapa usaremos a biblioteca TextBlob que realiza o processamento de Dados textuais. 
A análise de sentimento realizada em cada mensagem analisada gera como resultado o nível de polaridade e o nível de subjetividade que atribui uma pontuação a cada frase indo de -1 até +1 e classificando textos que expressam uma opinião positiva (+1) ou negativa (-1). O nível de subjetividade que varia de 0 até 1 e descreve sentimentos, avaliações e impressões do internautas, quanto mais próximo de 1, mais subjetiva é a frase.
Ainda nessa etapa, é gerado o gráfico de cada cidade a partir das pontuações apresentadas pela biblioteca TextBlob.

### Nuvem de palavras
Nessa etapa é feito a análise semântica dos tweets publicados, capturando o significado através das ferramentas gráficas usando a biblioteca wordcloud. Dessa forma é possível observar as palavras relacionadas aos sintomas e preocupações associadas a COVID-19.




