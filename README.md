# ADSBlockVM-Listas

Las listas de bloqueo que usa ADSBlockVM (DNS propio sin anuncios, en Rust), copiadas de sus autores y
convertidas a un solo formato para DNS:

- `||dominio^` para bloquear y `@@||dominio^` para permitir, ordenadas y sin repetidos;
- sin las reglas que no sirven en un DNS (las cosméticas y las de navegador);
- sin los subdominios que ya cubre su dominio padre;
- las reglas especiales que ADSBlockVM sí entiende (expresiones, `$important`, `$dnsrewrite`…), tal cual.

Se revisan **cada hora**: a cada autor se le pregunta si su lista cambió y solo se actualizan las que cambiaron.
`indice.json` dice, de cada copia, su huella, cuántas reglas tiene y cuándo cambió por última vez.

## Paquetes

Juntan varias listas en una, sin repetidos:

| Paquete | Para qué |
|---|---|
| `listas/paquete-basica.txt` | Anuncios y rastreo de las listas más usadas. Casi nunca rompe nada. |
| `listas/paquete-completa.txt` | Anuncios, rastreo, ventanas emergentes y rastreo disfrazado. Más fuerte. |
| `listas/paquete-seguridad.txt` | Malware, phishing, estafas, ransomware, minado escondido y stalkerware. |

## Créditos

Cada lista es obra de su autor y conserva su licencia: aquí solo se cambia el formato. En la cabecera de cada copia
está su fuente original, la página del autor y su licencia, y en [CREDITOS.md](CREDITOS.md) están todas juntas.
Gracias a AdGuard, HaGeZi, OISD, StevenBlack, Firebog, Block List Project, EasyList, AdAway, Peter Lowe y a todos
los demás autores.

Si eres autor de una lista y quieres que se cambie algo de cómo aparece aquí, abre un *issue*.

---

Creado por Ing. Victor Maldonado - VMSofts
