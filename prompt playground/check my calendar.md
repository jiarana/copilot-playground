# Revisa mi calendario

## Qué es

Un prompt de planificación que pide a Copilot que encuentre huecos libres para reuniones en los próximos 10 días laborables. Descarta las partes problemáticas del calendario, añade margen entre reuniones y devuelve texto sin formato que puedes pegar para alguien de fuera de tu organización.

Úsalo cuando necesites ofrecer tu disponibilidad sin revisar el calendario a mano.

> [!TIP]
> Si tu agenda tiene otras restricciones, ajusta la duración de la reunión, el horario laboral y la zona horaria antes de pegarlo.

---

## Copia rápida

```
Revisa mi calendario y enumera de 6 a 8 huecos libres de 30 a 45 minutos en los próximos 10 días laborables, entre las 9:00 y las 16:00 en mi zona horaria. Excluye desplazamientos, tiempo de concentración, la comida y los bloqueos reservados. Deja 15 minutos de margen antes y después de otras reuniones. Devuélvelo en texto sin formato que pueda pegar para un contacto externo, con este formato:

- Mar 18 nov, 10:30–11:00 CET
- Mié 19 nov, 13:00–13:45 CET
- Jue 20 nov, 9:15–10:00 CET

Añade una frase de cierre: "Si ninguno de estos horarios te viene bien, indícame algunas franjas y te envío una convocatoria."
```

---

## Qué hace cada instrucción

| Instrucción | Qué controla |
|---|---|
| `número de huecos y duración de la reunión` | Ofrece suficientes opciones sin saturar al destinatario. |
| `próximos 10 días laborables` | Mantiene el periodo de búsqueda útil y cercano. |
| `entre las 9:00 y las 16:00` | Evita horas demasiado tempranas, tardías o incómodas. |
| `Excluye desplazamientos, tiempo de concentración, la comida y los bloqueos reservados` | Protege los bloques del calendario que no deben convertirse en huecos para reuniones. |
| `texto sin formato que pueda pegar` | Deja el resultado listo para un correo o un chat. |

---

[Volver a Prompt Playground](../README.md#prompt-playground)
