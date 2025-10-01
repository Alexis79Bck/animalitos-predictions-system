# 🐾 Sistema de Predicción de Animalitos

Este proyecto es un **sistema modular de predicción de animalitos** cuyo propósito es realizar cálculos estadísticos, analíticos y probabilísticos para generar predicciones con altas probabilidades de ser sorteadas en los próximos juegos.

![PHP](https://img.shields.io/badge/PHP-8.2-blue?logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-11.x-red?logo=laravel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-yellow?logo=python&logoColor=white)
![License](https://img.shields.io/badge/license-Apache_2.0-green)
![Status](https://img.shields.io/badge/status-early%20development-orange)

---

## 📐 Arquitectura del Sistema

El sistema está dividido en componentes independientes para garantizar escalabilidad y mantenibilidad:

- **Frontend**
  - Tecnología libre (Vue, React, Angular o similar).
  - Función: consumir los endpoints del backend y mostrar las predicciones de forma interactiva.

- **Backend API (Laravel)**
  - Orquesta las solicitudes del frontend.
  - Gestiona la lógica de negocio y expone endpoints REST.

- **Data Pipeline (Python)**
  - Obtiene y procesa resultados históricos de sorteos.
  - Implementa los cálculos estadísticos y probabilísticos.
  - Consumido por la API en Laravel.

- **Base de Datos**
  - **MySQL** en la versión BETA.
  - **PostgreSQL** en la versión FINAL (más robusto y escalable).

---

## 🚀 Requisitos previos

Asegúrate de tener instalado:

- PHP **8.2+**, Composer y Laravel  
- Python **3.11+**  
- MySQL o PostgreSQL (dependiendo de la versión)  
- Node.js **18+** (si se implementa frontend SPA)  
- (Opcional) Docker & Docker Compose  

---

## ⚙️ Instalación y Configuración

### 1. Clonar repositorio

```bash
git clone https://github.com/Alexis79Bck/animalitos-predictions-system.git
cd animalitos-predictions-system
```

### 2. Api Backend

```bash
cd backend-api
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
php artisan serve
```

### 3. Data Pipeline

```bash
cd ../data-pipeline
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
pip install -r requirements.txt
```

### 4. Conexiones

Configura las credenciales de tu base de datos en los archivos *.env* correspondientes.

---
## 🤝 Contribuciones

¡Tus aportes son bienvenidos!
1. Haz un fork del repositorio.
2. Crea una rama:

```bash
git checkout -b feature/nueva-funcionalidad
```

3. Aplica tus cambios respetando estándares (PSR-12 para PHP, PEP-8 para Python).
4. Haz commit siguiendo Conventional Commits
5. Sube tu rama:

```bash
git push origin feature/nueva-funcionalidad
```

6. Abre un Pull Request.

### Checklis antes PR

* [ ] Tests ejecutados y pasados.
* [ ] Documentación actualizada.
* [ ] Código formateado según convenciones.
---

## 🛣️ Roadmap (sugerencia inicial y puede ser modificado segun la evolucion del proyecto)

- [X] Data Pipeline en Python
- [X] API básica en Laravel
- [ ] Data Processing Calculating en Python
- [ ] Integración inicial con frontend
- [ ] Migración a PostgreSQL
- [ ] Implementación de métricas de precisión
- [ ] Testing de funcionalidades e integración
- [ ] Dashboard UI de estadísticas
---

## Licencia

Este módulo está licenciado bajo la Licencia Apache 2.0. Consulta el archivo `LICENSE` en la raíz del repositorio para más detalles.
