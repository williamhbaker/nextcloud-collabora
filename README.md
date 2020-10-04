### Self-Hosted Nextcloud and Collabora

This is a docker-compose file for running Nextcloud along with Collabora.  It's like a self-hosted google drive.

**Details:**

- Uses Traefik for service routing, with Let's Encrypt integration to enforce secure connections over TLS.
- Uses Postgres for the RDBMS.
- Dynamic DNS service is provided by DuckDNS.

For the above to work properly, you will need to be set up with Let's Encrypt and DuckDNS.  Alternate DDNs providers should be viable as well, but would require different configuration.  Everything runs in docker containers, so familiarity with docker in addition to the above mentioned applications will be helpful.

**Installation**

You will need docker and docker-compose.  Then, make a copy of the `.env-template` file and rename it to `.env`.  This file defines the environment variables that the docker-compose will use.  Edit the `.env` file per the annotations in the file itself.

Move the `docker-compose.yml` and `.env` file to wherever you want the "root" directory of your nextcloud data to be.  Then, from that directory, use `docker-compose up -d` to start the stack.

After Nextcloud has started up, configure it as you wish.
