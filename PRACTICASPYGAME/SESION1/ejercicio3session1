import pygame
import sys

pygame.init()

# Contador de frames
frame = 0

# Crear reloj para controlar FPS
reloj = pygame.time.Clock()

# Configura la velocidad deseada (frames por segundo)
FPS = 100  # Por ejemplo, 10 frames por segundo

while True:
    frame += 1
    print(f"Frame: {frame}")

    # Detener después de 300 frames
    if frame >= 300:
        pygame.quit()
        sys.exit()

    # Controlar la velocidad del bucle
    reloj.tick(FPS)
