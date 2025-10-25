import pygame, sys

pygame.init()

# Configuración de ventana
ANCHO, ALTO = 800, 600
ventana = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Rectángulo con rastro y límites")

# Colores
BLANCO = (255,255,255)
ROJO = (255,0,0)
AZUL = (0,0,255)

# Rectángulo inicial
rect_x, rect_y = 400, 300
rect_ancho, rect_alto = 50, 30
vel = 5

# Lista para almacenar posiciones del rastro
rastro = []

while True:
    for e in pygame.event.get():
        if e.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Movimiento con teclado
    teclas = pygame.key.get_pressed()
    if teclas[pygame.K_LEFT]:
        rect_x -= vel
    if teclas[pygame.K_RIGHT]:
        rect_x += vel
    if teclas[pygame.K_UP]:
        rect_y -= vel
    if teclas[pygame.K_DOWN]:
        rect_y += vel

    # Limitar posición dentro de la ventana
    if rect_x < 0: rect_x = 0
    if rect_x + rect_ancho > ANCHO: rect_x = ANCHO - rect_ancho
    if rect_y < 0: rect_y = 0
    if rect_y + rect_alto > ALTO: rect_y = ALTO - rect_alto

    # Guardar posición actual en el rastro (centro del rectángulo)
    rastro.append((rect_x + rect_ancho//2, rect_y + rect_alto//2))

    # Dibujar
    ventana.fill(BLANCO)

    # Dibujar rastro
    for pos in rastro:
        pygame.draw.circle(ventana, AZUL, pos, 5)

    # Dibujar rectángulo
    pygame.draw.rect(ventana, ROJO, (rect_x, rect_y, rect_ancho, rect_alto))

    pygame.display.update()
