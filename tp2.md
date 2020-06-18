# Sujet 1 : Ecrire de l'assembleur

## Exercices

### Exo 1

```assembler
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

```assembler

```
