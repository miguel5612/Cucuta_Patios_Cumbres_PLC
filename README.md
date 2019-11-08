# Cucuta_Patios_Cumbres_PLC
Este tablero tiene por objetivo alternar dos motobombas, permitir su control manual/automatico.
# Diagrama de bloques
https://www.lucidchart.com/invitations/accept/70223c3f-a606-4776-b00d-ef4ae56e7da2
# Pines de conexionado
| Entrada | Definicion |
| ----- | ---- |
| I1 | Auto |
| I2 | Manual |
| I3 | Bomba 1 |
| I4 | Bomba 2 |

# Pines de Salida
| Salida | Definicion |
| ----- | ---- |
| Q1 | Activa el VFD |
| Q2 | Contactor 1 (Bomba 1) |
| Q3 | Contactor 2 (Bomba 2) |
| Q4 | Luz Naranja de Presion baja (M20) |
# Definicion del programa
* Version Base [Cerro Pastel](https://github.com/miguel5612/Cucuta_Cerro_Pastel_Control_Acueducto)
## Programa
* Validacion de presion:
Si hay presion esta activo M20 
Cada vez que hay presion, corre el timer de 5 minutos por M21
## Modo Auto
Si *Modo = Manual (I1)* y *Modo != Auto(I2)* Entonces M1 (Marca)
