# Ternary

Usando un diccionario:

    print({True: a, False: b} [a < b])

O una tupla:

    print( (b, a) [a < b] )

La manera mas eficiente es expresion lambda, dado que la expresion se evalua solo una vez, en vez de 2, como en caso de tupla o diccionario:

    
    print((lambda: b, lambda: a)[a < b]())
