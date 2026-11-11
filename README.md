# Web de recursos de Finmente Noir (GitHub Pages)

- **Qué es:** una web estática y sin build para alojar los recursos gratis (la calculadora y, más adelante, los PDF gratis) y la política de privacidad.
- **Dónde se publica:** cuenta de GitHub **0003-YIDev**.
- **No es el escaparate:** la página "Recursos Finmente Noir" de MailerLite sigue siendo el escaparate (el link de la bio). Esta web solo aloja lo que MailerLite no puede alojar.

## Contenido
| Ruta | Qué es |
|------|--------|
| `index.html` | Portada con los recursos publicados (de momento, solo la calculadora) |
| `calculadora/index.html` | Copia de `production/output/calculadora.html`. Si cambias la original, vuelve a copiarla aquí |
| `privacidad/index.html` | Política de privacidad. **Es un borrador con huecos en dorado: rellénalo antes de publicar** |
| `recursos/` | PDF **gratis**, si no usas el File manager de MailerLite |
| `estilo.css` | Paleta y tipografía de marca |
| `.nojekyll` | Evita que GitHub procese la web con Jekyll |

## Publicar (desde el navegador, sin instalar nada)
1. **Crea el repositorio:** en github.com, con la cuenta 0003-YIDev, **New repository** → nombre `recursos` → **Public** → Create.
   - El plan gratis de GitHub Pages necesita un repositorio público.
2. **Sube los archivos:** **Add file → Upload files** y arrastra **todo el contenido** de esta carpeta (no la carpeta en sí) → Commit.
   - Comprueba que `.nojekyll` también se sube. Si el navegador oculta los archivos que empiezan por punto, créalo con **Add file → Create new file**, con el nombre `.nojekyll` y vacío.
3. **Activa Pages:** **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)`** → Save.
4. **Comprueba:** en uno o dos minutos estará en `https://0003-yidev.github.io/recursos/`. GitHub pone el nombre de usuario en minúsculas en la URL.

## Subdominio propio (opcional, recomendado): `recursos.finalmente.money`
1. **En Namecheap → Advanced DNS:** registro **CNAME**, host `recursos`, valor `0003-yidev.github.io.`
2. **En GitHub → Settings → Pages → Custom domain:** escribe `recursos.finalmente.money` → Save. Cuando el certificado esté listo, marca **Enforce HTTPS**.
3. **Archivo CNAME:** GitHub crea en el repositorio un archivo `CNAME` con ese dominio. No lo borres.

Este registro CNAME convive sin problemas con los de MailerLite (SPF, DKIM y DMARC) y con el reenvío de email.

## Reglas
- **Solo recursos publicados y que funcionan:** nada de "próximamente" (distribution/CONTEXT.md).
- **Nunca la edición de pago:** el repositorio es público.
- **Ningún dato personal** más allá del responsable que exige la política de privacidad.
