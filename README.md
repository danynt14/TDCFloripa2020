# TDCFloripa2020 - Exemplo de POC's que eu appresentei na Talk

##Nod-Red


### Gera um número aleatório e retorna o valor no debug do Node-Red(Fluxo está ilustrado na apresentação acima)

[{"id":"6abb2480.d3c59c","type":"tab","label":"Flow 1","disabled":false,"info":""},{"id":"789dde05.524d1","type":"inject","z":"6abb2480.d3c59c","name":"","topic":"","payload":"","payloadType":"date","repeat":"","crontab":"","once":false,"onceDelay":0.1,"x":220,"y":160,"wires":[["c20dba4d.5ab548"]]},{"id":"9c1e77af.3a33e8","type":"debug","z":"6abb2480.d3c59c","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","x":720,"y":200,"wires":[]},{"id":"c20dba4d.5ab548","type":"function","z":"6abb2480.d3c59c","name":"RandomNumber","func":"msg.payload = Math.round( Math.random() *100)\nreturn msg;","outputs":1,"noerr":0,"x":500,"y":160,"wires":[["9c1e77af.3a33e8"]]},{"id":"4b0036c5.b4b1a8","type":"comment","z":"6abb2480.d3c59c","name":"Meu Primeiro Comentário","info":"# Informações do meu Node ^^\n\n### Markdows\n\n### ","x":590,"y":80,"wires":[]}]


### Exemplo de acender e apagar o led interno do Arduino
#### Antes você executar esse código é preciso ir na IDE do arduino e executar o exemplo na sua IDE do Arquivos>>Examplos>>Firmata>>SandardFirmata

[{"id":"fee60d22.5aedc","type":"tab","label":"Flow 6","disabled":false,"info":""},{"id":"799c5e2d.34f4f","type":"inject","z":"fee60d22.5aedc","name":"LIGA LED","topic":"","payload":"true","payloadType":"bool","repeat":"","crontab":"","once":false,"onceDelay":0.1,"x":360,"y":200,"wires":[["efde2757.f36768"]]},{"id":"efde2757.f36768","type":"arduino out","z":"fee60d22.5aedc","name":"LIGALED","pin":"13","state":"OUTPUT","arduino":"e9d514e1.c4fbd8","x":700,"y":260,"wires":[]},{"id":"7007591f.46a958","type":"inject","z":"fee60d22.5aedc","name":"DESLIGA LED","topic":"","payload":"false","payloadType":"bool","repeat":"","crontab":"","once":false,"onceDelay":0.1,"x":380,"y":300,"wires":[["efde2757.f36768"]]},{"id":"e9d514e1.c4fbd8","type":"arduino-board","z":"","device":"COM4"}]


### Outros exemplos 
#### (1)Exemplo pra ver quantos casos de covid existe
#### (2)Tradutor de um Texto através da API do Google


[{"id":"78fc6e00.f7d12","type":"tab","label":"Flow 2","disabled":false,"info":""},{"id":"fc83c956.915dc8","type":"debug","z":"78fc6e00.f7d12","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"true","targetType":"full","x":770,"y":360,"wires":[]},{"id":"19237b13.42b385","type":"worldwide","z":"78fc6e00.f7d12","name":"","infected":true,"deaths":true,"recovered":true,"active":true,"critical":true,"todaycases":true,"todaydeaths":true,"casepermilion":true,"deathspermilion":true,"x":480,"y":360,"wires":[["fc83c956.915dc8"]]},{"id":"77589fbe.962ea","type":"inject","z":"78fc6e00.f7d12","name":"","topic":"","payload":"","payloadType":"date","repeat":"","crontab":"","once":false,"onceDelay":0.1,"x":160,"y":340,"wires":[["19237b13.42b385"]]},{"id":"39f92105.c1cf8e","type":"google-translate","z":"78fc6e00.f7d12","name":"tradutor","to":"pt","x":460,"y":480,"wires":[["6882a36b.df2b0c"]]},{"id":"74c4952b.327a3c","type":"inject","z":"78fc6e00.f7d12","name":"Say Hello","topic":"","payload":"Say Hello","payloadType":"str","repeat":"","crontab":"","once":false,"onceDelay":0.1,"x":180,"y":460,"wires":[["39f92105.c1cf8e"]]},{"id":"6882a36b.df2b0c","type":"debug","z":"78fc6e00.f7d12","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"true","targetType":"full","x":740,"y":480,"wires":[]}]







