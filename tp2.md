# Sujet 1 : Ecrire de l'assembleur

## Exercices

### Exo 1

En utilisant uniquement des OR, AND, NOT, créer un code qui permet de réaliser un XOR.

```assembly
org 100h

mov  al,206
mov  bl,178

not bl
and bl,al
not al
or bl,al

mov cx, 8
print: mov ah, 2
       mov dl, '0'
       test bl, 10000000b
       jz zero
       mov dl, '1'

zero:  int 21h
       shl bl, 1
loop print

mov dl, 'b'
int 21h

mov ah, 0
int 16h

ret
```

### Exo 2

En utilisant uniquement le opérations logiques OR, AND, NOT et XOR, créer un additionneur.

```assembly

```

### Exo 3

Créer un programme qui affiche dans la sortie standard une chaîne de caractère définie dans le code.

```assembly
org 100h

jmp start

msg:    db      "Hello, World!", 0Dh,0Ah, 24h

start:  mov     dx, msg
        mov     ah, 09h
        int     21h

        mov     ah, 0

ret
```

### Exo 4

Créer une boucle qui calcule et affiche les chiffres de 1 à 10.

```assembly
org 100h

mov  al,1
mov  bl,1

add al, bl

mov cx, 8
print: mov ah, 2
       mov dl, '0'
       test bl, 10
       jz zero
       mov dl, '1'

zero:  int 21h
       shl bl, 1
loop print

mov dl, 'b'
int 21h

mov ah, 0
int 16h

ret
```
