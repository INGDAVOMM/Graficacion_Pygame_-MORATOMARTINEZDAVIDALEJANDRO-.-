import pygame
import sys

pygame.init()

ANCHO = 1000
ALTO = 800
ventana = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Mi primer programa gráfico")

COLOR_FONDO = (0, 255, 0)

while True:
    for evento in pygame.event.get():
        # 1. Cerrar al hacer clic en la "X" de la ventana
        if evento.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
        
        # 2. Cerrar al presionar la tecla ESCAPE
        if evento.type == pygame.KEYDOWN:
            if evento.key == pygame.K_ESCAPE:  # Tecla Esc
                pygame.quit()
                sys.exit()

    ventana.fill(COLOR_FONDO)

    pygame.display.update()
