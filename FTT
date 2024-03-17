from flask import Flask, request, jsonify
from your_module import GerenciadorPersonagens

app = Flask(__name__)
gerenciador = GerenciadorPersonagens()

@app.route('/characters/', methods=['POST'])
def criar_personagem():
    data = request.get_json()
    if not data:
        return jsonify({'error': 'No data provided'}), 400
    
    nome = data.get('Mini Keanu Reeves')
    descricao = data.get('O Mini Keanu Reeves e igual ao original mas engraçado')
    link_imagem = data.get('https://www.google.com/url?sa=i&url=https%3A%2F%2Fstayhipp.com%2Finternet%2Fmemes%2Fmini-keanu-reeves-memes-are-everything%2F&psig=AOvVaw3PEd4OTFqlbPArjIe9rxOi&ust=1710472236156000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCNC12-Hj8oQDFQAAAAAdAAAAABAR')
    programa = data.get('O Keanu Reeves')
    animador = data.get('Filmes como Matrix, Jhon Wick, Constantine entre outros')

    if not nome or not descricao or not link_imagem:
        return jsonify({'error': 'Mini Keanu Reeves, O Mini Keanu Reeves e igual ao original mas engraçado e https://www.google.com/url?sa=i&url=https%3A%2F%2Fstayhipp.com%2Finternet%2Fmemes%2Fmini-keanu-reeves-memes-are-everything%2F&psig=AOvVaw3PEd4OTFqlbPArjIe9rxOi&ust=1710472236156000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCNC12-Hj8oQDFQAAAAAdAAAAABAR'}), 400

    personagem = gerenciador.criar_personagem(nome, descricao, link_imagem, programa, animador)
    return jsonify({'message': 'Personagem criado com sucesso', 'personagem': str(personagem)}), 201

@app.route('/characters/', methods=['GET'])
def visualizar_personagens():
    personagens = gerenciador.visualizar_personagens()
    return jsonify({'personagens': personagens})

if __name__ == '__main__':
    app.run(debug=True)
