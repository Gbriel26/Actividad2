#Documentacion de la aplicación Flask para obtener la lista de personas 
Este script Python utiliza el framework Flask para crear una API que devuelve la lista de personas cuando se realiza una solicitud GET a la URL '/personas'.
Requisitos de importaciónSe importan las siguientes clases y objetos:from flask import Flask, jsonify  
from bd. personas import personas
Definición de la aplicación Flask y la rutaSe crea una instancia de la clase Flask y se define una ruta para la URL '/personas' que solo responde a solicitudes 
GET.app = Flask(_name_)  
@app.route('/personas', methods=['GET'])
Función para obtener la lista de personasSe define una función llamada get_personas() para manejar las solicitudes GET a la ruta '/personas'. Esta función devuelve un objeto JSON que contiene la lista de personas.
def get_personas():
    """
    Función para obtener la lista de personas.
    Devuelve un objeto JSON que contiene la lista de personas.
    """
    return jsonify({"personas": personas})Ejecución de la aplicaciónSe verifica si el script está siendo ejecutado directamente y se inicia la aplicación Flask en modo de depuración en el puerto 4000.if _name_ == "_main_": 
    app.run(debug=True, port=3000)Lista de personas
    solo de la APICuando se hace una solicitud GET a la URL '/personas', la API devuelve un objeto JSON que contiene la lista de personas con sus respectivos nombres, edades y ciudades.

