# Entendendo o problema

Vamos supor que fomos contratados por uma empresa de turismo, situada em Manaus, 
para desenvolver um pipeline de dados, ou, em inglês, data pipeline.

Extrair dados da previsão do tempo dos próximos 7 dias da cidade de Manaus e armazenar os dados, 
assim, ela poderá usá-los para organizar a programação de passeios de acordo com a previsão do tempo.

# Preparando o ambiente: API Visual Crossing

Para conseguirmos ter acesso a previsão do tempo na cidade de Manaus(Qualquer Cidade), vamos utilizar uma API chamada Visual Crossing.
Com ela, nós podemos fazer até 1000 requisições diárias de forma gratuita e ter acesso a dados passados e futuros em relação ao clima.

 https://www.visualcrossing.com
 
 Ao logar, surgem diversas informações sobre a sua conta. 
 A principal delas, é a key ("chave" em português), que será necessária para que possamos extrair os dados fornecidos pela API - 
 vale ressaltar que cada conta possui uma chave específica. Além disso, é importante que saibamos que, assim como qualquer outra API, 
 esta também possui limitações. Como estamos utilizando a versão gratuita, temos direito de realizar até 1000 requisições por dia.

Vamos acessar a documentação da API para melhor entender seu funcionamento. Para isso, clique em "More", na barra superior, e, em seguida, em "Documentation". 
Note que há diversos artigos sobre diferentes maneiras de extrair dados, mas vamos nos ater ao artigo "Timeline Weather API". Clique para abri-lo.

Esta API nos permite acessar dados antigos e atuais sobre o clima, além da previsão do tempo. Mais abaixo, após "API Request Types", 
há uma url que devemos utilizar para conseguir extrair dados da API. Perceba que, nela, constam campos que deveremos informar à url, como "location", "date" e "key", ou seja, localização, data e chave, respectivamente. 
Em seguida, estão listados outros parâmetros que também podem ser adicionados à url.

# Faça como eu fiz: desenvolvendo um pipeline de dados

Para desenvolver esse projeto, primeiro realizamos a instalação de uma biblioteca.

- Comando para instalação da biblioteca pandas
pip install pandas

Em seguida, criamos um script Python chamado extrai_infos_clima.py e rodar a extração.
