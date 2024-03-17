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
