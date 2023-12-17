---
# Projeto de Testes Automatizados de API REST | Postman | JSON Schema | Newman | GitHub Actions :test_tube:
---
# :information_source: Introdução 
Esse projeto "testes-automatizados-api-serve-rest_postman" é executado em um ambiente de desenvolvimento na ["API REST"](https://serverest.dev) do ["ServeRest"](https://github.com/ServeRest) que simula uma loja virtual, com o objetivo de me aprofundar um pouco mais nos estudos sobre validações de testes de API (Ex.: JSON Schema, geração de massa de dados dinâmicos, etc) nas ferramentas Postman, Newman e GitHub Actions.

---
# :dart: Executar testes automatizados de API da collection e environment do Postman, Gerar e armazenar relatório html no GitHub Actions 
- Nesse repositório, acessar a aba "Actions"
- Na seção "Actions", clicar em "Pipeline Testes Automatizados API ServeRest Postman"
- Em "This workflow has a workflow_dispatch event trigger.", clicar em "Run workflow" > "Run workflow" para executar testes automatizados de API da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições, gerar e armazenar relatório html no GitHub Actions
- Após o término da execução, clicar na run "Pipeline Testes Automatizados API ServeRest Postman"
- Na seção "Artifacts", clicar em "relatorio-api-serve-rest-postman"
- Na janela aberta, escolher um diretório para baixar a pasta compactada "relatorio-api-serve-rest-postman.zip"

# Verificar no navegador padrão o relatório html gerado e armazenado anteriormente no GitHub Actions e descompactado no computador :female_detective: 
- Abrir uma janela do "Windows Explorer"
- Acessar o diretório onde foi baixada a pasta compactada "relatorio-api-serve-rest-postman.zip" anteriormente
- Descompactar a pasta
- Acessar a pasta descompactada "relatorio-api-serve-rest-postman"
- Clicar 2 vezes sob o relatório "relatorio-api-serve-rest-postman.html" gerado e armazenado anteriormente no GitHub Actions e descompactado para ser aberto e verificado no navegador padrão no computador

  
# Antes de clonar ou executar esse projeto localmente no computador, é necessário seguir as instruções abaixo :point_down:

## :hammer_and_wrench: Janela do "Windows Explorer", criar uma pasta "tools"
- Abrir uma janela do "Windows Explorer"
- Acessar o diretório "C:"
- Criar uma pasta "tools"


## :hammer_and_wrench: Cmder (Console Emulator)
- Baixar o [Console Emulator (cmder)](https://github.com/cmderdev/cmder/releases/download/v1.3.5/cmder.zip)
- Clicar com botão direito na pasta compactada > Extrair para "cmder"
- Mover a pasta descompactada "cmder" para o diretório "C:\tools" criado anteriormente
- Acessar o diretório "C:\tools\cmder"
- Clicar com botão direito no executável "cmder.exe" > Enviar para > Área de trabalho (criar atalho)
- Acessar a Área de Trabalho
- Clicar 2 vezes no atalho "Cmder - Atalho"
- Clicar na opção "Unblock and Continue"


## :hammer_and_wrench: Instalar as dependências necessárias 
### Desinstalar completamente Node.js e npm que já foram instalados em algum outro momento
- Seguir os passos apresentados nesse link ["COMO REMOVER COMPLETAMENTE O NODE.JS DO WINDOWS?"](https://acervolima.com/como-remover-completamente-o-node-js-do-windows/#:~:text=Pesquise%20por%20programa%20e%20recursos,js%20e%20desinstale-o.)
  
### Node versão 18.12.1
- Baixar e instalar o [node v18.12.1](https://nodejs.org/dist/v18.12.1/) > node-v18.12.1-x64.msi
- Abrir um novo cmder ou outro terminal de preferência
- Informar o comando abaixo para confirmar se o node realmente foi instalado
```
node --version
```
- Verificar se foi retornada a mesma versão do node instalada anteriormente
```
v18.12.1
```
- Informar o comando abaixo para confirmar se o npm realmente foi instalado
```
npm --version
```
- E verificar se foi retornada essa mesma versão do npm:
```
8.19.2
```

### newman
- No cmder ou terminal aberto anteriormente, informar o comando abaixo para instalar o newman
```
npm install -g newman
```
- Informar o comando abaixo para verificar se foi retornada alguma versão e confirmar se o newman realmente foi instalado
```
newman --version
```

### newman-reporter-htmlextra
- No cmder ou terminal aberto anteriormente, informar o comando abaixo para instalar o newman-reporter-htmlextra
```
npm install -g newman-reporter-htmlextra
```
- Informar o comando abaixo para verificar se foi retornada alguma versão e confirmar se o newman-reporter-htmlextra realmente foi instalado
```
newman-reporter-htmlextra --version
```
- Fechar esse cmder ou terminal

### Baixar, instalar e configurar o git
- Caso ainda não tenha o git baixado e instalado, acessar o site do [git](https://git-scm.com/download/win), baixar e instalar
- Caso ainda não tenha configurado o git, seguir os passos apresentados nesse link [Configure a ferramenta](https://training.github.com/downloads/pt_BR/github-git-cheat-sheet/#:~:text=Configure%20a%20ferramenta) e configurar


## :hammer_and_wrench: Clonar o projeto
- Abrir uma janela do "Windows Explorer"
- Acessar o diretório onde será clonado o projeto "testes-automatizados-api-serve-rest_postman"
- Copiar esse diretório 
- Abrir um novo cmder 
- Informar o comando abaixo para acessar onde será clonado o projeto
```
cd "<diretório copiado anteriormente>"
```
Ex.: 
```
cd "C:\PROJETOS\Automação\Postman"
```
- Informar o comando abaixo para clonar este repositório via "HTTPS"
```
git clone https://github.com/AndressaKarla/testes-automatizados-api-serve-rest_postman.git
```
- Ou informar o comando abaixo para clonar este repositório via "SSH"
```
git clone git@github.com:AndressaKarla/testes-automatizados-api-serve-rest_postman.git
```


# :dart: Executar testes automatizados de API da collection e environment do Postman e Gerar relatório diretamente no terminal no computador
- No cmder aberto anteriormente, informar o comando abaixo para acessar o projeto “testes-automatizados-api-serve-rest_postman”
```
cd "testes-automatizados-api-serve-rest_postman"
```
Ex.: 
```
C:\PROJETOS\Automação\Postman\testes-automatizados-api-serve-rest_postman
```
- Informar o comando abaixo para executar testes automatizados de API da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições e Gerar relatório diretamente no terminal
```
newman run ./nome-collection.json -e ./nome-environment.json --delay-request 2
```
Ex.: 
```
newman run ./api-serve-rest_collection.json -e ./api-serve-rest_dev-environment.json --delay-request 2
```

# :dart: Executar testes automatizados de API da collection e environment do Postman e Gerar relatório html na pasta "relatorios" no computador
- No cmder aberto anteriormente, informar o comando abaixo para executar testes automatizados de API da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições e Gerar relatório html na pasta "relatorios" no computador (mesmo comando que é utilizado no "Passo 4" da "Pipeline Testes Automatizados API ServeRest Postman" em ".github > workflows > [workflow-testes-automatizados-api-serve-rest-postman.yml](https://github.com/AndressaKarla/testes-automatizados-api-serve-rest_postman/blob/main/.github/workflows/workflow-testes-automatizados-api-serve-rest-postman.yml)" no GitHub Actions)
```
newman run ./nome-collection.json -e ./nome-environment.json --delay-request 2 --reporters cli, -r htmlextra --reporter-htmlextra-export ./relatorios/nome-relatorio.html
```
Ex.: 
```
newman run ./api-serve-rest_collection.json -e ./api-serve-rest_dev-environment.json --delay-request 2 --reporters cli, -r htmlextra --reporter-htmlextra-export ./relatorios/relatorio-api-serve-rest-postman.html
```
- Fechar esse cmder

---
# Verificar no navegador padrão o relatório html gerado na pasta "relatorios" anteriormente no computador :female_detective:
- Abrir uma janela do "Windows Explorer"
- Acessar o diretório onde foi clonado o projeto “testes-automatizados-api-serve-rest_postman”

Ex.: 
```
C:\PROJETOS\Automação\Postman\testes-automatizados-api-serve-rest_postman
```
- Acessar a pasta "relatorios" 
- Clicar 2 vezes sob o relatório "relatorio-api-serve-rest-postman.html" gerado anteriormente no computador para ser aberto e verificado no navegador padrão

---
### Feito com ❤️ por Andressa Karla :wave: 

### [![Medium](https://img.shields.io/badge/-Medium-595D60?style=plastic&logo=Medium&logoColor=white&link=https://medium.com/@andressakarla)](https://medium.com/@andressakarla) [![Linkedin](https://img.shields.io/badge/-LinkedIn-595D60?style=plastic&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/andressakarla//)](https://www.linkedin.com/in/andressakarla/)

---
