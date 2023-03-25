As fórmulas essenciais do Core são pacotes disponíveis no gerenciador de pacotes Homebrew que permitem a instalação de diversos softwares e ferramentas. Para instalar essas fórmulas, basta executar o comando brew install <fórmula> no terminal. É importante destacar que o Homebrew Core é o repositório padrão do Homebrew e já vem instalado por padrão, tanto para macOS quanto para Linux.

Para mais informações sobre o Homebrew, como documentação, solução de problemas, contribuições, segurança, comunidade, doações, licença e patrocinadores, é possível consultar as seções correspondentes no arquivo README do Homebrew/brew. Além disso, é possível encontrar uma lista completa de todas as fórmulas disponíveis na página do Homebrew Formulae. Caso seja necessário obter informações mais detalhadas sobre uma fórmula específica, é possível utilizar a API do Homebrew, que permite listar metadados e eventos de analytics.

Algumas das principais informações que podem ser obtidas através da API do Homebrew incluem:

Listagem de todas as fórmulas disponíveis no Homebrew Core ou no Homebrew Cask
Metadados de uma fórmula específica, incluindo informações sobre a versão atual, dependências e analytics
Eventos de analytics para uma categoria específica de fórmulas, agrupados por nome de fórmula ou token de Cask
Para acessar essas informações, é necessário realizar requisições HTTP GET para os endpoints correspondentes na API do Homebrew. Por exemplo, para listar todas as fórmulas disponíveis no Homebrew Core, é possível utilizar o endpoint https://formulae.brew.sh/api/formula.json. Já para obter os metadados de uma fórmula específica, é necessário utilizar o endpoint https://formulae.brew.sh/api/formula/\${FORMULA}.json, substituindo \${FORMULA} pelo nome da fórmula desejada.
