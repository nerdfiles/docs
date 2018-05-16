.. _modules:

Openchain modules
=================

Openchain uses an extensible architecture where modules can be swapped in and out depending on the functionality needed. Modules are selected by:

- Referencing the appropriate package in the ``project.json`` file. Packages are then pull automatically from NuGet.
- Referencing the module in ``config.json``.

This document lists the available modules, and relevant packages.

Storage engines
---------------

Storage engines are core components responsible for storing the transaction chain and records.

=================  ===========================================================================   ================================================================  ====================================================================
Provider           Module                                                                        Description                                                       Maintainer
=================  ===========================================================================   ================================================================  ====================================================================
``SQLite``         `Openchain.Sqlite <https://www.nuget.org/packages/Openchain.Sqlite>`_         Stores the chain in a local Sqlite database.                      `Coinprism <https://github.com/openchain/openchain>`_
``MsSQL``          `Openchain.SqlServer <https://www.nuget.org/packages/Openchain.SqlServer>`_   Stores the chain in a SQL Server database.                        `Coinprism <https://github.com/openchain/openchain>`_
``MongoDB``        Openchain.MongoDb                                                             Stores the chain in a MongoDB database.                           `@fluce <https://github.com/openchain/mongodb-storage>`_
=================  ===========================================================================   ================================================================  ====================================================================

Validation engines
------------------

Implement Hypermedia Service Architecture ([HSA][hsa], Hypermedia-first Modeling) such that hypermedia is the engine of application state.

Anchoring media
---------------

Implement [Linked Data][ld]. 

<blockquote><p>While the ODRL Information Model is built using Linked Data principles, the design is intended to allow non-graph-based implementations.</p><sup>1</sup></blockquote>

____
<sup>1</sup> https://w3c.github.io/poe/model/#aimsModel

[hsa]: http://www.amundsen.com/talks/2016-04-sacon-patterns/2016-04-sacon-patterns.pdf
[ld]: https://github.com/WebOfTrustInfo/rebooting-the-web-of-trust-fall2016/blob/master/topics-and-advance-readings/blockchain-extensions-for-linked-data-signatures.md#blockchain-anchoring
