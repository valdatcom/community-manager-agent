# Community Manager de Val

Este es el agente que programa las publicaciones de Val (clips, teasers y trial reels) en Instagram y YouTube Shorts con Buffer, y lleva el calendario de Notion.

Todo lo que sabe hacer está en un solo archivo: `skill/SKILL.md`. Ahí están las reglas, los IDs de las cuentas, la cadencia, cómo escribir los captions y lo que fuimos aprendiendo.

## Cómo instalarlo en otra computadora

1. **Instala Claude** (la app de escritorio, pestaña Code) e inicia sesión con tu cuenta.
2. **Descarga este repositorio.** En PowerShell:

   ```powershell
   git clone https://github.com/valdatcom/community-manager.git D:\community-manager
   ```

3. **Conecta el skill con Claude.** En PowerShell (crea un acceso directo, así lo que se aprenda queda guardado en la carpeta del repositorio):

   ```powershell
   New-Item -ItemType Junction -Path "$env:USERPROFILE\.claude\skills\community-manager" -Target "D:\community-manager\skill"
   ```

   Si la carpeta `community-manager` ya existe en `.claude\skills`, bórrala primero.

4. **Activa los conectores en Claude** (Configuración › Conectores), con tus cuentas:
   - **Buffer** (cuenta gratis de Val): para programar.
   - **Notion**: calendario de publicaciones y Tracker de videos.
   - **Google Drive** (projects.valmorao): de ahí salen los videos.
   - **Google Calendar**: los recordatorios de los sábados.

5. **Pruébalo.** Abre una sesión nueva y escribe: "programa la semana en Buffer". Claude debería cargar el skill solo.

## Qué NO está aquí

- Contraseñas: nunca se guardan aquí. Cada conector se conecta con tu cuenta.
- Videos: viven en Drive y en tu computadora.
- Los skills de edición (`editar-vlog` y el de clips): están en sus propios repositorios.

## Cómo se mantiene al día

Cada vez que aprendemos algo nuevo, Claude lo anota en `skill/SKILL.md` y te ofrece subirlo a GitHub al cerrar la tanda de trabajo.
