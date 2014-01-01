<!---
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

<head>
  <title>Home</title>
</head>


## Apache Helix

Apache Helix is a generic _cluster management_ framework used for the automatic management of partitioned, replicated and distributed resources hosted on a cluster of nodes. __Helix automates reassignment of resources in the face of node failure and recovery, cluster expansion, and reconfiguration.__


## What Is Cluster Management?

To understand Helix, you first need to understand __cluster management__. A distributed system typically runs on multiple nodes for the following reasons:

* scalability
* fault tolerance
* load balancing

Each node performs one or more of the primary functions of the cluster, such as storing and serving data, producing and consuming data streams, and so on. __Once configured for your system, Helix acts as the global brain for the system__. It is designed to make decisions that cannot be made in isolation.  Examples of such decisions that require global knowledge and coordination:

* scheduling of maintainence tasks, such as backups, garbage collection, file consolidation, index rebuilds
* repartitioning of data or resources across the cluster
* informing dependent systems of changes so they can react appropriately to cluster changes
* throttling system tasks and changes

While it is possible to integrate these functions into the distributed system, it complicates the code. Helix has abstracted common cluster management tasks, enabling the system builder to model the desired behavior with a declarative state model, and let Helix manage the coordination. __The result is less new code to write, and a robust, highly operable system__.

## What does Helix provide?

* Automatic assignment of resources and partitions to nodes
* Node failure detection and recovery
* Dynamic addition of resources
* Dynamic addition of nodes to the cluster
* Pluggable distributed state machine to manage the state of a resource via state transitions
* Automatic load balancing and throttling of transitions
* Optional pluggable rebalancing for user-defined assignment of resources and partitions


## Why Helix?

Modeling a distributed system as a state machine with constraints on states and transitions has the following benefits:

* Separates cluster management from the core functionality of the system.
* Allows a quick transformation from a single node system to an operable, distributed system.
* Increases simplicity: system components do not have to manage a global cluster.  This division of labor makes it easier to build, debug, and maintain your system.

---

### News

Apache Helix has two new releases:

* [0.6.2-incubating](./site-releases/0.6.2-incubating-site/index.html) - A release that fixes numerous bugs and improves platform stability.

    [\[Quick Start\]](./site-releases/0.6.2-incubating-site/Quickstart.html) [\[Release Notes\]](./releasenotes/release-0.6.2-incubating.html)

* [0.7.0-incubating](./site-releases/0.7.0-incubating-site/index.html) (alpha) - A release that includes high-level APIs to logically interact with Participants, Controllers, Resources, and other Helix constructs. __This release is an alpha and APIs are in the process of being finalized__. Feel free to play with it and provide any feedback you have!

    [\[Quick Start\]](./site-releases/0.7.0-incubating-site/Quickstart.html) [\[Release Notes\]](./releasenotes/release-0.7.0-incubating.html)

### Download

<a href="./site-releases/0.6.2-incubating-site/download.html" class="btn btn-primary btn-small">0.6.2-incubating</a>

<a href="./site-releases/0.7.0-incubating-site/download.html" class="btn btn-primary btn-small">0.7.0-incubating (alpha)</a>

### Maven Dependency

```
<dependency>
  <groupId>org.apache.helix</groupId>
  <artifactId>helix-core</artifactId>
  <version>0.6.2-incubating</version>
</dependency>
```

### Building

Requirements: JDK 1.6+, Maven 2.0.8+

```
git clone https://git-wip-us.apache.org/repos/asf/incubator-helix.git
cd incubator-helix
git checkout helix-0.6.2-incubating
mvn install package -DskipTests
```

### Get Help

[#apachehelix](./IRC.html)

`user@helix.incubator.apache.org`
