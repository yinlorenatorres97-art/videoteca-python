# #Matriz [titulo, año de lanzamiento, calificacion (1-10), genero]

videoteca =[
    ["Avatar",2009,7,"ciencia ficcion"],
    ["Vengadores:endgame",2019,8,"accion"],
    ["El rey Leon",1994,6,"animacion"],
    ["Titanic",1997,9,"drama"],
    ["Jurassic Word",2015,7,"aventura"],
    ["Interstellar",2014,8,"ciencia ficcion"],
    ["Rapidos y furiosos 7",2015,6,"accion"]
]

def contar_titulos(matriz,calificacion_minima,año_limite):
    contador = 0
    for titulo in matriz:
        año = titulo[1]
        calificacion = titulo[2]
        
        if calificacion >= calificacion_minima and año >= año_limite:
            contador += 1
    return contador

calificacion_minima = 6
año_limite = 2005

resultado = contar_titulos(videoteca,calificacion_minima,año_limite)

print(f"Conteo total de titulos que cumplen con ambos criterios: {resultado}")
