\# Decisiones de Workflow - scv-empresarial



\## ¿Cuándo usamos rebase en este proyecto?

Usamos rebase cuando queremos limpiar el historial antes de publicar cambios en el repositorio. En especial, aplicamos `git rebase -i` para unir commits relacionados (squash), mejorar mensajes poco claros (reword) y eliminar commits innecesarios. Esto nos permite mantener un historial más legible, lineal y fácil de revisar.



\## ¿Cuándo usamos merge en este proyecto?

Utilizamos merge cuando queremos integrar una rama completa a `main` y conservar el contexto de desarrollo. Esto es útil cuando una funcionalidad ya está terminada y queremos dejar registro de cuándo y cómo se unió al proyecto principal. El merge es más seguro en ramas compartidas porque no reescribe el historial.



\## ¿Cuándo usamos cherry-pick?

Usamos cherry-pick cuando necesitamos aplicar un cambio específico sin traer todos los commits de una rama. Por ejemplo, en la Fase 2 se usó `git cherry-pick -x` para llevar a `main` solo el commit que estaba listo para producción, evitando incluir cambios experimentales. Esto es muy útil para hotfixes o correcciones urgentes.



\## Lecciones aprendidas en la Fase 2

Durante esta fase aprendimos que un historial limpio facilita el mantenimiento del proyecto y el code review. También entendimos que el rebase es una herramienta poderosa, pero peligrosa si se usa en ramas compartidas. Finalmente, aprendimos que el reflog es una herramienta clave para recuperar estados anteriores y que cherry-pick permite un control preciso de qué cambios llegan a producción.



