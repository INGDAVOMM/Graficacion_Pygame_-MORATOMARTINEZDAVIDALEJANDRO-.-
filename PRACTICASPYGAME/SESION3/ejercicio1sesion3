import pygame, sys, random

pygame.init()

# Configuración de ventana
ANCHO, ALTO = 800, 600
ventana = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Cambio de color al tocar borde")

# Colores
BLANCO = (255,255,255)
colores = [
    (255,0,0),    # rojo
    (0,0,255),    # azul
    (0,255,0),    # verde
    (255,255,0),  # amarillo
    (255,0,255),  # rosa/magenta
    (128,0,128)   # morado
]

# Rectángulo inicial
rect_x, rect_y = 300, 200
rect_ancho, rect_alto = 100, 50
color_rect = random.choice(colores)

# Velocidad
vel = 5

# Flags para detectar toque en los bordes
tocando_izq = tocando_der = tocando_arriba = tocando_abajo = False

while True:
    for e in pygame.event.get():
        if e.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Movimiento con teclas
    teclas = pygame.key.get_pressed()
    if teclas[pygame.K_LEFT]:
        rect_x -= vel
    if teclas[pygame.K_RIGHT]:
        rect_x += vel
    if teclas[pygame.K_UP]:
        rect_y -= vel
    if teclas[pygame.K_DOWN]:
        rect_y += vel

    # Detectar y limitar bordes
    if rect_x < 0:
        rect_x = 0
        if not tocando_izq:  # Cambiar color solo la primera vez
            color_rect = random.choice(colores)
            tocando_izq = True
    else:
        tocando_izq = False

    if rect_x + rect_ancho > ANCHO:
        rect_x = ANCHO - rect_ancho
        if not tocando_der:
            color_rect = random.choice(colores)
            tocando_der = True
    else:
        tocando_der = False

    if rect_y < 0:
        rect_y = 0
        if not tocando_arriba:
            color_rect = random.choice(colores)
            tocando_arriba = True
    else:
        tocando_arriba = False

    if rect_y + rect_alto > ALTO:
        rect_y = ALTO - rect_alto
        if not tocando_abajo:
            color_rect = random.choice(colores)
            tocando_abajo = True
    else:
        tocando_abajo = False

    # Dibujar
    ventana.fill(BLANCO)
    pygame.draw.rect(ventana, color_rect, (rect_x, rect_y, rect_ancho, rect_alto))
    pygame.display.update()
