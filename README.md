> Este tutorial é público e estará em atualização constante!. [Como contribuir?](#contribuições)

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

Para construirmos nosso projeto precisamos ter algumas ferramentas à nossa disposição. E ter as ferramentas adequadas significa ter o ambiente de desenvolvimento preparado para executar nosso projeto.

### Ferramentas que iremos utilizar:

- Node.js (versão 14.5.0)
- NVM ou ASDF
- NPM
- MDX Deck
- Code Surfer
- VS Code

<br>

Escolha um diretório dentro da sua máquina para executar o projeto e os comandos que serão informados aqui neste tutorial. 

Você pode usar o diretório onde se encontram seus outros projetos, pois quando iniciarmos este novo projeto com Code Surfer ele criará uma nova com seu nome.

Acesse pelo terminal o diretório escolhido (Seja do Windows, Linux ou IOS) e vamos para a instalação de cada um deles.

[Menu🔝](#menu)

---

### Node.js

Para que o projeto com Code Surfer e MDX-Deck funcione perfeitamente, é necessário que você tenha a versão do Node.js instalado corretamente na sua máquina.

Baixe diretamente do site oficial do [Node.js](https://nodejs.org/dist/v18.16.0/node-v18.16.0-x64.msi). Ou, para instalar manualmente pelo terminal do linux, digite o seguinte comando:

```
sudo apt-get install nodejs
```

Após terminar a instalação, confira a versão instalada com o seguinte comando:

```
node -v
```
<br>

#### Importante!!!
**_O projeto com Code Surfer e Mdx-Deck funciona melhor com as versões mais antigas do Node.js como, por exemplo, a versão 14.5.0._**

E agora?!

Agora devemos utilizar um gerenciador de versões, para alterarmos o Node.js para a versão mais adequada ao projeto. É aí que entra o NVM ou o ASDF.

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

Caso prefira não instalar o NVM e sim instalar o ASDF, pule para o próximo passo.

<br>

### ASDF

O ASDF (Another System Version Manager) permite que você instale e gerencie diferentes versões de linguagens em um único sistema, e permite alternar facilmente entre as versões instaladas. ( *[Fonte: Documentação do ASDF](https://asdf-vm.com/pt-br/guide/getting-started.html)* )

A instalação do ASDF envolve:

1- Instalar as dependências;
2- Instalar o núcleo do asdf;
3- Adicionar o asdf ao seu shell;
4- Instalar um plugin para cada ferramenta que você gostaria de gerenciar;
5- Instalar uma versão desta ferramenta;
6- Definir uma versão global e uma versão local através do arquivo de configuração ```.tool-versions```;

> **Você pode também acompanhar o passo a passo da instalação  [neste vídeo](https://www.youtube.com/watch?v=8W3xaSPjeog).**

#### 1 - Instalando as dependências

O ASDF requer principalmente ```git``` & ```curl```. Instale estas dependências com o seguinte comando:

```
apt install curl git
```

#### 2 - Faça o download

Com o comando abaixo faça o download do ASDF:

```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.11.3
```

#### 3 - Adicionando ao seu shell

Existem diversas combinações de shells, sistemas operacionais e métodos de instalação que podem impactar a configuração. Abaixo, expanda a seção que se adeque mais com o seu sistema:

Adicione esta linha ao seu ```~/.bashrc```:

```
. "$HOME/.asdf/asdf.sh"
```

O auto completar deve ser configurado manualmente a partir da adição da seguinte linha ao ```.bashrc```:

```
. "$HOME/.asdf/completions/asdf.bash"
```

Reinicie seu shell para que as mudanças na variável PATH tenham efeito. Abrir uma nova janela/sessão de terminal irá fazer isso.

#### 4 - Instalando um plugin

Para demonstração, vamos instalar e configurar o Node.js através do plugin ```asdf-nodejs```.

**Dependências dos plugins**

Cada plugin possui algumas dependências, por isso precisamos checar no repositório onde elas estão listadas. Por exemplo, para o ```asdf-nodejs``` são:

```
apt-get install dirmngr gpg curl gawk
```

Devemos instalar instalar as dependências primeiro, pois alguns plugins exigem algumas ações após a instalação.

**Instalando o plugin**

```
asdf plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
```

#### 5 - Instalando uma versão

Agora temos o plugin para o Node.js, nós podemos instalar uma versão desta ferramenta.

Podemos ver quais versões tão disponíveis através do comando ```asdf list all nodejs```, ou uma lista específica de versões com ```asdf list all nodejs 14```

#### 6 - Definindo uma versão

O ASDF executa uma verificação das versões das ferramentas a serem utilizadas através do arquivo ```.tool-versions``` presente desde diretório atual, até o diretório ```$HOME```. A varredura ocorre no momento em que você executa uma ferramenta que o asdf gerencia.

**Versões globais**

Os padrões globais são gerenciados em ```$HOME/.tool-versions```. Defina uma versão global para ser utilizada como padrão nos demais projetos, através do comando:

```asdf global nodejs latest```

```$HOME/.tool-versions``` ficará assim:

```nodejs <versão desejada>```

**Versões locais**
Versões locais são definidas no arquivo ```$PWD/.tool-versions``` (seu diretório atual). Geralmente, será um repositório Git para um projeto. Quando estiver no diretório desejado, execute:

```asdf local nodejs latest```

```$PWD/.tool-versions``` ficará assim:

```nodejs 14.5.0```

**Setup finalizado!**

A configuração inicial do ASDF foi finalizada 🎉. Agora, você pode gerenciar versões do nodejs para o seus projetos. Siga passos semelhantes para cada ferramenta do seu projeto.

O ASDF possui diversos outros comandos para se acustomar ainda, você pode ver todos eles através do comando ```asdf --help``` ou simplesmente ```asdf```. 

Agora com a versão correta do Node.js podemos passar para a próxima ferramenta que é o NPM.

[Menu🔝](#menu)


---

### NPM

O NPM (Node Package Manager) é um repositório on-line de pacotes de software Node.js prontos para uso, e é acessado usando o comando "npm" a partir do terminal ou da linha de comando. Além disso, ele é capaz de gerenciar as dependências de um projeto, permitindo que os desenvolvedores especifiquem quais pacotes ou bibliotecas o projeto precisa para ser executado corretamente.

**O NPM é instalado automaticamente com o Node.js.** Portanto, se você já tiver o Node.js instalado em seu sistema, o NPM já estará disponível.

Mesmo assim, só para ter certeza, você pode verificar se a sua máquina está com o NPM instalado corretamente, digitando o seguinte comando no terminal:

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

Code Surfer é uma biblioteca de apresentação de programação, criada pelo incrível desenvolvedor @pomber, que permite incorporar código ao vivo nas apresentações e visualizar os resultados em tempo real. Ele é altamente configurável e suporta diferentes temas, apresentações em tela cheia, gravação de apresentações em vídeo e muito mais.

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

Antes de rodarmos o projeto com o próximo código, é necessário fazer mais um procedimento: Incluir arquivo ```.tool-versions``` na raiz do projeto. Este arquivo vai definir a versão do node.js que está sendo usada.

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

Caso você queira dar uma sugestão, fazer uma reclamação ou me pagar um café, crie uma *issue* contendo as informações sugeridas que ela será analisada como contribuição.

Aqui estão os atuais contribuidores deste projeto:

[![Contributors](https://contributors-img.web.app/image?repo=mikaelmonteirodev/code-surfer-test)](https://github.com/mikaelmonteirodev/code-surfer-test/graphs/contributors)

[Menu🔝](#menu)


---

### Licença

[Licença MIT](https://github.com/mikaelmonteirodev/code-surfer-project/blob/main/LICENSE)

[Menu🔝](#menu)

