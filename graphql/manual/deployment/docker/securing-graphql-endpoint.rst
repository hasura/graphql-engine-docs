Securing GraphQL endpoint
=========================

To make sure that your Hasura GraphQL endpoint is not publicly accessible, you need to configure an access key.

Note: If you're looking at adding authentication and access control to your GraphQL API then head to :doc:`Authentication / access control <../../auth/index>`.

Run the docker command with an access key flag
----------------------------------------------

.. code-block:: bash
   :emphasize-lines: 7

    #! /bin/bash
    docker run -p 8080:8080 \
     hasura/graphql-engine:latest \
     graphql-engine \
     --database-url postgres://username:password@hostname:port/dbname \
     serve
     --access-key mysecretkey
