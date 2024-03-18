# DESAFIO 3
1.nome do arquivo:FTT

# API de Gerenciamento de Personagens

Esta é uma API simples para criar e visualizar personagens.

## Como usar

### Configuração

1. Certifique-se de ter o Python instalado em sua máquina.
2. Instale as dependências do projeto executando o seguinte comando:
3. pip install flask

### Executando a API

1. Clone este repositório em sua máquina.
2. Navegue até o diretório clonado.
3. Execute o seguinte comando para iniciar o servidor da API:
python app.py

### Endpoints

#### `POST /characters/`

Este endpoint é usado para criar um novo personagem.

- Parâmetros:
- `nome` (string, obrigatório): O nome do personagem.
- `descricao` (string, obrigatório): A descrição do personagem.
- `link_imagem` (string, obrigatório): O link da imagem do personagem.
- `programa` (string, opcional): O programa associado ao personagem.
- `animador` (string, opcional): O animador associado ao personagem.

Exemplo de requisição:
```json
{
"nome": "Mini Keanu Reeves",
"descricao": "O Mini Keanu Reeves é igual ao original mas engraçado",
"link_imagem": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fstayhipp.com%2Finternet%2Fmemes%2Fmini-keanu-reeves-memes-are-everything%2F&psig=AOvVaw3PEd4OTFqlbPArjIe9rxOi&ust=1710472236156000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCNC12-Hj8oQDFQAAAAAdAAAAABAR",
"programa": "O Keanu Reeves",
"animador": "Filmes como Matrix, Jhon Wick, Constantine entre outros"
}
GET /characters/
Este endpoint é usado para obter todos os personagens cadastrados.

Exemplo de resposta:
{
  "personagens": [
    {
      "nome": "Mini Keanu Reeves",
      "descricao": "O Mini Keanu Reeves é igual ao original mas engraçado",
      "link_imagem": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fstayhipp.com%2Finternet%2Fmemes%2Fmini-keanu-reeves-memes-are-everything%2F&psig=AOvVaw3PEd4OTFqlbPArjIe9rxOi&ust=1710472236156000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCNC12-Hj8oQDFQAAAAAdAAAAABAR",
      "programa": "O Keanu Reeves",
      "animador": "Filmes como Matrix, Jhon Wick, Constantine entre outros"
    }
  ]
}

# DESAFIO 4
# API de Gerenciamento de Personagens

Esta é uma API simples para criar, visualizar, atualizar e deletar personagens.

## Configuração

1. Certifique-se de ter o Python instalado em sua máquina.
2. Instale as dependências do projeto executando o seguinte comando:
pip install flask flask_sqlalchemy
## Executando a API

1. Clone este repositório em sua máquina.
2. Navegue até o diretório clonado.
3. Execute o seguinte comando para iniciar o servidor da API:
python app.py
## Endpoints

### Criar Personagem

Para criar um novo personagem, envie uma solicitação HTTP POST para o endpoint `/characters/` com os dados do personagem no corpo da solicitação no formato JSON.

Exemplo de solicitação:
```json
{
"nome": "Mini Keanu Reeves",
"descricao": "O Mini Keanu Reeves é igual ao original mas engraçado",
"link_imagem": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fstayhipp.com%2Finternet%2Fmemes%2Fmini-keanu-reeves-memes-are-everything%2F&psig=AOvVaw3PEd4OTFqlbPArjIe9rxOi&ust=1710472236156000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCNC12-Hj8oQDFQAAAAAdAAAAABAR",
"programa": "O Keanu Reeves",
"animador": "Filmes como Matrix, Jhon Wick, Constantine entre outros"
}
Visualizar Personagens
Para visualizar todos os personagens cadastrados, envie uma solicitação HTTP GET para o endpoint /characters/. Isso retornará uma lista de todos os personagens.

Para visualizar um personagem específico, envie uma solicitação HTTP GET para o endpoint /characters/<id>/, onde <id> é o ID do personagem desejado. Isso retornará os detalhes desse personagem.

Atualizar Personagem
Para atualizar um personagem existente, envie uma solicitação HTTP PUT para o endpoint /characters/<id>/, onde <id> é o ID do personagem que você deseja atualizar. Envie os dados atualizados do personagem no corpo da solicitação no formato JSON.
Exemplo de solicitação:
{
  "nome": "Novo Nome",
  "descricao": "Nova Descrição",
  "link_imagem": "https://example.com/nova-imagem.jpg",
  "programa": "Novo Programa",
  "animador": "Novo Animador"
}
Deletar Personagem
Para deletar um personagem existente, envie uma solicitação HTTP DELETE para o endpoint /characters/<id>/, onde <id> é o ID do personagem que você deseja excluir.

Contribuindo
Se você encontrar algum problema ou tiver sugestões de melhoria, sinta-se à vontade para abrir uma issue ou enviar um pull request.

Este é um exemplo básico de como usar a API de Gerenciamento de Personagens. Certifique-se de substituir os exemplos de URL e dados pelos valores reais ao interagir com a API.
Este README fornece instruções sobre como configurar e executar a API, além de explicar como usar cada endpoint para criar, visualizar, atualizar e deletar personagens. Ele também inclui exemplos de solicitações para cada operação.
