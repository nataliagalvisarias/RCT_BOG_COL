# Prueba remota de la plataforma C4 — RCT VAC Bogotá 2026

Repositorio de prueba de la plataforma de clasificación de llamadas que se usará en el estudio *Who Answers the Call* (AEARCTR-0017873) con operadores de la Línea 123 del C4 Bogotá. Su único propósito es verificar, antes del experimento, que la plataforma funciona correctamente desde los equipos y la red del C4.

*English: test repository for the C4 Bogotá operator platform. The platform runs in the browser; no installation is needed. Contact details at the end.*

---

## Enlace para la prueba

**https://nataliagalvisarias.github.io/RCT_BOG_COL/**

No se instala nada y no se necesita cuenta de GitHub. Funciona en Chrome o Edge actualizados, con conexión a internet.

## Antes de empezar

**Use únicamente identificadores de prueba.** La plataforma asigna la condición experimental de forma permanente según el identificador que se escriba. Si un operador usa su identificador real durante la prueba, conocería de antemano su condición en el experimento.

| Para ver la versión **con** asistencia algorítmica | Para ver la versión **sin** asistencia algorítmica |
|---|---|
| `PRUEBA-01`, `PRUEBA-03`, `PRUEBA-05`, `PRUEBA-07` | `PRUEBA-02`, `PRUEBA-04`, `PRUEBA-06`, `PRUEBA-08` |

**Red institucional.** Si la página no carga las llamadas, solicite a Sistemas habilitar estos dominios:
`nataliagalvisarias.github.io` · `raw.githubusercontent.com` · `cdn.jsdelivr.net` · `www.gstatic.com` · `firestore.googleapis.com` · `fonts.googleapis.com`

## Pasos

1. **Abra el enlace** y haga clic en *Abrir la plataforma*.
2. **Consentimiento.** Lea el texto, marque la casilla y haga clic en *Continuar al sistema*.
3. **Configuración.** Complete todos los campos:
   - *ID Participante*: uno de la tabla anterior (por ejemplo `PRUEBA-01`);
   - *Género*, *Edad*, *Años de experiencia*, *Nivel de formación*, *Turno de trabajo*, *Tipo de empleado* y *Rol en C4*: valores ficticios.
4. **Cargue las llamadas** con *Cargar desde GitHub*. Debe aparecer **6000** en *Llamadas cargadas*.
5. Escriba **5** en *Llamadas a clasificar* para una prueba corta.
6. Haga clic en *Asignar condición*: debe coincidir con la columna de la tabla. Luego haga clic en *Iniciar experimento*.
7. **En cada llamada:**
   - lea la transcripción;
   - elija la *Circunstancia modificadora*;
   - elija la *Prioridad*: 1 alta, 2 media o 3 baja. También puede usar las teclas 1, 2 y 3;
   - si quiere, escriba *Anotaciones* (opcional);
   - haga clic en *Confirmar*.

   En la versión con asistencia, cuando el modelo detecta alto riesgo aparece la recomendación **Prioridad 1**, que se puede aceptar o no.
8. **Resultados.** Al terminar, la plataforma envía los resultados al servidor del estudio y muestra un mensaje de confirmación. Haga clic además en *Descargar CSV*.

Una prueba de 5 llamadas toma unos 10 minutos. Repítala con un identificador de cada columna.

## Qué reportar

Envíe a **natalia.galvisarias@postgrad.manchester.ac.uk**:

- [ ] el archivo CSV descargado de cada prueba;
- [ ] una captura de la pantalla final (mensaje de envío verde o rojo);
- [ ] el navegador usado (Chrome, Edge…) y si fue desde la red del C4;
- [ ] cualquier error, texto confuso o paso que no funcionó, con una captura si es posible.

## Problemas frecuentes

| Problema | Qué hacer |
|---|---|
| *Llamadas cargadas* queda en 0 | Recargue la página. Si continúa, la red bloquea alguno de los dominios de arriba: avise a Sistemas. |
| El botón *Iniciar experimento* no se activa | Falta un campo de configuración, el consentimiento o la carga de llamadas. |
| Mensaje rojo «No se pudo conectar al servidor» | La red bloquea `www.gstatic.com` o `firestore.googleapis.com`. Use *Descargar CSV* y envíe el archivo por correo. |
| La condición no coincide con la tabla | Revise que el ID esté escrito exactamente igual (mayúsculas y guion) y repórtelo. |
| La página se ve desordenada | Use la ventana maximizada en un computador; la plataforma no está diseñada para celular. |

## Contenido del repositorio

| Archivo | Para qué sirve |
|---|---|
| `index.html` | Página de inicio de la prueba (el enlace de arriba). |
| `C4_Bogota.html` | La plataforma de clasificación. |
| `RCT_calls.csv` | 6.000 llamadas archivadas **desidentificadas** que carga la plataforma (solo las 15 columnas que usa). |
| `README.md` | Estas instrucciones. |

## Privacidad

Las transcripciones provienen de llamadas reales de la Línea 123 y fueron desidentificadas: nombres, teléfonos, cédulas, direcciones, barrios y placas se reemplazaron por etiquetas como `[NOMBRE_VICTIMA]` o `[NUMERO_SENSIBLE]`. No intente identificar a ninguna persona. Si encuentra un dato que permita identificar a alguien, repórtelo de inmediato al contacto de abajo para retirarlo.

Durante la prueba no escriba datos personales reales en ningún campo.

## Contacto

Natalia Galvis Arias — University of Manchester
natalia.galvisarias@postgrad.manchester.ac.uk
