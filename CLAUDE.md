# Men De Antes SMP — Contexto del proyecto

Este es el servidor de Minecraft del Men De Antes SMP. Un servidor narrativo con lore profundo, dungeons personalizadas y una historia que los jugadores descubren progresivamente. Antes de hacer cualquier cambio, lee este archivo completo.

---

## Stack técnico

- **Minecraft:** 1.19.2
- **Base:** Arclight (Forge + Bukkit híbrido) — versión 1.0.5
- **Forge:** 43.3.8
- **Host:** Exaroton
- **Jugadores simultáneos:** 8-10

---

## Estructura del servidor

```
/
├── mods/              # Mods de Forge (.jar)
├── plugins/           # Plugins de Bukkit (.jar y configs)
├── kubejs/
│   ├── server_scripts/    # Scripts de eventos y lógica del juego
│   ├── startup_scripts/   # Recetas y registro de ítems
│   └── client_scripts/    # Tooltips y efectos cliente
├── scripts/           # Scripts de CraftTweaker (.zs)
├── config/            # Configuraciones de mods
├── world/             # Datos del mundo
│   └── ftbquests/     # Progreso de quests de jugadores
├── config/ftbquests/
│   └── quests/
│       └── chapters/  # Definición de quests en formato SNBT
└── server.properties
```

---

## Mods instalados — estado actual

### Optimización (conservar todos)
- `embeddium` — renderer optimizado
- `embeddiumplus` — extensión de embeddium
- `ferritecore` — reduce uso de RAM
- `modernfix` — optimización general
- `starlight` — optimización de lighting
- `entityculling` — culling de entidades
- `chunky` — pre-generación de chunks
- `lazydfu` — optimiza carga inicial
- `ai-improvements` — mejora IA de mobs
- `alternate-current` — optimiza redstone
- `fastsuite` — optimiza furnace

### Narrativos (núcleo del proyecto)
- `mns` — mod del Wither Storm (contiene Formidibomb y Pico de Comandos)
- `dungeonsarise` — dungeons generadas para el lore
- `the_graveyard` — estructuras oscuras para el científico
- `terralith` — biomas del mundo
- `structory` — ruinas y estructuras narrativas
- `supplementaries` — props narrativos (notas, mapas, señales)
- `create` — maquinaria del científico (taladro del lore)
- `kubejs` — eventos y lógica narrativa custom
- `crafttweaker` — recetas custom
- `ftb-quests` — sistema de misiones y páginas del diario
- `ftb-library` — dependencia de FTB
- `ftb-teams` — dependencia de FTB
- `geckolib` — animaciones de mobs custom
- `curios` — ítems equipables del lore (Collar del Silencio)
- `camera-forge` — cinemáticas in-game
- `mdamod1.0` — mod custom del owner con ítems argumentales

### SMP (quality of life)
- `voicechat` — comunicación de voz
- `jei` — recetas en juego
- `jade` — información de bloques
- `ironchest` — cofres mejorados
- `sophisticatedbackpacks` — mochilas
- `chipped` — variaciones decorativas
- `mcw-furniture` — muebles
- `emojiful` — emojis en chat
- `immersive-portals` — portales mejorados
- `automodpack` — distribución automática del modpack
- `architectury` — dependencia de mods
- `cloth-config` — dependencia de mods
- `moonlight` — dependencia de mods
- `resourcefullib` — dependencia de mods
- `placebo` — dependencia de mods
- `cupboard` — dependencia de mods
- `konkrete` — dependencia de mods
- `polymorph` — conflictos de recetas
- `rhino` — dependencia de KubeJS
- `mine-pop` — funkos coleccionables

### A eliminar (pendiente)
- `twilightforest` — 23MB, no se usa en el proyecto
- `ImmediatelyFast` — client-only, causa crash en servidor
- `Icterine` — shaders client-only
- `betterfpsdist` — optimización client-only
- `CTM` — connected textures client-only
- `CullLessLeaves` — visual client-only

---

## Plugins instalados

| Plugin | Función |
|--------|---------|
| WorldEdit | Construcción de dungeons y estructuras |
| WorldGuard | Protección de regiones y zonas |
| ExecutableItems | Ítems especiales del lore (Collar del Silencio, etc.) |
| ConditionalEvents | Eventos narrativos y triggers |
| Multiverse-Core | Gestión de mundos |
| SkinsRestorer | Skins de jugadores |
| PlaceholderAPI | Variables para plugins |
| ProtocolLib | Dependencia de plugins |
| Vault | Economía básica |
| NametagEdit | Nombres de jugadores |
| ItemEdit | Edición de ítems (usar solo v3.7.1) |
| SCore | Dependencia de ExecutableItems |

### Plugins a instalar (pendiente)
- **LuckPerms** — sistema de permisos y rangos
- **MythicMobs** — jefes narrativos (bestia del coliseo)
- **FancyNpcs** — NPCs con diálogos (el Científico, guías)

---

## Problemas activos a resolver

1. **CRASH CRÍTICO** — `CasinoCraft` requiere `lucky77 4.0+` pero Lucky77 instalado no se registra correctamente → actualizar Lucky77 o eliminar CasinoCraft
2. **ItemEdit duplicado** — `ItemEdit-2.10.jar` y `ItemEdit-3.7.1.jar` instalados simultáneamente → eliminar el 2.10
3. **Configs huérfanas** — existen configs de `corpse`, `elevator`, `journeymap`, `fastleafdecay` sin su jar correspondiente → limpiar
4. **server.properties** — `max-tick-time=600000` (debería ser 60000), `difficulty=easy` (cambiar a normal), `enforce-whitelist=false`

---

## Lore del proyecto (resumen ejecutivo)

