# Laboratorio de Algoritmos Genéticos - Curso 1

**Universidad de Cundinamarca - Seccional Ubaté**
**Programa de Ingeniería de Sistemas y Computación**
**Docente:** Fabio Alejandro Sastoque Rincón

## Descripción

Este repositorio contiene la solución a la actividad *"Exploración y Optimización
Matemática"*, en la que se adapta un algoritmo genético base para resolver 4 ejercicios:

1. **Maximización cúbica** — maximizar $f(x) = x^3 - 4x^2 + 5x$ en el rango $[0, 1.9]$.
2. **Optimización multivariable** — minimizar $f(x,y) = x^2 + y^2$, cromosoma dividido en
   2 bloques de 4 bits (x, y).
3. **Impacto de la tasa de mutación** — comparación de `pm = 0.01, 0.1, 0.5`.
4. **Elitismo ampliado** — preservar los 3 mejores individuos (en lugar de solo 1) de una
   generación a la siguiente.

Todo el desarrollo está en `Actividad_Algoritmos_Geneticos.ipynb`.

## Requisitos

- Python 3.10+
- Extensión de Jupyter en el editor de código (VS Code u otro)
- Paquetes: `numpy`, `matplotlib`

## Configuración del entorno

```bash
# 1. Clonar el repositorio
git clone <url-del-repositorio>
cd <carpeta-del-repositorio>

# 2. Crear y activar entorno virtual
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# 3. Instalar dependencias
pip install numpy matplotlib jupyter
```

Recuerden agregar un archivo `.gitignore` con al menos:

```
venv/
env/
__pycache__/
.ipynb_checkpoints/
*.pyc
```

## Flujo de trabajo en Git (Branching)

1. Un integrante crea el repositorio en GitHub e invita a los demás como colaboradores.
2. A partir de `main`, cada integrante crea su propia rama, por ejemplo:
   ```bash
   git checkout -b feature/ejercicio1-maximizacion
   git checkout -b feature/ejercicio2-multivariable
   git checkout -b feature/ejercicio3-tasa-mutacion
   git checkout -b feature/ejercicio4-elitismo
   ```
3. Cada integrante trabaja y hace *commits* descriptivos en su rama:
   ```bash
   git add .
   git commit -m "Implementa fitness del Ejercicio 1 y ajusta rango de búsqueda"
   git push origin feature/ejercicio1-maximizacion
   ```
4. Al terminar, se abre un **Pull Request** hacia `main` desde GitHub para cada rama.
5. El equipo revisa y une (*merge*) los Pull Requests.
6. El entregable final es el **link del repositorio** con los Pull Requests correspondientes.

## Estructura del repositorio

```
├── README.md
├── .gitignore
└── Actividad_Algoritmos_Geneticos.ipynb
```

## Contenido del notebook

- **Funciones base:** codificación/decodificación binaria (soporta 1 o más variables),
  selección por torneo, cruce de un punto, mutación bit a bit y elitismo configurable.
- **Ejercicio 1 a 4:** cada uno reutiliza las funciones base, cambiando solo la función de
  aptitud y los parámetros pedidos en el enunciado, con sus respectivas gráficas de
  convergencia y conclusiones.




