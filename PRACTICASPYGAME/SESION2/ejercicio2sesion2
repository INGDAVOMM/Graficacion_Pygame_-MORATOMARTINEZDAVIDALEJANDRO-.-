import pygame, sys

# Inicializar Pygame
pygame.init()

# Configurar ventana
ANCHO = ALTO = 400
ventana = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Círculos concéntricos")

# Colores para los círculos
colores = [(255,0,0), (0,255,0), (0,0,255), (255,255,0), (255,0,255)]

# Centro de los círculos
centro = (ANCHO//2, ALTO//2)

# Radios
radios = [20, 40, 60, 80, 100]

while True:
    for e in pygame.event.get():
        if e.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Fondo blanco
    ventana.fill((255,255,255))

    # Dibujar círculos
    for color, radio in zip(colores, radios):
        pygame.draw.circle(ventana, color, centro, radio, 2)  # 2 píxeles de grosor

    pygame.display.update()
