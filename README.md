Resa · KPI Assistant — Deploy en GitHub Pages
Archivos del proyecto
```
/
├── index.html       ← La aplicación (no tocar)
├── config.json      ← Tu API key de Anthropic  ⚠️
├── context.txt      ← Tu documentación de KPIs y modelo de datos
└── README.md
```
---
1. Configurar la API key
Edita `config.json` y sustituye el placeholder por tu key real:
```json
{
  "apiKey": "sk-ant-api03-TU_KEY_REAL_AQUÍ"
}
```
---
2. Actualizar el contexto
Edita `context.txt` con tu documentación real:
Glosario de KPIs y métricas
Fórmulas y criterios de cálculo
Descripción del modelo de datos
Filtros y exclusiones aplicadas
Notas de negocio
El archivo puede tener hasta ~80.000 palabras sin problema.
---
3. Publicar en GitHub Pages
Crea un repositorio en GitHub (puede ser privado)
Sube los 3 archivos: `index.html`, `config.json`, `context.txt`
Ve a Settings → Pages
En Source selecciona `Deploy from a branch` → `main` → `/ (root)`
Guarda. En 1-2 minutos tendrás una URL tipo:
`https://tu-usuario.github.io/nombre-repo/`
---
4. Embeber en Power BI
Opción A — Visual "HTML Viewer" (AppSource)
En Power BI Desktop, importa el visual "HTML Viewer" desde AppSource
Añádelo al informe
En el campo URL pega tu URL de GitHub Pages
Opción B — Tile de URL (Dashboard)
En un Dashboard de Power BI Service, añade un tile
Selecciona "Contenido web"
Pega la URL
---
⚠️ Seguridad
`config.json` con la API key quedará accesible si el repo es público.
Para uso interno corporativo es aceptable. Si necesitas más seguridad:
Usa un repo privado con GitHub Pages (requiere plan de pago)
O monta un proxy mínimo en Azure Functions / Cloudflare Workers
que inyecte la key en servidor
---
Actualizar el contexto sin redesplegar
Simplemente edita `context.txt` en GitHub directamente desde el navegador
y haz commit. El cambio se refleja en segundos, sin tocar el HTML.
