# JBoss GossipRouter Docker image

This is an example Dockerfile that deploys a JBoss JGroups GossipRouter.

This can be used with TCPGOSSIP discovery to handle docker container deployments of JBoss with dynamic IP addresses.

This is important when trying to deploy Docker based JBoss clusters in cloud IaaS like AWS which are not multicast capable.

This image is built on the [jboss/immutant](https://registry.hub.docker.com/u/jboss/immutant/) docker image.

This could easily be adapted to use any of the other [JBoss dockerfiles](https://github.com/jboss/dockerfiles/).

## Usage

    docker run -it -p 12001:5000 ianblenke/jboss-gossiprouter

## Building on your own

You don't need to do this on your own, because there is an [automated build](https://registry.hub.docker.com/u/ianblenke/jboss-gossiprouter/) for this repository, but if you really want:

    docker build --rm=true --tag=ianblenke/jboss-gossiprouter .

## Source

The source is [available on GitHub](https://github.com/ianblenke/jboss-gossiprouter/).

This is a _very_ simple Dockerfile. Please fork it and make improvements.

