# Como iniciar meu projeto em Code-Surfer?

Neste tutorial, iremos aprender como instalar as dependências necessárias para contruirmos nosso projeto com Code Surfer e MDX-Deck. A princípio ele parece grande, pode dar preguiça, mas vale a pena, pois tá bem fácil de ler e de usar.

---

## Resumo
Primeiramente nós temos que organizar nosso ambiente de desenvolvimento com as tecnologias necessárias para a instalação e execução do nosso projeto de acordo com que pede a documentação de cada aplicação. E é ísso que vamos fazer agora.

---
## Menu

- Ambiente de Desenvolvimento
    - Lista de Ferramentas
- Iniciando o projeto com Code Surfer
    - Comandos
    - Instalando
    - Acessando
- Usando
- Contribuidores
- Licença

---

## Ambiente de Desenvolvimento

Para construírmos nosso projeto precisamos ter algumas ferramentas à nossa disposição. E ter as ferramentas adequadas significa ter o ambiente de desenvolvimento definido.

#### Ferramentas que iremos utilizar:

- Node.js (versão 14.5.0)
- NVM ou ASDF
- NPM
- MDX Deck
- Code Surfer
- VS Code

---

## Ambiente de Desenvolvimento

Para construírmos nosso projeto precisamos ter algumas ferramentas à nossa disposição. E ter as ferramentas adequadas significa ter o ambiente de desenvolvimento definido.

#### Ferramentas que iremos utilizar:

- Node.js (versão 14.5.0)
- NVM ou ASDF
- NPM
- MDX Deck
- Code Surfer
- VS Code

Escolha um diretório dentro da sua maquina para executar o projeto e os comandos que serão informados aqui neste tutorial. 

Você pode usar o diretório onde se encontram seus outros projetos, pois quando iniciarmos o projeto com Code Surfer ele criará uma nova pasta para ele.

Acesse o diretório escolhido pela terminal (Seja do Windows, Linux ou IOS) e vamos para a instalação de cada um deles.

#### Node.js

Para que o projeto com Code Surfer e MDX-Deck funcione perfeitamente, é necessário que você tenha a versão do Node.js instalado corretamente na sua maquina.

Baixe diretamente do site oficial do [Node.js](https://nodejs.org/dist/v18.16.0/node-v18.16.0-x64.msi). Ou, para instalar manualmente pelo terminal do linux, digite o seguinte comando:

```
sudo apt-get install nodejs
```

Após terminar a instalação, confira a versão instalada com o seguinte comnando:

```
node -v
```

###### Importante!
O projeto com Code Surfer e Mdx-Deck funciona melhor com as versões mais antigas do Node.js, como por exemplo a versão 14.5.0.

E agora?!

Agora devemos utilizar um gerenciador de versões, para alterarmos o Node.js para a versão mais adequada ao projeto. É aí que entram o NVM ou o ASDF.

---

#### NVM ou ASDF

Tanto o NVM quanto o ASDF são ferramentas muito úteis para desenvolvedores que precisam trabalhar com diferentes versões de linguagens de programação em um único sistema. Eles permitem que você instale e gerencie várias versões de uma linguagem de programação e suas dependências, sem precisar se preocupar com conflitos entre as diferentes versões instaladas.
<br>

###### NVM

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
Por exemplo, para instalar o Node.js na versão 14.5.0, você pode usar o seguinte comando:

```
nvm install 14.5.0
```
<br>

###### ASDF

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

<br>

###### NPM

O NPM (Node Package Manager) 
é um repositório on-line de pacotes de software Node.js prontos para uso, e é acessado usando o comando "npm" a partir do terminal ou da linha de comando. Além disso, ele é capaz de gerenciar as dependências de um projeto, permitindo que os desenvolvedores especifiquem quais pacotes ou bibliotecas o projeto precisa para ser executado corretamente.

Para verificar se a sua máquina está com o NPM instalado correta












<!-- # MDX Deck + Code Surfer template

This project was generated with the `npm init code-surfer-deck` command.

## Development

To run the presentation deck in development mode:

```sh
npm start
```

Edit the [`deck.mdx`](deck.mdx) file to get started.

## Exporting

To build the presentation deck:

```sh
npm run build
```

For more documentation see [MDX Deck](https://github.com/jxnblk/mdx-deck) and [Code Surfer](https://codesurfer.pomb.us/) -->
