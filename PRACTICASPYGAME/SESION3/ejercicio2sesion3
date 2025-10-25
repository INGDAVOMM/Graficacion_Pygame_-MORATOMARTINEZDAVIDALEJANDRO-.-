import pygame, sys, math

pygame.init()

# Configuración de ventana
ANCHO, ALTO = 800, 600
ventana = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Movimiento circular automático")

# Colores
BLANCO = (255,255,255)
ROJO = (255,0,0)

# Centro de la trayectoria
centro_x, centro_y = 400, 300
radio = 150  # Radio de la trayectoria circular
angulo = 0   # Ángulo inicial
vel_angular = 0.02  # Velocidad de giro (radianes por frame)

# Tamaño del rectángulo
rect_ancho, rect_alto = 50, 30

while True:
    for e in pygame.event.get():
        if e.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Calcular posición circular
    rect_x = centro_x + radio * math.cos(angulo) - rect_ancho/2
    rect_y = centro_y + radio * math.sin(angulo) - rect_alto/2

    # Incrementar ángulo para movimiento
    angulo += vel_angular

    # Dibujar
    ventana.fill(BLANCO)
    pygame.draw.rect(ventana, ROJO, (rect_x, rect_y, rect_ancho, rect_alto))
    pygame.display.update()
