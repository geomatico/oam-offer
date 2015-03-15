Common projects
===============

Despite Micho and Oscar work as independent freelance developers, they have worked together in many occasions. Some common developments:


Integrated Carbon Observation System Data Portal
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A dataportal to help climate change scientific research community. The general architecture is very similar to what we need for OAM Catalog:

1. A data repository: collection of NetCDF files, made available through Thredds Data Server.
2. An indexed catalog: customized GeoNetwork instance harvesting and indexing the former repository metadata.
3. A search & preview web interface: simple search form with text + bbox + timerange filters; paged results with in-browser data preview; "shopping cart" where to add the desired datasets for full download in original format.

Built on existing Open Source products (Thredds, GeoNetwork, Lucene, OpenLayers, ExtJS), we put the glue and fine-tunning.

Developed by Micho Garcia, Oscar Fonts and Fernando Gonzalez at geomati.co. Presented at various FOSS4G european conferences (Spain, Netherlands, UK):

* Article and Slides: http://dugi-doc.udg.edu/handle/10256/4196
* Demo video: https://vimeo.com/44806500
* GitHub repo: https://github.com/geomatico/dataportal
* Documentation (spanish): http://geomati.co/dataportal/


Geotalleres
^^^^^^^^^^^

Geotalleres is a compilation of reusable spanish language workshop materials for Open Source Geospatial training. It's a collective creative-commons knowledge base. Micho and Oscar contributed various initial PostGIS and GeoServer chapters.

* GitHub repo: https://github.com/geotalleres/geotalleres


SatAgro
^^^^^^^

A Satellite Information Service for farmers. Including:

#. Backend scripts to extract significative indicators for farmers (timeseries and time-dependant raster layers) out of free MODIS and Landsat imagery. Mainly via `Python GDAL`_ scripting and `OpenForis`_.
#. Automatic raster data publishing in GeoServer through REST API, using `gsconfig` python client.
#. A browsable REST API using `Django Rest Framework`_.
#. A web application structured with Backbone and RequireJS, and using Bootstrap, Leaflet and Highcharts.

* Demo site (dev version, not production ready): https://dev.satagro.pl

.. _Python GDAL: http://gdal.org/python/
.. _OpenForis: http://www.openforis.org/
.. _gsconfig: https://github.com/boundlessgeo/gsconfig
.. _Django Rest Framework: http://www.django-rest-framework.org/



GeoPoster
^^^^^^^^^

Distributed map edition: markers and rich text descriptions. Wants to be like having a map on the wall where a group of people can stick pins and add notes effortlessly.

Techncally, an exercise to:

* Completely separate JS Client from REST API;
* Conceive the simplest possible UI with in-line rich text and map editing;
* Use Flask Python microframework.

* API: https://github.com/geomatico/geoposter/tree/master/geoposter-api
* UI: https://github.com/geomatico/geoposter/tree/master/geoposter-client


Mapa Literari Català
^^^^^^^^^^^^^^^^^^^^

Not a techically complex application, but a very popular one. Links literature and territory, proposing different routes related to classical witers' texts.

Oscar optimized the web application, separating the UI from the Data Acces, and replacing Google Maps with Leaflet. Django + PostgreSQL in the server, jQuery and Leaflet the browser. Micho developed the `Android app`_ and `iOS app`_ using Cordova for multiplatform development.

.. _Web: http://mapaliterari.cat
.. _Android app: https://play.google.com/store/apps/details?id=co.geomati.mapaliterari
.. _iOS app: https://itunes.apple.com/cn/app/mapa-literari-catala/id882530151?l=en&mt=8
