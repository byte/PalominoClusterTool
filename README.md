Palomino Cluster Tool
=====================

A tool for creating large database clusters quickly. The goal is to allow an
organisation to build realistically-sized distributed database clusters in a
matter of hours instead of days. Once the cluster is built, you should be able
to evaluate the cluster properly by running benchmarks on it and having proper
instrumentation to be able to reason logically about the performance of the
cluster.


How to Use It
=============

   1. Allocate cluster nodes, ensure passwordless SSH user with sudo is
      available to your Management machine.
   1. Decide your distribution, cluster configuration software, and database
      architecture.
   1. Enter [ConfigManager]/[Distribution] directory, edit INI and YAML files
      (this will take the longest time). Some available choices are:
      1. AnsiblePlaybooks/Ubuntu-12.04
      1. ChefCookbooks/CentOS
   1. Ask PalominoClusterTool to generate your cluster.
   1. Join the mailing list
      (https://groups.google.com/d/forum/palomino-cluster-tool) and IRC channels
      to report errors or concerns, and to discuss with other professionals.


What is it?
===========

At its core, the Palomino Cluster Tool is simply a set of playbooks, recipes,
and manifests for setting up complex database clusters. There are some simple
scripts to help it coordinate with your cluster management tool.

One goal is to make sure that once your cluster is set up, there is trending
and alerting set up for the cluster. It is difficult to evaluate the
performance of a database unless it is instrumented properly.

The project is by necessity somewhat large and complex. There are three major
configuration management systems, three major Linux OS distributions, and three
very desireable cluster layouts. That's 27 different sets of complex scripts
that need to be generated. If your desired OS/CMS/ClusterType isn't
represented, please join the mailing list and/or IRC to discuss it. There may
be others with the same needs, or who are already working on it.

There is a set of slides on the various architectures to be supported, hopeful
timelines, and project architecture here:
http://dev.palominodb.com/time_public_html/PalominoDBClusterTool/.


Prerequisites
=============

You need a cluster management tool: Ansible, Chef, or Puppet for example. The
end goal of the Palomino Cluster Tool remains the same, you should be able to
set up the distributed database in hours, so if you do not have one of these
tools set up, we recommend beginning with Ansible since it is the simplest.


Authors
=======

Help is solicited! If you've written Chef Recipes or Puppet Manifests for
setting up clusters of MySQL, HBase, Cassandra, MongoDB, or other distributed
database systems, please contact us! We'd love to hear about it and welcome
your participation in the project.

   * Tim Ellis, CTO & Principal Architect, Palomino - Project Leader
   * René Cannaò, Senior DBA, Data Architect, Palomino
   * Charlie Killian, Director of Engineering, Palomino
   * Cliff Erson, Riot Games
   * Jamie Winsor, Riot Games
   * Istvan Szukacs, Riot Games


License
=======

The project and all related scripts, playbooks, manifests, recipes are
Copyrighted works by the respective authors (noted in the source files
themselves) and distributed under the terms of the Apache License, version 2.0.

