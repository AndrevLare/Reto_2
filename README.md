# Reto_2
```mermaid
classDiagram
    class Carta {
        +String palo
        +String valor
    }

    class Baraja {
        +List~Carta~ cartas
        +mezclar()
        +repartirCarta(): Carta
    }

    class Jugador {
        +String nombre
        +List~Carta~ mano
        +apostar(cantidad)
        +retirarse()
        +mostrarMano()
    }

    class Mesa {
        +List~Jugador~ jugadores
        +List~Carta~ cartasComunitarias
        +repartirCartas()
        +mostrarMesa()
    }

    class Juego {
        +Mesa mesa
        +Baraja baraja
        +iniciarJuego()
        +siguienteRonda()
        +determinarGanador()
    }

    Carta --> Baraja : "Usada en"
    Jugador --> Mesa : "Se sienta en"
    Mesa --> Juego : "Es parte de"
    Jugador --> Juego : "Participa en"
    Baraja --> Juego : "Usada en"
