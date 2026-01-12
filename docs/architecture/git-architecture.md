# Arquitectura de Git — Sistema de Control de Versiones Empresarial

## 1. Estructura del Repositorio

Este repositorio sigue una estructura modular y escalable para facilitar el mantenimiento, la colaboración y la extensibilidad del proyecto.

scv-empresarial/
├── src/
│ ├── components/ # Componentes reutilizables
│ ├── utils/ # Funciones auxiliares
│ └── services/ # Lógica de negocio y servicios
├── tests/
│ ├── unit/ # Pruebas unitarias
│ └── integration/ # Pruebas de integración
├── docs/
│ ├── architecture/ # Documentación de arquitectura
│ └── guides/ # Guías de uso y desarrollo
├── .gitignore
└── README.md


Esta estructura permite un crecimiento ordenado del proyecto y una separación clara de responsabilidades entre módulos.

---

## 2. Estrategia de Branching

El proyecto utiliza una estrategia de branching simple y eficiente.

### Rama principal: `main`

- Contiene únicamente código estable.
- Solo se integran cambios que han sido revisados y probados.
- Es la rama protegida del proyecto.

### Ramas de trabajo

Todas las nuevas funcionalidades, correcciones o tareas se desarrollan en ramas independientes:

| Tipo de Rama | Uso |
|--------------|-----|
| feature/*    | Nuevas funcionalidades |
| fix/*        | Corrección de errores |
| docs/*       | Documentación |
| chore/*      | Mantenimiento |

Ejemplos:
- `feature/login-system`
- `fix/auth-bug`
- `docs/api-guide`
- `chore/update-dependencies`

Estas ramas se integran a `main` mediante Pull Requests.

---

## 3. Política de Commits

Este proyecto sigue el estándar **Conventional Commits** para mantener un historial limpio, legible y automatizable.

### Formato de commit

<tipo>(<scope opcional>): <descripción>

### Tipos utilizados

| Tipo     | Descripción |
|----------|------------|
| feat     | Nueva funcionalidad |
| fix      | Corrección de errores |
| docs     | Cambios en documentación |
| style    | Cambios de formato |
| refactor | Refactorización |
| test     | Pruebas |
| chore    | Tareas de mantenimiento |

### Ejemplos

- `feat(auth): add login system`
- `fix(api): correct token validation`
- `docs: update README`
- `chore: update dependencies`

---

## 4. Firma de Commits (GPG)

Todos los commits deben estar firmados con GPG.

Esto garantiza:

- Autenticidad del autor
- Integridad del historial
- No repudio de cambios

GitHub valida estas firmas y las muestra como **Verified**.

---

## 5. Flujo de Trabajo

1. Crear una rama desde `main`
2. Realizar cambios
3. Hacer commits firmados
4. Subir la rama al repositorio remoto
5. Crear un Pull Request
6. Revisar los cambios
7. Integrar a `main`

---

## 6. Seguridad y Buenas Prácticas

- Uso obligatorio de firmas GPG
- Historial descriptivo
- Separación de responsabilidades
- Documentación continua
- Control de accesos por roles

---

Documento mantenido por el equipo de desarrollo del proyecto **Sistema de Control de Versiones Empresarial (SCV)**.
