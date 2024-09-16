# TEMPERTURAS-2
# TEMPERARTURAS
"TEMPERATURAS DE LAS CIUDADES"
#Registro de Temperaturas Diarias
#Ejemplo de anidado
#javier mejia

import numpy as np

# Definir las dimensiones de la matriz
ciudades = ['QUITO', 'GUAYAQUIL', 'CUENCA']
dias = ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo']
semanas = ['PRIMER Semana', 'SEGUNDA Semana', 'TERCERA Semana', 'CUARTA Semana']

# Crear la matriz 3D con valores aleatorios de temperatura
temperaturas = np.random.rand(len(ciudades), len(dias), len(semanas))

# Calcular el promedio de temperaturas para cada ciudad y semana
for i, ciudad in enumerate(ciudades):
    for j, semana in enumerate(semanas):
        promedio = np.mean(temperaturas[i, :, j])
        print(f'Promedio de temperatura para {ciudad} en {semana}: {promedio:.2f}°C')