### El mundo
Ocurre 3000 años después de una batalla contra el Wither Storm. El mundo es el mismo pero envejecido. Los jugadores despiertan sin que nadie recuerde lo que pasaron.

### El antagonista — El Científico
Entidad de un mod con consciencia propia. Perdió a su hija en la Tormenta Warden (evento causado por el owner/admin del servidor anterior). Lleva 3000 años planeando conseguir el poder del huevo de dragón para controlar el mundo y que ningún admin pueda volver a causar desastres. En el fondo solo quiere revertir la muerte de su hija. Frío, calculador, frustrado. No es un villano que disfruta el mal.

### El equipo — Los Men De Antes
- Diego (Hearty_FM) — owner y admin, el único con poderes de admin
- Rafa (Rafaqv11) — sociable, rol clave en el final
- Mati — el más querido del grupo
- Roa (Matibuu) — original
- Tux (pingux_1234) — el más creativo
- Más jugadores que se unen en Capítulo 1

### Mele
Goblin de las cuevas. Amigo del grupo desde el servidor anterior. Detectó el Wither Storm antes que nadie. Reaparece en el final en avioneta con la Formidibomb.

---

## Ítems argumentales

### Collar del Silencio
- Tipo: totem de cuello (ítem equipable via Curios)
- Función: sobrecarga la consola admin de Diego, lo deja sin poderes por minutos
- Lore: *"Construido para silenciar al arquitecto del mundo. Mientras lo portes, ningún dios podrá tocarte."*
- Implementar en: ExecutableItems

### Formidibomb
- Tipo: objeto real del mod `mns` (Wither Storm mod)
- Crafteo: Super TNT + 4 Gunpowder (esquinas) + 4 Blaze Powder (lados)
- Función: única forma de pasar Fase 5 del Wither Storm
- Lore: *"Una sola explosión. Una sola oportunidad. Úsala bien."*

### Ballesta del Fin
- Tipo: ballesta custom con Poder 255
- Función: instakill a cualquier entidad, un solo uso
- Lore: *"Tres mil años de investigación en un solo disparo. Que no falle."*
- Implementar en: ExecutableItems

### Pico de Comandos
- Tipo: objeto real del mod `mns`
- Obtención: libro de Withered Symbiont + pico en Anvil
- Función: destruye bloques irrompibles
- Lore: *"Hecho para romper lo irrompible. Porque a veces las reglas del mundo también necesitan romperse."*

---

## Dungeons

### Stronghold (Capítulo 1)
Portal del End vacío — el Científico se lo llevó con el Pico de Comandos. Pasillos llenos de mobs acumulados. Genera sensación de amenaza sin revelar quién.

### El Cubo (Capítulo 2)
Rectángulo de piedra con grabados. 8 botones en la entrada que separan al equipo en caminos distintos. Todos convergen en el coliseo interior techado. El Científico los observaba desde la zona VIP. Al llegar ya se fue — solo quedan páginas del diario.

### El Laboratorio (Capítulo 3)
Casa normal cerca de la aldea. Explosión deliberada como anzuelo. Palanca oculta tras escaleras → laboratorio subterráneo. Contiene los 8 libros con los nombres del equipo y las páginas más importantes. TNT temporizador como trampa para ganar tiempo.

### Dungeons generadas (Capítulos 1-4)
DungeonsArise, The Graveyard, Structory. El Científico dejó páginas del diario sueltas. No todas las dungeons tienen páginas — la exploración es la aventura.

---

## Sistema de páginas del diario

Las páginas están dispersas por el mundo en cofres de dungeons generadas. Son entradas de un diario desarmado. Tono frío y técnico — el Científico escribe como científico, no como diario personal.

Las páginas de los ítems están agrupadas en el laboratorio.

En FTB Quests: capítulo `paginas_del_diario` existe pero está vacío. Hay que poblarlo.

---

## Scripts activos en CraftTweaker

- `removebackpacks.zs` — elimina todas las recetas de SophisticatedBackpacks
- `removeironchesst.zs` — elimina todas las recetas de IronChest

Estos bloqueos son intencionales. Los ítems existen pero no se pueden craftear normalmente.

---

## Convenciones para scripts KubeJS

- Todos los scripts narrativos van en `kubejs/server_scripts/`
- Un archivo por capítulo o sistema: `capitulo1.js`, `coliseo.js`, `laboratorio.js`, etc.
- Mensajes del Científico en color `#8888FF` (azul frío)
- Mensajes del sistema narrativo en `#AAAAAA` (gris, itálica)
- Mensajes de evento global en `#FFD700` (dorado, negrita)
- Coordenadas siempre en comentarios sobre el trigger

---

## Convenciones para ExecutableItems

- Ítems del lore van en `plugins/ExecutableItems/items/Lore/`
- Nomenclatura: `MDA_NombreItem.yml`
- Siempre incluir lore del ítem en la descripción

---

## Prioridades de desarrollo

1. Limpiar mods client-only y arreglar crash de CasinoCraft
2. Corregir server.properties
3. Instalar LuckPerms, MythicMobs, FancyNpcs
4. Crear scripts KubeJS para eventos del Capítulo 1 y 2
5. Implementar Collar del Silencio y Ballesta del Fin en ExecutableItems
6. Poblar FTB Quests con las páginas del diario
7. Construir las dungeons con WorldEdit

---

## Lo que NO debes hacer

- No eliminar `mdamod1.0.jar` — es el mod custom del owner
- No eliminar `mns` — contiene la Formidibomb y el Pico de Comandos del lore
- No eliminar `immersive-portals` — tiene uso activo
- No modificar las recetas de CraftTweaker sin consultar — los bloqueos son intencionales
- No cambiar el mundo existente sin backup previo
- No instalar mods client-only en la carpeta del servidor
