# Contributing

We werken op de volgende wijze:

## Git werkwijze

Voor elke feature maken we een aparte branch. Als de feature klaar is voor review, wordt er een merge request aangemaakt, zodat andere teamleden feedback kunnen geven. Als minimaal 1 andere teamlid de feature goedkeurt, wordt het ge-merged en automatisch ge-deployed.

## Features

Elke feature heeft in principe z'n eigen CSS en JavaScript bestanden. De basis layout van de feature wordt in het `index.html` bestand gedefinieerd. De styling komt in een apart CSS bestand in `./docs/assets/css` en wordt via `./docs/assets/css/main.css` ge-import. Eventuele JavaScript logica komt in een apart bestand in de `./docs/assets/js` folder en wordt in `./docs/main.js` ingeladen.
