---
published: true
title: DisplayFeatures
layout: post
---
# Habilitar o DisplayFeatures do Google Analytics

[Exigências para utilização do Display Features](https://support.google.com/analytics/answer/2700409)

## Cookies

Os cookies são informações enviadas do cliente (um browser) para um o servidor de rede (um site da web). Geralmente, ficam armazenados no navegador por um período de tempo determinado e são utilizados para salvar informações de uma visita ou sessão.

### Origem do cookie

Os cookies são considerados de primeira pessoa quando as informações são enviadas para o mesmo servidor de rede que disponibiliza e hospeda o site.

Exemplo: quando visitamos **www12.senado.gov.br** o browser recebe um cookie de nome `__ac`. A partir daí, toda requisição feita a uma página no domínio **www12.senado.gov.br**, e somente neste domínio, enviará de volta para o servidor o valor desse cookie.

Já os cookies de terceira pessoa, enviam informações para um servidor distinto daquele que foi visitado. Exemplo: quando visitamos **g1.globo.com**, algumas informações coletadas durante esta sessão são enviadas para o **azure-2mobile.netdna-ssl.com**.

> O administrador do site não possui controle dos dados transmitidos pelos cookies de terceira pessoa, tampouco possui conhecimento sobre como esses dados são coletados ou utilizados.

## DisplayFeatures

O Google Anlytics é um sistema que permite a coleta de dados estatísticos relacionados ao tráfego em um site da web. Essa coleta é feita por meio de um Tracker, que nada mais é do que um trecho de código inserido em todas as páginas que se queira analisar. A cada ação de um visitante em um site habilitado, o Tracker envia para os servidores do Google algumas informações inerentes à própria visita, como, por exemplo:

- o título da página acessada
- o tempo em que o usuário está ativo
- o dispositivo utilizado
- como o visitante chegou ao site

Os cookies armazenados nessa situação são de primeira pessoa (são enviados apenas para o servidor que hospeda o site habilitado).

Além das métricas de tráfego, o Google Analytics também permite também a coleta de informações demográficas e de informações de interesse dos visitantes de um site habilitado. Este recurso é chamado de _DisplayFeatures_.

Com o _DisplayFeatures_ habilitado, ao invés dos dados transitarem pela rede do Analytics, eles serão transmitidos pela rede de publicidade do Google, o DoubleClick (via cookies de terceira pessoa).

Para aderir ao _DisplayFeatures_, o Google exige que seja notificado aos seus usuários (i) quais os recursos de publicidade do Google estão em uso, (ii) como os cookies de primeira pessoa e os cookies de terceira pessoa são utilizados, e (iii) como os visitantes podem desabilitar o rastreio de comportamento durante as sessões no site habilitado (opt-out).

Além da notificação, também é exigido que não haja cruzamento de informações que possam identificar pessoalmente um visitante com informações coletadas pelo _DisplayFeatures_, a menos que o visitante _expressamente_ concorde com a coleta (opt-in).

## Exemplos de Políticas de Privacidade

Sites que utilizam o Analytics sem o _DisplayFeatures_:

- <https://www.gov.uk/help/cookies> (não compartilha nem os dados de métricas com o Google)
- <https://www.whitehouse.gov/privacy/cookies>
- <http://www.gouvernement.fr/mentions-legales#cookies>
- <https://www.bundesregierung.de/Webs/Breg/EN/Service/Datenschutz_en/_node.html>

Sites que utilizam o Analytics com o _DisplayFeatures_ mas não possuem política de privacidade adequada:

- <http://www.ufabc.edu.br/>
- <http://www.agu.gov.br/>
- <http://www.ebc.com.br/>
- <http://www.cgu.gov.br/>
- <http://www2.planalto.gov.br>
- <http://www.aneel.gov.br/>
- <http://www2.camara.leg.br/>

## Links

- <https://www.gov.uk/service-manual/making-software/analytics-tools.html#privacy>
- <https://www.blog.gov.uk/cookies/>
- <http://www.pcworld.com/article/158563/whitehouse_gov_cookies.html>
