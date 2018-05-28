# Awesome International Image Interoperability Framework (IIIF) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

[<img src="https://upload.wikimedia.org/wikipedia/commons/e/e8/International_Image_Interoperability_Framework_logo.png" align="right" width="100">](http://iiif.io/)

Una lista de listas de recursos awesome [IIIF](http://iiif.io/).

El International Image Interoperability Framework (IIIF) es un grupo de APIs estándar para compartir y reusar información. También es una creciente comunidad de galerías, bibliotecas, archivos, museos, compañías, y otros que desarrollan estándares e implementaciones de software interoperables. El contenido incluye enlaces útiles para cada estándar, demostraciones de sus usos, y tutoriales y presentaciones. La lista es especialmente útil para orientar a nuevos miembros de la comunidad y desarrolladores.

[![Orientaciones para Contribuir](http://img.shields.io/badge/CONTRIBUTING-Guidelines-blue.svg)](./contributing.md)

**Aviso Legal**: Esta lista es creada para propósitos informativos solamente, y sus enlaces no constituyen un apoyo, recomendación, o preferencia por parte de IIIF Consortium.

## Contenidos
- [Estándares](#standards)
- [Servidores de Imágenes](#image-servers)
- [Shims de Servidor de Imágenes](#image-server-shims)
- [Visores de Imágenes](#image-viewers)
- [Librerías de la API de Imagen](#image-api-libraries)
- [Herramientas de Imagen](#image-tools)
- [Librerías de la API de Presentación](#presentation-api-libraries)
- [Shims de la API de Presentación](#presentation-api-shims)
- [Herramientas de Manifest de Presentación](#presentation-manifest-tools)
- [Servidores de la API de Búsqueda de Contenido](#content-search-api)
- [Autenticación](#authentication)
- [Tutoriales](#tutoriales)
- [Videos y Diapositivas](#videos-and-slide-decks)
- [Descubrimiento](#discovery)
- [Anotaciones](#annotations)
- [Integración a CMS](#cms-integration)
- [Periódicos](#newspapers)
- [STEM](#stem)
- [Experimentos y Diversión](#experiments-and-fun)
- [Comunidad](#community)

## Estándares

La comunidad de IIIF ha desarrollado varios estándares para la entrega de imágenes interoperables, basadas en la web.

- [API de Imagen](http://iiif.io/api/image/) - especifica un servicio web que retorna una imagen en respuesta a una petición HTTP o HTTPS estándar.
- [API de Presentación](http://iiif.io/api/presentation/) - proporciona la información necesaria para presentar al usuario humano un entorno de visualización en línea, enriquecido, para objetos basados primariamente en imágenes, posiblemente en conjunto con la API de Imagen de IIIF.
- [API de Búsqueda de Contenido](http://iiif.io/api/search/) - especifica el mecanismo de interoperabilidad para buscar en las anotaciones.
- [API de Autenticación](http://iiif.io/api/auth/) - describe un conjunto de flujos de trabajo para guiar al usuario a través de un sistema de control de acceso existente.
- [Anexo de API de Servicios Externos](http://iiif.io/api/annex/services/) - describe el conjunto de servicios relacionados que se han identificado como útiles para referenciar desde las APIs de IIIF.
- [Documentos de Anexo de API](http://iiif.io/api/annex/) - Lista de todos los documentos de anexo de API y notas de implementación de API.

## Listas Adicionales

- [Implementaciones](https://github.com/IIIF/awesome-iiif/blob/master/implementations.md)
- [Lectura y Visualización](https://github.com/IIIF/awesome-iiif/blob/master/reading-viewing.md)

## Servidores de Imágenes

Estos servidores soportan la API de Imagen de IIIF. Algunos pueden tener soporte para la API de Presentación.

- [Loris](https://github.com/loris-imageserver/loris) escrito en Python.
- [IIPImage Server](http://iipimage.sourceforge.net/documentation/server/) servidor de imágenes de alto rendimiento.
- [riiif](https://github.com/curationexperts/riiif) escrito en Ruby como motor Rails.
- [SIPI](https://github.com/dhlab-basel/Sipi) servidor de imágenes de IIIFv2 escrito en C++.
- [RAIS](https://github.com/uoregon-libraries/rais-image-server) servidor de mosaicos, de código abierto 100%, para imágenes JP2, escrito en Go.
- [digilib](http://digilib.sourceforge.net) servidor de imágenes escrito en Java.
- [Cantaloupe](https://medusa-project.github.io/cantaloupe/) servidor de imágenes escrito en Java.
- [iiif_s3](https://github.com/cmoa/iiif_s3) librería de Ruby para generar un servidor de IIIF estático de nivel 0 para las APIs de Imagen y Presentación en Amazon S3.
- [Hymir IIIF Server](https://github.com/dbmdz/iiif-server-hymir) servidor de IIIF escrito en Java que soporta las APIs de Imagen y Presentación de IIIF.
- [go-iiif](https://github.com/thisisaaronland/go-iiif) servidor de IIIF escrito en go (fork de [greut/iiif](https://github.com/greut/iiif)).

## Shims de Servidor de Imágenes

Estos shims permiten usar un servidor de imágenes que no soporte IIIF. Si aún no ha implementado un servidor de imágenes, este no debiera ser su punto de partida.

- [gem de Ruby Djatoka](https://github.com/jronallo/djatoka) convierte URLs de IIIF en las URLs que requiere Djatoka.
- [Shimmy](https://github.com/mejackreed/shimmy) es una gem de Ruby diseñada para ayudar a construir shims para la API de Presentación de IIIF.
- [traductor de imágenes de ContentDM](https://github.com/azaroth42/pi3f/tree/master/shims/ContentDM) hace que las imágenes de ContentDM estén disponibles a través de IIIF. Python.
- [Flask-IIIF](https://github.com/inveniosoftware/flask-iiif) extensión de Flask para soportar IIIF en aplicaciones Python/Flask. Vea [demo Flask-IIIF previewer](http://flask-iiif.herokuapp.com/previewer) y [demo Flask-IIIF RESTful](http://flask-iiif.herokuapp.com/restful).

## Visores de Imágenes
- [Universal Viewer](https://github.com/UniversalViewer/universalviewer) es una interfaz incrustable enriquecida.
- [OpenSeadragon](https://openseadragon.github.io/examples/tilesource-iiif/) tiene soporte de mosaicos de IIIF.
  - [Plugin Scalebar](https://github.com/NIST-ISG/OpenSeadragonScalebar) plugin de OpenSeadragon para superposición de escala física.
  - [Plugin Imaging Helper](https://github.com/msalsbery/OpenSeadragonImagingHelper) plugin de OpenSeadragon con funciones de utilidad.
- [Leaflet-IIIF](https://github.com/mejackreed/Leaflet-IIIF) visor de imágenes de IIIF ligero y extensible.
- [Mirador](https://github.com/IIIF/mirador) espacio de trabajo multi-up. Vea también [lista Awesome de Mirador](https://github.com/ProjectMirador/mirador-awesome).
- [Diva.js](https://ddmal.github.io/diva.js/) visor de imágenes de IIIF optimizado para velocidad y flexibilidad.
- [IIIFViewer](https://github.com/klokantech/iiifviewer) visor WebGL / Canvas / DOM de IIIF, veloz y compatible con móviles, basado en OpenLayers V3
- [Tify](https://github.com/subugoe/tify) es un visor de documentos de IIIF, ligero y veloz, construído con Vue.js
- [IIIF Curation Viewer](http://codh.rois.ac.jp/software/iiif-curation-viewer/) - Un visor general de IIIF con enfoque añadido a la curación y ordenamiento de imágenes recortadas de IIIF. [Demo](http://codh.rois.ac.jp/software/iiif-curation-viewer/demo/?curation=https://gist.githubusercontent.com/2SC1815J/18e1228c52a6650c64902142ed7496f8/raw/7a247b64b6e22357e83f573b7283e31f3111af68/curation_kibutsu.json&pos=4)
- [CanvasPanel](http://canvas-panel.netlify.com/) es una librería React para construir experiencias de visualización de nivel de Presentación 3 de IIIF, incluyendo soporte para anotaciones.

## Librerías de la API de Imagen
- [iiif-apis](https://github.com/dbmdz/iiif-apis) librerías de las APIs de IIIF en Java.
- [piffle](https://github.com/emory-lits-labs/piffle) librería de Python para generar y parsear URLs de la API de Imagen de IIIF.
- [iiif_url](https://github.com/NCSU-Libraries/iiif_url) librería de Ruby para crear y parsear URLs de la API de Imagen de IIIF.
- [iiif](https://github.com/zimeon/iiif) librería de Python que proporciona una implementación de referencia de la API de Imagen. También incluye un servidor de pruebas y un generador de mosaicos estáticos.
- [iOSTiledViewer](https://github.com/moravianlibrary/iOSTiledViewer) - visor de la API de Imagen de IIIF y Zoomify para iOS, escrito en Swift

## Herramientas de Imagen

Diversas herramientas para trabajar con imágenes, por ejemplo, herramientas de recorte.

- [Recorte de Leaflet-IIIF](https://bl.ocks.org/mejackreed/6936585f435b60aa9451ae2bc1c199f2) - Ejemplo de uso de Leaflet para proporcionar recorte de IIIF.
- [Recortador de Stanford](https://github.com/lizfischer/iiif-tools#cropper) - Sencillo recortador de imágenes.
- [Herramienta de Recorte de OpenSeadragon](http://sul-dlss.github.io/iiif-cropper/demo/) - Script para permitir el recorte de imágenes desde OpenSeadragon.
- [Recortador de Imágenes de Wikimedia Commons](http://zone47.com/crotos/lab/cropper/) - Crea regiones de imagen de IIIF a partir de archivos de imagen de Wikimedia Commons.
- [TryIIIF](http://tryiiif.herokuapp.com/) - Herramienta de ejemplo para visualizar cualquier imagen accesible en la web desde un par de visores de imágenes de IIIF.
- [IIIF-imageManipulation](https://github.com/jbhoward-dublin/iiif-imageManipulation) - Herramienta de la UCD para recortar imágenes y manipular por medio de atributos de IIIF; integra con Mirador mediante plugin.
- [Compariscope](https://vanda.github.io/iiif-features/) - Una app demo del Victoria & Albert útil para la alineación de imágenes superpuestas, servidas por la API de Imagen de IIIF, y que proporciona un visor interactivo para las imágenes superpuestas, presentadas con fluidez, usando etiquetas de imagen responsivas.


## Librerías de la API de Presentación
- [Manifesto](https://github.com/UniversalViewer/manifesto) librería de utilidades de cliente y servidor de la API de Presentación de IIIF.
- [Manifold](https://github.com/UniversalViewer/manifold) Envuelve Manifesto para ofrecer estado de visor y utilidades relacionadas.
- [O'Sullivan](https://github.com/IIIF/osullivan) API de Ruby para crear manifests de IIIF.
- [iiif-prezi](https://github.com/IIIF/iiif-prezi) librería de Python que proporciona una implementación de referencia.
- [iiif-apis](https://github.com/dbmdz/iiif-apis) librerías de las APIs de IIIF en Java.
- [IIIF Manifest Generator](https://github.com/yale-web-technologies/IIIF-Manifest-Generator) librería de PHP para generar manifests de IIIF.
- [tabula-rasa](https://www.npmjs.com/package/tabula-rasa) módulo npm para crear y manipular manifests de IIIF.
- [iiif-tree-component](https://github.com/edsilv/iiif-tree-component) menú de árbol de IIIF, ordenable por fecha, con capacidad de multi-selección.
- [Tripoli](https://ddmal.github.io/tripoli/) librería de validación de la API de Presentación de IIIF 2.0+.
- [ViewDir](https://viewdir.github.io/index.html) documentación sobre librerías y componentes relacionados a IIIF, de una comunidad abierta de diseñadores y desarrolladores interesados en crear interfaces componibles e interoperables para consumir y crear contenido en línea.
- [Swiiift](https://github.com/mejackreed/Swiiift) - librería de la API de Presentación de IIIF para Swift.

## Shims de la API de Presentación

Estos shims permiten usar sistemas con metadatos de presentación (por ejemplo, estructura o secuencias) que no soporten IIIF. Si aún no ha implementado la API de Presentación, este no debiera ser su punto de partida.

- [Shimmy](https://github.com/mejackreed/shimmy) es una gem de Ruby diseñada para ayudar a construir shims para la API de Presentación de IIIF, y tiene muestras para NYPL, Flickr, y US National Archives.
- [Chronicling America](https://github.com/azaroth42/presentation-api-shims/tree/master/shims/chronam) para periódicos digitalizados en el National Digital Newspaper Program.

## Herramientas de Manifest de Presentación

- [Manifest Editor](https://github.com/bodleian/iiif-manifest-editor) - Aplicación web para importar, visualizar, actualizar, y exportar manifests. Vea un [demo](http://morning-journey-27147.herokuapp.com/#/?_k=agcbor).
- [demetsiiify](https://github.com/jbaiter/demetsiiify) - Servicio web para crear manifests de IIIF a partir de documentos METS/MODS.
- [biiif](https://github.com/edsilv/biiif/) - Organiza sus archivos de acuerdo a una sencilla convención de nombrado para generar manifests de IIIF v3.

## API de Búsqueda de Contenido

Librerías y aplicaciones que soportan la API de Búsqueda de Contenido.

- [Ocracoke](https://github.com/NCSU-Libraries/ocracoke) - Aplicación Rails para crear, indizar, y buscar texto de imágenes de página, y proporcionar resultados en el formato de la API de Búsqueda de Contenido de IIIF.

## Autenticación

Algunos recursos sobre la API de Autenticación de IIIF.

- [IIIF Auth Demonstrator](https://iiifauth.digtest.co.uk/) - Manifests con imágenes acompañantes que demuestran varios modos de autenticación de IIIF.
- [IIIF.io : the hardest part will be saying "no".](http://mcormond.blogspot.com/2017/06/iiif-hardest-part-saying-no.html) - Blogpost de Russell McOrmond considerando los retos de restringir el acceso a los recursos de Canadiana.
- [iiif-auth-server](https://github.com/digirati-co-uk/iiif-auth-server) - Un demo de implementación de servidor de todos los aspectos de la especificación de Autenticación de IIIF.
- [iiif-auth-client](https://github.com/digirati-co-uk/iiif-auth-client) - Implementación de cliente de la especificación de Autenticación de IIIF.

## Tutoriales

Tutoriales sobre como conseguir funcionalidad en sus aplicaciones.

- [demo live de la API de Imagen de IIIF](http://yenda.tools/en/iiif-api-demo-en/) Aprenda sobre la estructura de una URL de IIIF manipulando sus parámetros y viendo los resultados en un demo live.
- [Guía de Implementación de IIIF](http://iiif.io/assets/acc_implementation_guide_011017.pdf)  Un recorrido paso-a-paso de como implementar IIIF.
- [Guía de Inicio Rápido de IIIF](http://iiif.io/technical-details/) es una rápida reseña de como podría empezar a implementar varios estándares de IIIF.
- [Arrastrar y Soltar](https://medium.com/@aeschylus/create-and-share-iiif-items-quickly-and-easily-with-drag-and-drop-over-email-879f13c9caba) una imagen de IIIF en Mirador.
- [Fellow Travelers: The Canterbury Tales and IIIF](http://web.stanford.edu/group/dmstech/cgi-bin/wordpress/author/blalbrit/) por Benjamin Albritton incluye una explicación del caso de uso de los estudiosos de la Edad Media usando a Chaucer como ejemplo, y una sección breve sobre como hacer un demo de comparación de páginas en Mirador.
- [Intro a IIIF (fr)](http://doc.biblissima-condorcet.fr/introduction-iiif) Introducción a IIIF (en francés).
- [Introducción a las APIs usando IIIF](http://www.meanboyfriend.com/overdue_ideas/2016/06/introduction-to-apis-using-iiif/) usa IIIF como ejemplo para explicar las APIs.
- [video sobre selección de imágenes](https://www.youtube.com/watch?v=4AJPVktQ1Zw) demostración de como un canvas puede tener una selección de varias imágenes, y un visor puede alternar entre las mismas.
- [Comenzando con IIIF](https://iiif.github.io/training/intro-to-iiif/) Introducción presentada originalmente durante un taller en la Conferencia Code4Lib de 2017, en Los Angeles, CA
- [Playground de la API de Imagen](https://www.learniiif.org/image-api/playground/) - Manera visual, basada en formularios, de explorar los parámetros de la API de Imagen.  Desarrollada para un curso en Georgia Tech por Jack Reed.
- [Taller de IIIF](http://ronallo.com/iiif-workshop/) - Un taller en línea que cubre los fundamentos de IIIF, incluyendo las APIs de Imagen y Presentación.

## Videos y Diapositivas

Diapositivas y videos acerca de IIIF.

- [Introducción a la API de Imagen](https://docs.google.com/presentation/d/1urCPiL3LffkIWglKGW4SSEiojBt2_RKmt5YuDtBoRfY/edit?usp=sharing) una reseña de alto nivel de los parámetros de la API de Imagen.
- [OA - Shared Canvas - TEI - Biblissima project](http://www.slideshare.net/biblissima/oa-shared-canvas-tei-biblissima-project) parte de un taller sobre TEI y estándares cercanos incluyendo IIIF.
- [IIIF Para Proyectos Pequeños](http://www.slideshare.net/workergnome/iiif-for-small-projects) como IIIF puede ser usado en proyectos pequeños con infraestructura limitada, presentado en [KeystoneDH 2016](http://keystonedh.network/2016/).
- [Introducción a la API de Presentación](http://www.slideshare.net/azaroth42/iiif-presentation-api) por Rob Sanderson.
- [Video del evento de IIIF en la National Gallery of Art](https://www.youtube.com/playlist?list=PLYPP1-8uH9c6iQpKTXnhnlQpmoMLT1fB7) en mayo de 2015.
- [Video del evento de alcance en el Museum of Modern Art](https://www.youtube.com/playlist?list=PLYPP1-8uH9c5smSD2wyVgsqKxD218khZq) en mayo de 2016.
- [Colección de diapositivas](http://www.slideshare.net/IIIF_io/clipboards) de varios eventos de IIIF.
- [Una Introducción al International Image Interoperability Framework](https://drive.google.com/file/d/0BwIq5pa1_rvfMnhCZmtzNTc5dnc/view) - Presentación que introduce IIIF a nuevas audiencias como "la API para humanos" - también contiene videos de otras presentaciones sobre IIIF.
- [Introducción a IIIF](https://drive.google.com/open?id=0B8APFBow4sHvNUNDQmp1Yko4VjQ) Extensa presentación que introduce IIIF con numerosos ejemplos y demos en video, Beijing, octubre de 2017.
- [Introducción a IIIF (alemán)](https://drive.google.com/open?id=1PQAuaTbkPzmJOMDxtihyS0-gbUtTTcDC) Una traducción al alemán de la presentación anterior.


## Descubrimiento

Enlaces para ayudar a descubrir recursos de IIIF que han sido compartidos, demostraciones de descubrimiento de IIIF, y herramientas de descubrimiento útiles.

- [iiif-universe](https://github.com/ryanfb/iiif-universe) es un repositorio que incluye enlaces a colecciones conocidas de manifests de presentación de IIIF.
- [demo de iNQUIRE](http://inquire.armtest.uk/) es un demo de una plataforma de investigación y descubrimiento de código abierto, compatible con IIIF. Esta es la versión compatible con IIIF de la plataforma de la [Digital Bodleian] (http://digital.bodleian.ox.ac.uk/).
- [código fuente de iNQUIRE](https://github.com/armadillo-systems/inquire) es el repositorio de Github para iNQUIRE.
- [Musiclibs](https://musiclibs.net) ofrece búsqueda entre librerías de miles de partituras musicales y manuscritos.

## Anotaciones

Aunque las anotaciones no son especificadas por IIIF, son una importante tecnología habilitadora.

- [Storiiies](http://storiiies.cogapp.com/) - Demos del uso de anotaciones para la narración.

### Servidores de Anotaciones

- [MangoServer](https://github.com/azaroth42/MangoServer) - Servidor de anotaciones respaldado por Mango, escrito en Python.
- [SimpleAnnotationServer](https://github.com/glenrobson/SimpleAnnotationServer) - Servidor de anotaciones Java, respaldado por un triple almacén de Apache Jena, Sesame, o Solr.
- [Elucidate](https://github.com/dlcs/elucidate-server) - Servidor de anotaciones de Java y Postgres.
- [ipfs-iiif-db](https://github.com/pgte/ipfs-iiif-db) - Cliente JS de anotaciones de IIIF sobre IPFS.
- [annotot](https://github.com/mejackreed/annotot) - Sencillas anotaciones de IIIF montadas en una aplicación Ruby on Rails.

## Integración a CMS

Módulos de Content Management Systems (CMS) que implementan o aprovechan las APIs de IIIF.

- [IIIF Image Field](https://www.drupal.org/sandbox/sdellis/2421047) - módulo de Drupal 7 que proporciona una manera fácil de añadir las imágenes de IIIF a los tipos de contenido, y configurar la presentación de las mismas. Soporta las versiones 1.0 o 2.0 de la API de Imagen.
- [UniversalViewer4Omeka](https://github.com/Daniel-KM/UniversalViewer4Omeka) - plugin de Omeka que implementa las APIs de IIIF (Imagen y Presentación) e integra el UniversalViewer en Omeka.

## Periódicos

Estos recursos son útiles específicamente en el trabajo con periódicos. Muchos de ellos son productos del [Grupo de la Comunidad de Periódicos de IIIF](http://iiif.io/community/groups/newspapers/).

- [Carpeta de Google Drive de Periódicos de IIIF](https://goo.gl/jNFfVw) tiene documentos en progreso del Grupo de Interés para actas de reuniones, y borradores en progreso de las mejores prácticas, etc.
- [Welsh Newspapers Online](http://newspapers.library.wales/) proporciona acceso a más de 1 millón de páginas de periódicos usando la API de Imagen de IIIF.
- Guía para [Periódicos de IIIF](http://dev.llgc.org.uk/wiki/index.php?title=IIIF_Newspapers) de la National Library of Wales ofrece una explicación y ejemplos de como IIIF es aplicable a los periódicos.
- [Poblando el Almacén de Anotaciones con la Lista de Anotaciones de IIIF](https://github.com/glenrobson/SimpleAnnotationServer/blob/master/doc/PopulatingAnnotations.md) contiene instrucciones sobre como editar texto OCR usando anotaciones en Mirador.
- [open-oni](https://github.com/open-oni/open-oni) es un amigable fork de [chronam](https://github.com/libraryofcongress/chronam), una webapp para visualizar datos del National Digital Newspaper Program de la Biblioteca del Congreso.
- [docker-open-oni](https://github.com/open-oni/docker-open-oni) es un setup compatible con Docker para open-oni, que instalará y configurará la aplicación web, así como MySQL, Solr, y el servidor de imágenes RAIS.
- [ndnp_iiif](https://github.com/umd-mith/ndnp_iiif) es un programa de Python para convertir [datos del National Digital Newspaper Program](https://www.loc.gov/ndnp/) en JSON estático de IIIF, listo para montar en la web.

## STEM

Science, Technology, Engineering, Math/Medicine - Ciencia, Tecnología, Ingeniería, Matemática/Medicina

- [CellXplorer](https://courses.edx.org/courses/course-v1:HarvardX+MCB64.1x+2T2016/d16e07a5cec442eeb7cd9dfcb695dce0/) - Anotaciones de biología celular en un visor de zoom profundo.

## Experimentos y Diversión

- [Puzzles! Basados en IIIF](http://puzzle.mikeapps.me/) - Puzzles de mosaico de imágenes, de arrastrar-y-soltar, creados por Michael Appleby, Yale Center for British Art.
- [Slider puzzles](http://blalbrit.github.io/puzzles) - Más puzzles de arrastrar-y-soltar, creados por Ben Albritton, Stanford University Libraries.
- [David Rumsey MapTab](https://chrome.google.com/webstore/detail/david-rumsey-map-collecti/fnheacjohhlddiffbmafmpoblbkfgmde?hl=en) - Una extensión de Chrome, basada en IIIF, que muestra un mapa aleatorio de la David Rumsey Map Collection cada vez que se abre una nueva pestaña en el navegador. Construído usando Leaflet-IIIF y React.js. Creado por Jack Reed, Stanford Univerity Libraries.
- [Fractals](http://showcase.iiif.io/showcase/fractals.html) - Zoom profundo en una enorme (mil millones x mil millones de píxeles) imagen fractal, creado por Sean Martin, Applied IIF. Vea también la [lista completa de fractales](http://www.appliediiif.org.uk/live/fractalshome.htm).
- [The Transcriptinator](http://labs.cogapp.com/transcriptinator/) - Un prototipo de "juego" creado para usar en la máquina arcade de crowd-sourcing de la British Library. Los jugadores tienen que señalar errores en las transcripciones OCR de contenido tomado de la [Qatar Digital Library](http://www.qdl.qa). Creado por Jon White y Tristan Roddis, Cogapp.
- [Galería IIIF](http://digirati-co-uk.github.io/iiif-gallery/src/) - Una galería de arte virtual que usa OpenSeadragon y generación personalizada de imágenes, creada por Stephen Fraser, Digirati. Vea también el [código fuente completo](https://github.com/digirati-co-uk/iiif-gallery/).
- [Exquisite Corpse](https://github.com/harvardartmuseums/exquisite-iiif-demo) - Un prototipo que mezcla retratos deliberadamente. Creado usando Node.js por Jeff Steward, Harvard Art Museums.
- [explorador 3D de tarjetas de comercio](http://labs.cogapp.com/tc/) - Un entorno 3D que muestra tarjetas de comercio del siglo XIX de la [Boston Public Library](https://www.digitalcommonwealth.org/collections/commonwealth:gq67jz045). Diseñado para ser visto en un teléfono móvil, idealmente con Google Cardboard. Creado usando three.js por Jon White, Cogapp.
- [Sleep Stories](http://bitly.com/wcquilt) - un experimento con el Web Annotation Data Model de W3C. Las anotaciones presentan una secuencia de historias asociadas a una imagen grande. Optimizado para móviles. Creado por Andrew Dyton y Stephen Fraser, Digirati, para la Wellcome Collection.
- [Comparación de Imágenes con un Deslizador](http://resources.digirati.com/iiif/an-introduction-to-iiif/dee-sbs.html) - Comparación de imágenes usando el deslizador de leaflet, por Digirati.
- [Comparación de Imágenes con una Lupa](http://resources.digirati.com/iiif/an-introduction-to-iiif/dee-mag.html) - Comparación de imágenes usando la lupa de leaflet, por Digirati.
- [X-raying Balenciaga](https://www.vam.ac.uk/articles/x-raying-balenciaga) - Bello uso de imágenes de IIIF para mostrar rayos X de la moda Balenciaga, por el Victoria & Albert Museum.
- [Storiiies](http://storiiies.cogapp.com/) - Exhibición de Cogapp de recientes experimentos de narración digital usando IIIF.
- [Old Map Room](https://itunes.apple.com/us/app/old-map-room/id1347431506) - Una aplicación de AppleTV que usa IIIF para convertir cualquier habitación en una sala de mapas.

## Comunidad

IIIF es una iniciativa basada en la comunidad que depende de la participación activa, discusión, y aportes. Para participar y saber más, vea la [página de la Comunidad de IIIF](http://iiif.io/community/).
- Únase a la [lista de correo electrónico IIIF-Discuss](https://groups.google.com/forum/#!forum/iiif-discuss).
- Lea los [boletines trimestrales de la Comunidad de IIIF](http://iiif.io/news/) para estar actualizado sobre las últimas actividades de la comunidad.
- [Envíe una noticia relacionada a IIIF](https://goo.gl/forms/2LMe9zUHVBEbI62C3) al Boletín de la Comunidad de IIIF.
- Contribuya a uno de los [grupos técnicos y/o comunitarios de IIIF](http://iiif.io/community/groups/).
- Participe en las convocatorias bisemanales de la Comunidad de IIIF. Vea el [calendario de la Comunidad de IIIF](http://iiif.io/community/groups/) para los detalles.
- Conozca más sobre el [IIIF Consortium](http://iiif.io/community/consortium/).
- Asista a un [evento de IIIF](http://iiif.io/event/).
- [iiif_io en Twitter](https://twitter.com/iiif_io).

## Licencia

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

Hasta donde es posible bajo la ley, todos los contribuyentes renuncian a sus derechos de copyright y relacionados para este trabajo.
