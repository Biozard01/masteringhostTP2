# Sujet 1 : Ecrire de l'assembleur

## Préliminaires

```
org 100h

mov  al,206
mov  bl,178

not bl
and bl,al
not al
or bl,al

; mov  ah,11001110b
; mov  al,10110010b
; xor  al,ah
; al = 01111100b 124

mov cx, 8
print: mov ah, 2   ; print function.
       mov dl, '0'
       test bl, 10000000b  ; test first bit.
       jz zero
       mov dl, '1'

zero:  int 21h
       shl bl, 1
loop print

; print binary suffix:
mov dl, 'b'
int 21h

; wait for any key press:
mov ah, 0
int 16h

ret
```
