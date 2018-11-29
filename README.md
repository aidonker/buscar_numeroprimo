# buscar_numeroprimo
Buscar un numero primo en Python

"""
Buscar un numero primo, con un numero determinado ingresado por pantalla
"""
n = int(input("Ingrese hasta que numero quiere hallar los numeros primos: ")) #Ingreso del dato
contador = 0
if n > 0: #Comprueba si el numero ingresado sea ENTERO POSITIVO
    for i in range(2, n + 1): #Empieza i desde 2 hasta el numero ingresado
        creciente = 2 #Variable para dividir, y comprobar si es una division exacta
        esPrimo = True #Consideremos todos los numeros PRIMOS

        while esPrimo and creciente < i: #Mientras esPrimo es TRUE y creciente menor a i(El numero de del arreglo)
            if i % creciente == 0: #Si el modulo de i es igual a 0(Division exacta)
                esPrimo = False #esPrimo cambia a ser Falso
                #print(f"{i} no es un numero primo") Si desea mostrar el numero que NO es primo
            else:
                creciente += 1 #Creciente aumenta en 1, si el residuo es 0
        if esPrimo: #Si esPrimo es verdadero (True)
            print(f"{i} es numero primo") #Imprime todos los numeros primos
            contador += 1 #Cuenta cuantos numeros primos son
else:
    print("El numero ingresado no es correcto, porfavor ingrese nuevamente") #Imprime error, si el numero no es entero y no es positivo
    print(f"{contador}, numeros son primos menores a {n}.")
