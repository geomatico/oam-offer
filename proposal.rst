Technical Proposal
==================

We could go for the mature Open Source Geospatial Catalog implementation: GeoNetwork. With some Lucene indexing tweaks it can be adapted to specific search needs. We have `done it in the past <http://geomati.co/dataportal/search-service.html#configuracion-de-gn-para-busqueda-por-variables>`_.

But we would first bet for the recently graduated PyCSW project backed by SQLite. Start as simple as possible, and increase complexity only if/when neeed.

Tasks:

#. Generate some sample metadata records for testing, following the proposed `OAM metadata model <https://github.com/hotosm/OpenAerialMap/wiki/Metadata>`_. Probably this exercise will help refine the model proposal.
#. Deploy a PyCSW instance incorporating the sample records.
#. Deploy a first viewer such as the `PyCSW viewer demo <http://demo.pycsw.org/viewer/index.html>`_.

No puedo...

---

Description of your proposed tech challenge solution (max 2 pages), explaining the technology and design of choice for implementing the catalog and the user interface. Please also include a brief description of strategies that you will employ to ensure project code sustainability (see section 8 below for more details);

3. Scope of Work

The scope of work (SoW) for this challenge is to build the OAM catalog and integrate it with other OAM components. The selected candidates shall perform the following tasks:

Review existing open source catalog solutions and identify code that can be reused and adapted for developing the OAM catalog.
Implement the OAM API for communication between project components
Design and develop the system by integrating a backend database, a fast lightweight catalog, and a graphical Web user interface for searching and displaying imagery datasets 
Develop “potentially-shippable” versions of the OAM Catalog every month
Participate in the integration of the OAM Catalog with the OAM Server
Create comprehensive and clear documentation for code and API
Implement testing, metrics, and code sustainability strategies
Development will employ agile methods such as scrum, with iterative and incremental working product releases. The selected candidates will interact with the OAM community, integrating contributions by volunteer coders and participating in monthly code sprints. The OAM project manager will seek feedback from OAM users, organize and prioritize issues for developers to work on during each sprint.

Key requirements to be considered in developing the OAM Catalog are:

Maximum effort to reuse code and integrate with existing open source projects
Lightweight with small footprint even if installed on portable hardware (e.g. i5/i7 laptop)
Limited and focused to handling raster imagery data, with an effort to reduce overhead from features of reused code that are not needed for OAM
Self-contained, portable, with simple installation steps (e.g. through deployment with software containers or by virtualization) for compatibility with multiple operating systems
Developed using interoperable and modern programming languages
Scalable, to support increased workload of peak request periods (e.g. during a disaster emergency) and able to quickly replicate across multiple instances.

4. Deliverables

Code and documentation will be created and hosted in GitHub in a HOT organization repository. Two major releases of the OAM Catalog are expected during the contract:

OAM Catalog V1: released by the end of the second month, it will include a functional prototype with a well documented API, connecting to local metadata and imagery sources, and a complete Web user interface.

OAM Catalog V2: released by the end of the fourth month, it will include complete integration with other OAM components, ability to connect with any imagery tile service and other OAM nodes, packaged installers, tested scalable architecture, and complete documentation.

8. Project Sustainability

One important objective of this tech challenge is to create a final product that is well documented and coded according to best practices standards. We prefer technology and software that have large developer pools in the open source community. We invite candidates to review current HOT projects on GitHub and get familiar with technology already used, in order to maximize support by the community and make it easier for other volunteers to contribute. It is important that once this tech challenge contract ends, the HOT community is able to continue supporting and developing the project.


References
----------

The Request:
http://hot.openstreetmap.org/get_involved/openaerialmap_catalog_tech_challenge

Some Info:
http://hotosm.github.io/OpenAerialMap/oam-components/oam-c/

Discussion:
https://github.com/hotosm/OpenAerialMap/issues
https://groups.google.com/a/hotosm.org/forum/#!forum/openaerialmap

The old discontinued OAM project:
https://github.com/oam/oam
