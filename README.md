# postman

# O que é?
Este repositório é criado para o bootcamp

# Tecnologias utilizadas
Postman
Newman
newman htmlextra
node version  v22.15.0
newman-reporter-html

# Documentações
Visite a  documentação utilizada(https://serverest.dev/))<br/>
API Utilizada: (https://serverest.dev/)

# Como instalar o ambiente
2° Baixe o node clicando aqui [BaixarNode](https://nodejs.org/en/download)<br/>
3° Realize a instalação do newman de forma global clicando no link:   [BaixarNewman](https://www.npmjs.com/package/newman)<br/>
```
npm install -g newman 
```
3ºterceiro: realize a instalação da dependência dos relatórios [newman-reporter-html](https://www.npmjs.com/package/newman-reporter-html) 

```
npm install -g newman newman-reporter-html
```
# Como rodar os testes
- import collection e environments
- execute os testes de forma manual ou automatizada

# Pelo newman
-abra o console de sua preferência CMD (que é o prompt de comandos do windows, powelshell e execute a linha de comandos abaixo:
Obs: o comando abaixo executa todos os testes
"""
newman run serverest.postman_collection.json -e ServerRest_env.postman_environment -r cli
"""
 # Gerando os relatórios de testes

 newman run serverest.postman_collection -e ServerRest_env.postman_environment -r cli,htmlextra --reporter-htmlextra-export ./relatorios/resultado.html

#Report 
Se você optou por rodar os testes com o htmlextra, você gerou um arquivo html com o resultados dos testes e para verificar as validações, você deve abrir a pasta **newman** que foi criado no local em que os arquivos de collection e environmet se encontram.  
