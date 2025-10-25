import pygame
import sys

# Inicializar Pygame
pygame.init()

# Configuración de la ventana
ANCHO = 800
ALTO = 600
ventana = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Cambio de color con tecla C")

# Lista de colores (RGB)
colores = [
    (255, 255, 255),  # Blanco
    (0, 0, 255),      # Azul
    (255, 0, 0),      # Rojo
    (0, 255, 0),      # Verde
    (255, 255, 0),    # Amarillo
    (255, 0, 255),    # Magenta
    (0, 255, 255),    # Cyan
    (128, 0, 128),    # Púrpura
    (255, 165, 0),    # Naranja
    (0, 128, 128)     # Verde azulado
]

indice_color = 0  # Color inicial

# Bucle principal
while True:
    for evento in pygame.event.get():
        # Cerrar la ventana
        if evento.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
        
        # Cambiar color al presionar la tecla C
        if evento.type == pygame.KEYDOWN:
            if evento.key == pygame.K_c:
                indice_color += 1
                if indice_color >= len(colores):
                    indice_color = 0  # Volver al primer color

    # Pintar la ventana con el color actual
    ventana.fill(colores[indice_color])

    # Actualizar pantalla
    pygame.display.update()
