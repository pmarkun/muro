# Pré-Requisitos

## PHP
* php5-gd

No Ubuntu:

apt-get install php5-gd

## Python
* birdy

No Ubuntu:

apt-get install pip
pip install birdy

## Como usar

Configure o settings.py (copie do template settings.py-template) com os códigos das APIs e a tag.

* Twitter -> https://apps.twitter.com/
* Instagram -> https://instagram.com/developer/
* Flickr -> https://www.flickr.com/services/api/misc.api_keys.html


O sistema esta divido em duas partes:

1) Backend -> Script.py

Desenvolvido em Python e responsável por raspar os serviços e gerar um arquivo 'muro.json' com as informações e urls das fotos.

2) Interface -> index.html

A interface roda direto no cliente e toda a interação é feita com javascript.
A excessão é o timthumb.php que é um pequeno script php para gerar um cache local dos thumbnails das imagens.


Para funcionar:
Rode o script.py para capturar as tags.
É preciso rodar ele de tempos em tempos (usando cron ou qualquer outro sistema de atualização) para manter o site atualizado.

Deixe o index.html em algum ponto vísivel do seu webserver.

**Atenção:** Verifique se o diretório 'cache' esta acessível para escrita pelo servidor. 
