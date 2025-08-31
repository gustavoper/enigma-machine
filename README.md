# Enigma Machine Simulator

Este projeto é um simulador da máquina **Enigma**, desenvolvido em **JavaScript (Node.js)** e compatível com execução via **navegador**.

## 🚀 Funcionalidades

- Simulação de encriptação e decriptação (a Enigma aplica o mesmo processo para ambos).
- Configuração de rotores, refletores, ring settings e posições iniciais.
- Suporte a plugboard.
- Execução tanto no navegador quanto em ambiente Node.js.

---

## 📦 Pré-requisitos

- [Node.js](https://nodejs.org/) (>= 18.x recomendado)
- [Yarn](https://classic.yarnpkg.com/lang/en/) instalado globalmente

---

## 🔧 Instalação e execução local

Clone o repositório:

```bash
git clone https://github.com/gustavoper/enigma-machine.git
cd enigma-machine
```

Instale as dependências com Yarn:

```bash
yarn install
```

▶️ Uso no Node.js

Você pode importar a classe Enigma e usá-la diretamente em scripts Node.js:


```bash
const { Enigma } = require('./enigma');

const machine = new Enigma({
  rotors: ['I', 'II', 'III'],
  rings: [1, 1, 1],
  positions: ['A', 'A', 'A'],
  reflector: 'B',
  plugboard: 'AV BS CG DL FU HZ IN KM OW RX'
});

const cipher = machine.process('HELLO WORLD');
machine.resetPositions(['A', 'A', 'A']);
const plain = machine.process(cipher);

console.log({ cipher, plain });
```

Execute o script:

```bash
node index.js
```


🌐 Uso no navegador

Abra o arquivo index.html no seu navegador.

Configure rotores, refletores, posições e plugboard conforme desejar.

Digite um texto no campo Input e clique em Encrypt ou Decrypt.

O mesmo processo funciona para criptografar e descriptografar.

📜 Scripts disponíveis

yarn start → Abre o simulador no navegador (via live-server, se configurado).

yarn test → Executa testes unitários (caso implementados).

📖 Observações

A encriptação e decriptação são realizadas pelo mesmo processo: basta usar a mesma configuração de máquina.

Apenas caracteres do alfabeto são processados, outros podem ser ignorados ou mantidos (opção configurável no app).

🛠️ Próximos passos

Adicionar presets históricos (ex.: configuração Wehrmacht).

Salvar/compartilhar configuração via URL.

Exportação como ES Module (import { Enigma } from './enigma.js').

📜 Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para usar e modificar.