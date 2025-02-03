# TrabajoListas

#Trabajo Programación Febrero 3

#-------------------------------------------------------
#Ejercicio 1: Lista con elementos no repetidos
#-------------------------------------------------------

def elementos(lista):
    return len(lista) == len(set(lista))

ejemplolista = [1,2,3,4,5,6]
if elementos(ejemplolista):
    print("En la lista no hay elementos repetidos")
else:
    print("En la lista hay elementos repetidos")

#-------------------------------------------------------
#Ejercicio 2: Determinar si un elemento de una lista es una cadena palíndrome 
#-------------------------------------------------------

def palindrome(p):
   return p == p[::-1]

def encontrar_palindrome(strings):
    for p in strings:
        if palindrome(p):
            return p
    return "No existe"

lista = ["hola", "oso", "mundo"]
print(encontrar_palindrome(lista))

#-------------------------------------------------------
#Ejercicio 3: Cadena de caracteres con dos o más vocales
#-------------------------------------------------------

def vocales(v):
    vocal = {'a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U'}
    conteo = sum(1 for char in v if char in vocal)
    return conteo >= 2

def encontrar_vocales(strings):
    encontrado = False  
    for v in strings:
        if vocales(v):
            print(v)
            encontrado = True  
    
    if not encontrado:
        print("No existe")

lista = ["gato", "zxcvb", "hola", "xyz"]
encontrar_vocales(lista)


#-------------------------------------------------------
#Ejercicio 4: Determinar si una lista es palíndrome 
#-------------------------------------------------------

def palindrome(pal):
    return pal == pal[::-1]

lista = ["aerea"]
if palindrome(lista):
    print("La cadena es palíndrome")
else:
    print("La cadena no es palíndrome")

#-------------------------------------------------------
#Ejercicio 5: Cadena de caracteres con dos o más MAYÚSCULAS
#-------------------------------------------------------

def buscar_mayusculas(lista):
    encontrado = False  
    for cadena in lista:
        mayusculas = sum(1 for m in cadena if m.isupper())
        
        if mayusculas >= 2:
            print(cadena)
            encontrado = True
    
    if not encontrado:
        print("No existe")

lista = ["hola", "Hola Mundo", "abcDEF", "uNaL", "ejemplo", ""]
buscar_mayusculas(lista)

#-------------------------------------------------------
#Ejercicio 6: Cadena de caracteres con dos o más consonantes
#-------------------------------------------------------

def buscar_numeros(lista):
    encontrado = False  
    for cadena in lista:
        numeros = sum(1 for n in cadena if n.isdigit())

        if numeros >= 2:
            print(cadena)
            encontrado = True 
    
    if not encontrado:
        print("No existe")

lista = ["abc123", "numeros", "abc12", "prueba345", "abc1", "12345"]
buscar_numeros(lista)

#-------------------------------------------------------
#Ejericicio 7: Determina la cantidad de palíndromos existentes en una cadena
#-------------------------------------------------------

def es_palindromo(cadena):
    cadena = cadena.lower()
    
    return cadena == cadena[::-1]

def encontrar_palindromos(lista):
    palindromos = []
    for s in lista:
        if es_palindromo(s):
            palindromos.append(s)  
    
    if palindromos:
        for pal in palindromos:
            print(pal)  
        print(f"Total de palíndromos encontrados: {len(palindromos)}")
    else:
        print("No existe")

lista = ["madam", "hello", "racecar", "abcba", "world"]
encontrar_palindromos(lista)

#-------------------------------------------------------
#Ejericicio 8: Determina si una cadena cuenta con más de 5 caracteres
#-------------------------------------------------------

def palabra_larga(cadena):
    palabras = cadena.split()
    for palabra in palabras:
        if len(palabra) > 5:
            return True
    return False

def encontrar_palabras(lista):
    encontrado = False
    for s in lista:
        if palabra_larga(s):
            print(s)  
            encontrado = True
    
    if not encontrado:
        print("No existen cadenas con palabras de más de 5 caracteres")

lista = ["Hola Mundo", "Universidad Nacional", "Julian Santana", "abc def"]
encontrar_palabras(lista)
