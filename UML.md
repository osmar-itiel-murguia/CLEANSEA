```mermaid
    usecase-beta
    direction LR
    actor Jugador
    actor Sistema

    systemBoundary recoleccion["Recolección"]
        Herramienta("Seleccionar herramienta o equipo")
        Recolectar("Recolectar basura")
        Clasificar("Clasificar basura")
        Inventario("Ver inventario")
        Descartar("Descartar basura sin valor")
    end

    systemBoundary economia["Economía"]
        Vender("Vender basura")
        Precios("Consultar precios de la basura")
        Comprar("Comprar mejoras")
        Catalogo("Ver catálogo de la tienda")
        Dinero("Consultar dinero")
    end

    systemBoundary progresion["Progresión y niveles"]
        Progreso("Ver porcentaje de limpieza")
        Avanzar("Avanzar de nivel")
        Verificar("Verificar porcentaje requerido")
        Regresar("Regresar a un nivel anterior")
        Seleccionar("Seleccionar nivel")
        Estadisticas("Ver estadísticas del cuerpo de agua")
    end

    systemBoundary partida["Sistema y partida"]
        Guardar("Guardar partida")
        Cargar("Cargar partida")
        Nuevo("Iniciar nuevo juego")
        Opciones("Configurar opciones (sonido, controles)")
        Tutorial("Ver tutorial")
    end

    Jugador -- Herramienta
    Jugador -- Recolectar
    Jugador -- Inventario
    Jugador -- Descartar
    Jugador -- Vender
    Jugador -- Precios
    Jugador -- Comprar
    Jugador -- Dinero
    Jugador -- Progreso
    Jugador -- Avanzar
    Jugador -- Regresar
    Jugador -- Seleccionar
    Jugador -- Estadisticas
    Jugador -- Guardar
    Jugador -- Cargar
    Jugador -- Nuevo
    Jugador -- Opciones
    Jugador -- Tutorial

    Sistema -- Progreso
    Sistema -- Verificar
    Sistema -- Avanzar
    Sistema -- Guardar

    Recolectar ..> : include Clasificar
    Descartar ..> : extend Inventario
    Comprar ..> : include Catalogo
    Avanzar ..> : include Verificar
    Comprar ..> : extend Vender
```

```mermaid


```
