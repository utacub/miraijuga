# Integració dels recursos PWA de Mira Juga

## Fitxers preparats

La carpeta `icons/` conté els PNG i el favicon. `manifest.webmanifest` utilitza rutes relatives perquè es pugui situar a l’arrel de l’app publicada a `/miraijuga/`. El nom visible preparat és **Mira Juga**.

1. Copia el contingut de `icons/` a la carpeta `icons/` de l’app.
2. Incorpora el manifest preparat després de revisar-lo amb el projecte. Conserva l’identificador, l’inici i l’abast relatius `./` de la configuració consultada.
3. Revisa les etiquetes existents del document i integra les de `head-snippet.html`, evitant duplicar els enllaços al manifest i a les icones.
4. Actualitza el títol i els textos visibles de l’app que encara diguin «Mira i Juga» si es vol aplicar el canvi de nom a tota la interfície.
5. Si el projecte precarrega les icones al service worker, incorpora les noves rutes al mecanisme de memòria cau corresponent.
6. Després de publicar, comprova l’apartat d’icones i manifest del navegador, i prova la instal·lació en els sistemes objectiu. La validació del paquet comprova fitxers i geometria; no substitueix aquesta prova en dispositius.

## `any` i `maskable`

Les imatges `icon-192.png`, `icon-512.png` i `icon-1024.png` són les versions normals. Les `icon-maskable-*.png` incorporen un marge més ampli. El manifest distingeix les dues finalitats per permetre que cada sistema esculli el recurs apropiat (MDN contributors, 2025).

Les icones tenen fons opac. A les maskable, el símbol essencial s’ha situat dins el cercle central protegit de radi 40% (MDN contributors, 2025; Steiner & Oakes, s. d.).

## iPad i iPhone

S’inclouen les etiquetes `apple-touch-icon` amb les mides 152, 167 i 180 px i l’àlies de 180 px. La guia oficial d’Apple documenta l’ús de diversos enllaços amb `sizes` perquè el dispositiu triï el recurs adequat (Apple, s. d.).

## Referències

Apple. (s. d.). *Configuring web applications*. Safari Web Content Guide. https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html

MDN contributors. (2025, 30 de juny). *Define your app icons*. MDN Web Docs. https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/How_to/Define_app_icons

Steiner, T., & Oakes, T. (s. d.). *Adaptive icon support in PWAs with maskable icons*. web.dev. https://web.dev/articles/maskable-icon
