> Este tutorial é público e estará sempre aberto para contribuições. [Veja](#contribuições)

# Como iniciar meu projeto em Code-Surfer?

Este README tem a intenção de servir como tutorial. E nele, iremos aprender como instalar as dependências necessárias para construirmos nosso projeto com MDX-Deck e Code Surfer. 

A princípio ele parece grande, pode dar preguiça, mas vale a pena, pois está bem fácil de ler e de executar.

---

## Menu

- [Ambiente de Desenvolvimento](#ambiente-de-desenvolvimento)
    - [Lista de Ferramentas](#ferramentas-que-iremos-utilizar)
        - [Node.js](#nodejs)
        - [NVM ou ASDF](#nvm-ou-asdf)
            - [NVM](#nvm)
            - [ASDF](#asdf)
        - [NPM](#npm)
        - [MDX-Deck e Code Surfer](#mdx-deck-e-code-surfer)
            - [MDX-Deck](#mdx-deck)
            - [Code Surfer](#code-surfer)
            - [Instalando o MDX-Deck + Code Surfer](#instalando-o-mdx-deck--code-surfer)
- [Contribuições](#contribuições)
- [Licença](#licença)

---

## Ambiente de Desenvolvimento

Para construírmos nosso projeto precisamos ter algumas ferramentas à nossa disposição. E ter as ferramentas adequadas significa ter o ambiente de desenvolvimento preparado para executar nosso porjeto.

### Ferramentas que iremos utilizar:

- Node.js (versão 14.5.0)
- NVM ou ASDF
- NPM
- MDX Deck
- Code Surfer
- VS Code

<br>

Escolha um diretório dentro da sua maquina para executar o projeto e os comandos que serão informados aqui neste tutorial. 

Você pode usar o diretório onde se encontram seus outros projetos, pois quando iniciarmos este novo projeto com Code Surfer ele criará uma nova com seu nome.

Acesse pelo terminal o diretório escolhido (Seja do Windows, Linux ou IOS) e vamos para a instalação de cada um deles.

[Menu🔝](#menu)

---

### Node.js

Para que o projeto com Code Surfer e MDX-Deck funcione perfeitamente, é necessário que você tenha a versão do Node.js instalado corretamente na sua maquina.

Baixe diretamente do site oficial do [Node.js](https://nodejs.org/dist/v18.16.0/node-v18.16.0-x64.msi). Ou, para instalar manualmente pelo terminal do linux, digite o seguinte comando:

```
sudo apt-get install nodejs
```

Após terminar a instalação, confira a versão instalada com o seguinte comando:

```
node -v
```
<br>
###### **Importante!**
**_O projeto com Code Surfer e Mdx-Deck funciona melhor com as versões mais antigas do Node.js, como por exemplo a versão 14.5.0._**

E agora?!

Agora devemos utilizar um gerenciador de versões, para alterarmos o Node.js para a versão mais adequada ao projeto. É é aí que entram o NVM ou o ASDF.

[Menu🔝](#menu)


---
### NVM ou ASDF

Tanto o NVM quanto o ASDF são ferramentas muito úteis para desenvolvedores que precisam trabalhar com diferentes versões de linguagens de programação em um único sistema. Eles permitem que você instale e gerencie várias versões de uma linguagem de programação e suas dependências, sem precisar se preocupar com conflitos entre as diferentes versões instaladas.
<br>

### NVM

O NVM (Node Version Manager) é um gerenciador de versão para o Node.js. Ele permite que você instale e gerencie várias versões do Node.js em um único sistema, e permite alternar facilmente entre as versões instaladas. Com o NVM, você pode facilmente instalar diferentes versões do Node.js e alternar entre elas usando um único comando no terminal.

Para instalar o NVM no seu sistema Linux ou macOS, você pode seguir os seguintes passos:

1 - Abra o terminal no seu sistema.
2 - Baixe o script de instalação do NVM usando o comando ```curl```:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
```
Este comando baixa o script de instalação do NVM diretamente do repositório oficial no GitHub e o executa usando o Bash.

3 - Após a instalação ser concluída, você pode verificar se o NVM foi instalado corretamente digitando o seguinte comando no terminal:

```
nvm --version
```
4 - Agora, você pode usar o NVM para instalar o Node.js em uma versão específica usando o seguinte comando:

```
nvm install <versão>
```
No caso deste projeto, para instalar o Node.js na versão 14.5.0, você deve usar o seguinte comando:

```
nvm install 14.5.0
```
<br>

### ASDF

O ASDF (Another System Version Manager) permite que você instale e gerencie diferentes versões de linguagens em um único sistema, e permite alternar facilmente entre as versões instaladas.

O comando para instalar o ASDF depende do sistema operacional que está sendo utilizado. Aqui estão os comandos para algumas plataformas comuns:

No Ubuntu ou Debian digite:

```
sudo apt-get install asdf
```

No macOS (usando Homebrew) digite:

```
brew install asdf
```

No Arch Linux digite:

```
sudo pacman -S asdf
```

Para verificar a versão do ASDF instalada no seu sistema, você pode usar o seguinte comando no terminal:

```
asdf --version
```

Para alterar a versão do Node.js usando o ASDF, você pode usar o seguinte comando:

```
asdf global node <versão>
```

Substitua <versão> pela versão específica do Node.js que você deseja usar. Por exemplo, se você quiser mudar para a versão 14.5.0, o comando seria:

```
asdf global node 14.5.0
```

Pronto!

Agora com a versão correta do Node.js podemos passar para a próxima ferramenta que é o NPM.

[Menu🔝](#menu)


---

### NPM

O NPM (Node Package Manager) é um repositório on-line de pacotes de software Node.js prontos para uso, e é acessado usando o comando "npm" a partir do terminal ou da linha de comando. Além disso, ele é capaz de gerenciar as dependências de um projeto, permitindo que os desenvolvedores especifiquem quais pacotes ou bibliotecas o projeto precisa para ser executado corretamente.

**O NPM é instalado automaticamente junto com o Node.js.** Portanto, se você já tiver o Node.js instalado em seu sistema, o NPM já estará disponível.

Mesmo assim, só para ter certeza, você pode verificar se a sua máquina está com o NPM instalado corretamente, digitando o seguinte comando no termimal:

```
npm -v
```

[Menu🔝](#menu)


---

### MDX-Deck e Code Surfer

MDX-Deck e Code Surfer são duas bibliotecas de código aberto que permitem criar apresentações interativas usando React e MDX.

### MDX-Deck

Com o MDX-Deck, os usuários podem criar apresentações com componentes React personalizados e utilizar a sintaxe de Markdown para formatar o conteúdo.

O MDX-Deck é altamente configurável e fornece recursos para personalizar a aparência e o comportamento das apresentações. Ele também suporta temas personalizados e é fácil de usar para iniciantes, enquanto ainda oferece recursos avançados para usuários experientes.

Alguns dos recursos do MDX-Deck incluem a capacidade de criar transições personalizadas entre os slides, incorporar código ao vivo e suporte para apresentações em tela cheia. Com o MDX-Deck, é possível criar apresentações profissionais e envolventes em pouco tempo.

### Code Surfer

Code Surfer é uma biblioteca de apresentação de programação que permite incorporar código ao vivo nas apresentações e visualizar os resultados em tempo real. Ele é altamente configurável e suporta diferentes temas, apresentações em tela cheia, gravação de apresentações em vídeo e muito mais.

### Instalando o MDX-Deck + Code Surfer

Com as ferramentas anteriores devidamente instaladas, nós temos agora um ambiente local organizado para iniciar nosso projeto.

Ainda dentro do seu diretório escolhido, digite o seguinte comando no terminal:

```
npm init code-surfer-deck nome-do-seu-projeto
```

Substitua _**"nome-do-seu-projeto"**_ pelo nome do seu projeto.

Com o código acima digitado, o MDX-Deck e o Code Surfer irão criar as dependências do seu projeto com os arquivos e pastas necessários para que você possa rodar a sua apresentação.

Quando a instalação terminar, acesse a pasta do seu novo projeto pelo terminal com o comando:

```
cd nome-do-seu-projeto
```

Antes de rodarmos o projeto com o próximo código, é necessário fazer mais um procedimento: Inlcuir arquivo ```.tool-versions``` na raiz do projeto. Este arquivo vai definir a versão do node.js que está sendo usada.

Para isso, dentro do diretório do seu projeto, digite:

```
code .
```

Este comando vai abrir seu projeto dentro do **VSCode**. E por ele mesmo você criar o arquivo ```.tool-versions```.

Após criado, abra o arquivo e digite o texto ```Nodejs 14.5.0``` que é a versão do node.js que será usado no projeto.

Depois disso salve seu projeto e continue o próximo passo.

Agora é hora de rodar o projeto! Digite no terminal o seguinte comando:

```
npm start
```

O comando ```npm start``` vai rodar seu projeto e abrirá uma janela no navegador mostrando uma apresentação de slides de demonstração, feita com MDX-Deck e Code Surfer.

Pronto! Agora projeto está preparado para receber sua apresentação. E ela deve ser preparada no arquivo principal, chamado ```deck.mdx```.

Para saber todas as funcionalidades do Code Surfer acesse https://codesurfer.pomb.us e use a criatividade.

[Menu🔝](#menu)


---

### Contribuições

Este tutorial é público e estará sempre aberto para contribuições.

Caso você queira dar uma sugestão, fazer uma reclamação ou me pagar um café, crie uma issue contendo as informações sugeridas que ela será analisada como contribuiçõa.

Aqui estão os atuais contribuidores deste projeto:

[![Contributors](https://contributors-img.web.app/image?repo=mikaelmonteirodev/code-surfer-test)](https://github.com/mikaelmonteirodev/code-surfer-test/graphs/contributors)

[Menu🔝](#menu)


---

### Licença


[Menu🔝](#menu)

