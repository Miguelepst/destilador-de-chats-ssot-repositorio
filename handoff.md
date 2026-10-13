# HANDOFF — Destilador de chats ssot

> Archivo de traspaso entre chats desechables. Se lee al INICIO de cada chat y se actualiza al CIERRE.
> Fuente de verdad (SSOT): el repositorio público en GitHub. Este archivo es el puente, no el archivo final.

## 0. Metadatos

- Repo: `<PENDIENTE: URL del repo público>`
- Rama de trabajo: `main`
- Ruta raw de este archivo: `<PENDIENTE: https://raw.githubusercontent.com/<usuario>/<repo>/main/handoff.md>`
- Nombre canónico del archivo: `handoff.md` (minúscula; la URL raw distingue mayúsculas)
- Última actualización: 2026-10-13
- Versión del handoff: 0.2 (convención de commits registrada)

## 1. Propósito del proyecto

Destilar el contenido valioso de chats cortos y desechables hacia un documento persistente (SSOT) alojado en GitHub. Los chats se borran sin pérdida; todo lo que importa vive en el repo.

## 2. Estado actual

- [x] Proyecto creado en Claude
- [x] Handoff.md inicial
- [x] Convención de mensajes de commit definida (sección 8)
- [ ] Repo en GitHub enlazado y verificado
- [ ] Los 3 moldes de archivo entregados y revisados
- [ ] Los "modes" entregados y revisados
- [ ] Primer documento persistente generado

## 3. Ciclo de vida de un chat (resumen)

1. **Abrir**: leer `handoff.md` (raw) → confirmar objetivo del chat en una línea.
2. **Trabajar**: un solo objetivo por chat; los logros se anotan al vuelo en la sección 6.
3. **Destilar**: antes de cerrar, convertir los logros en entradas formales para el archivo persistente.
4. **Cerrar**: actualizar `handoff.md` (estado, pendientes, siguiente paso) y hacer commit al repo con el mensaje según la sección 8.
5. **Desechar**: borrar el chat solo cuando el commit esté confirmado.

## 4. Decisiones tomadas

| Fecha | Decisión | Motivo |
|---|---|---|
| 2026-10-12 | Repo público en GitHub como SSOT | Acceso raw sin autenticación para Claude |
| 2026-10-12 | Chats cortos y desechables | Evitar contexto contaminado; todo lo valioso se persiste |
| 2026-10-13 | Mensajes de commit largos con formato fijo (sección 8) | Historial legible y registro persistente de las decisiones de base |
| 2026-10-13 | Nombre canónico `handoff.md` en minúscula | La ruta raw de GitHub distingue mayúsculas; evita enlaces rotos |

## 5. Pendientes / bloqueos

- Falta URL del repo para verificar alineación handoff ↔ repo.
- Faltan los 3 moldes de archivo (el registro persistente usa formato temporal hasta entonces).
- Faltan los modes para revisión.

## 6. Registro temporal de logros (pendiente de migrar a los moldes definitivos)

Formato por entrada:

```
### [AAAA-MM-DD] Título corto del logro
- Chat: <nombre o tema del chat>
- Qué se logró: ...
- Evidencia / archivo afectado: ...
- Estado: borrador | confirmado | commiteado
- Siguiente paso: ...
```

### [2026-10-12] Arranque del proyecto
- Chat: Configuración inicial
- Qué se logró: definición de descripción, instrucciones del proyecto y handoff base.
- Evidencia / archivo afectado: `handoff.md`
- Estado: borrador
- Siguiente paso: entregar URL del repo, los 3 moldes y los modes.

### [2026-10-13] Convención de mensajes de commit
- Chat: Convención de commits
- Qué se logró: se definió y registró el formato de commits largos (sección 8) y se fijó `handoff.md` como nombre canónico.
- Evidencia / archivo afectado: `handoff.md`
- Estado: borrador
- Siguiente paso: hacer el commit con el mensaje propuesto y confirmarlo para pasar a `commiteado`.

## 7. Siguiente paso recomendado

Entregar la URL del repo para verificar el handoff contra el contenido raw y luego los 3 moldes.

## 8. Convención de mensajes de commit

Todos los commits usan mensaje largo (encabezado + cuerpo + pie), en español.

**Estructura**

```
<emoji> <tipo>(<alcance>): <resumen en infinitivo>

<Una frase de contexto: qué se crea o cambia y para qué.>

* <Cambio 1, en infinitivo.>
* <Cambio 2.>

Refs: <archivo1>, <archivo2>
```

**Reglas**

1. Encabezado de máximo 72 caracteres, verbo en infinitivo (registrar, definir, añadir, corregir), sin punto final.
2. `<alcance>` es el archivo o área afectada en minúscula (`handoff`, `moldes`, `modes`, `registro`).
3. Una línea en blanco entre encabezado, cuerpo y pie.
4. El cuerpo abre con una frase de contexto y sigue con viñetas `*`, cada una describe un cambio concreto.
5. El pie `Refs:` lista los archivos tocados con su nombre real (respetando mayúsculas/minúsculas).
6. Un commit por cierre de chat; el commit debe incluir el `handoff.md` actualizado.

**Emojis y tipos**

| Emoji | Tipo | Uso |
|---|---|---|
| 📝 | docs | Documentación y handoff |
| ✨ | feat | Nuevo molde, mode o documento persistente |
| 🐛 | fix | Corrección de errores o contradicciones |
| ♻️ | refactor | Reorganizar sin cambiar el contenido |
| 🔧 | chore | Configuración y mantenimiento del repo |

**Ejemplo (commit inicial del proyecto)**

```
📝 docs(handoff): registrar documento inicial del proyecto

Crear la primera versión de `handoff.md` como documento de traspaso entre chats desechables.

* Definir el repositorio persistente como fuente única de verdad (SSOT).
* Establecer el uso del handoff al inicio y al cierre de cada chat.
* Documentar el propósito de destilar información valiosa de los chats hacia el repositorio.
* Registrar el estado inicial del proyecto y los metadatos pendientes de completar.
* Identificar la versión 0.1 como borrador inicial.

Refs: handoff.md
```
