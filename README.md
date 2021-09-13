

# 🗂 Alguns sites que irá nos ajudar na configuração do projeto

<li> npm : https://www.npmjs.com/ </li>
<li>Webpack 5 : https://webpack.js.org/ </li>


# 🧰 Ferramentas que precisamos instalar:

<li> Visual Studio Code : https://code.visualstudio.com/Download </li>
<li> Node (LTS): https://nodejs.org/en/download/  </li> 

# 🔨 Iniciando o projeto

Primeiro, abra o CMD e digite o seguinte comando para criar e entrar na pasta do projeto e depois criar um arquivo package.json:

mkdir meu-projeto<br>
cd meu-projeto<br>
npm init -y<br>
<br>

Agora iremos instalar o webpack, webpack-cli, react e react-dom com o seguinte comando no CMD <b>sempre dentro da pasta do arquivo do seu projeto</b> :<br>
<br>
npm install -D webpack webpack-cli react react-dom<br>
<br>
Depois disso iremos instalar a estrutura básica para o projeto, crie uma pasta "src" (sem as aspas) e dentro crie um arquivo index.js e outro arquivo chamando app.js <br>

![image](https://user-images.githubusercontent.com/73039194/133170617-dd78c1b3-ed63-4f0c-b57c-0eb7db1d8f15.png)
<br>

Dentro do seu arquivo app.js você vai criar um componente react básico (copie e cole no <b>app.js</b>): <br>

import React from 'react'

const App = () => (
    <div>
   Configurando o meu projeto com webpack 5 
    </div>
)

export default App

![image](https://user-images.githubusercontent.com/73039194/133171307-e53313cf-688f-456f-af93-454411edb277.png)

<br>
<br>
No index.js vamos utilizar o react-dom para montar nossa aplicação de uma div dentro do template.html que iremos criar ja ja (copiar e colar dentro do arquivo <b>index.js</b>)<br>
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
<br>
![image](https://user-images.githubusercontent.com/73039194/133171446-d2ac3846-fe50-4d7e-a519-7b7b9814f83d.png)

<br>

# ✍🏽 Configurando Webpack 5

Crie um arquivo <b> webpack.config.js</b> na raiz do seu projeto ele vai ser responsável por toda configuração do Webpack, depois iremos definir a entrada da seguinte forma:<br>
![image](https://user-images.githubusercontent.com/73039194/133171660-6f8020ea-f6db-4244-a10b-ae4d228e5877.png)
<br>
const path = require('path')

module.exports = {
  entry: {
    main: path.resolve(__dirname, "./src/index.js"),
    hot: 'webpack/hot/dev-server.js',
    client: 'webpack-dev-server/client/index.js?hot=true&live-reload=true',
  },
}

<br>
Agora a saida desta maneira <br>

  output: {
    path: path.resolve(__dirname, "./dist"),
    filename: "[name].bundle.js",
  },
  ![image](https://user-images.githubusercontent.com/73039194/133172141-89347c9f-016a-4cfc-8af4-e27d24cc482c.png)

<br>







