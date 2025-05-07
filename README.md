# 📈 Proyecto de Regresión Lineal Simple - Advertising vs Sales


Implementación orientada a objetos de un modelo de regresión lineal simple para predecir ventas en función del gasto en publicidad.

## 📚 Tabla de Contenidos
- [Modelo Matemático](#-modelo-matemático)
- [Implementación](#-implementación)
- [Estructura del Código](#-estructura-del-código)
- [Instalación y Uso](#-instalación-y-uso)
- [Resultados y Visualización](#-resultados-y-visualización)
- [Ejemplo de Salida](#-ejemplo-de-salida)
- [Dependencias](#-dependencias)
- [Licencia](#-licencia)

## 🔢 Modelo Matemático

### Regresión Lineal Simple
El modelo establece una relación lineal entre la variable independiente (X = advertising) y la variable dependiente (Y = sales):

\[ Y = \beta_0 + \beta_1X + \epsilon \]

Donde:
- \( \beta_0 \): Intercepto (valor base de ventas sin publicidad)
- \( \beta_1 \): Pendiente (impacto de cada unidad de publicidad en ventas)
- \( \epsilon \): Término de error aleatorio

### Estimación por Mínimos Cuadrados
Los parámetros se calculan para minimizar la suma de errores al cuadrado:

\[ \beta_1 = \frac{\sum{(X_i - \bar{X})(Y_i - \bar{Y})}}{\sum{(X_i - \bar{X})^2}} \]

\[ \beta_0 = \bar{Y} - \beta_1\bar{X} \]

## 💻 Implementación

Características principales:
- ✅ Implementación desde cero (sin usar scikit-learn)
- 🧠 Enfoque orientado a objetos
- 📊 Visualización integrada
- 🔮 Capacidad predictiva

## 🏗️ Estructura del Código

### Diagrama de Clases
```mermaid
classDiagram
    class LinearRegression{
        +B_0 : float
        +B_1 : float
        +equation : str
        +fit(X, y) : None
        +predict(X_new) : ndarray
        +plot(X, y, X_new, y_pred) : None
        +get_equation() : str
    }
    
    class DataProcessor{
        +advertising : ndarray
        +sales : ndarray
        +get_data() : tuple
    }
