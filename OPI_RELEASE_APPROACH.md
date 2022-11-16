# OPI Release Approach

OPI will release some artifacts around the work being done in the
project. This document details *how* the artifacts are released, and how it
relates to the form the project takes, meaning this document is the result of a
[mailing list discussion](https://lists.opiproject.org/g/tsc/message/30)
around the OPI release process.

## Release Cadence

The OPI Project will strive to release code on a cadence of once every 6
months.

## Concrete OPI Release Approach

OPI will be releasing a set of artifacts, including an example architecture
and integration platform. **The example architecture and integration platform
are not meant to be used in production.**

The details of what this will look like are as follows:


* The protobuf files themselves
  * Some language specific bindings for those files. For example, bindings for
    C++, golang, python, and Rust
  * Documentation around the protobuf files
* An example implementation which implements the protobuf files
  * gRPC server code which incorporates the protobuf files
  * Implementation specific examples of the APIs themselves
    * SPDK for the Storage APIs
    * strongSwan for Security IPsec APIs
    * XDP program for the Security Firewall programs
  * gRPC client code to work with the server code
  * CLI based on the gRPC client code
* An integration and development platform
  * A containerized version of a DPU or IPU device
* A test suite and test plan
  * A test plan containing a list of tests for the covered OPI APIs
  * Integration tests which run not only on the integration platform above, but also
    will be run on vendor DPU and IPU devices
* Code related to provisioning and lifecycle:
  * OTEL integration points
  * sZTP code, including a custom client
* A Container Storage Interface (CSI) library, client and helpful
  utilities called [goopicso](https://github.com/opiproject/goopicsi)
* A behavioral model representing a DPU/IPU, against which all APIs/code will
  be implemented.

OPI is tracking work in the following specific areas, which will each contain
pieces of the above release artifacts:

* AI/ML
* Networking
* Storage
* Security

### Working Group Specific Release Items

* [Storage](https://github.com/opiproject/opi-api/tree/main/storage#deliverables)
* [SZTP agent/client](https://github.com/opiproject/sztp/releases)
* [GoOPICsi library](https://github.com/opiproject/goopicsi/releases)

The above example allows for vendors to release their own bindings for
the APIs as well. For example:

* OPI AMD/Pensando
* OPI Intel
* OPI Marvell
* OPI NVIDIA

The above list is not meant to be inclusive of all DPU and IPU vendors,
but merely an example of some vendors showing how they could release
bindings for OPI APIs.

We also propose these bindings are created in repositories in the
[OPI Github](https://github.com/opiproject). However, if a vendor wants to
use their own GitHub organization for the repository, they are free to do
that as well.

We will version the releases using [semantic versioning](https://semver.org).

### Testing and the Release Plan

All of the OPI APIs will be tested using the
[OPI PoC Integration](https://github.com/opiproject/opi-poc/tree/main/integration)
platform for both developer testing as well as verification. Each time a new
API is added, the API will need to be implemented in the integration test
suite in the OPI PoC repository.

OPI will also produce a test plan, including a set of conformance tests, which
each vendor is recommended to run against their HW DPU or IPU devices
running the OPI APIs. The vendors will then be encouraged to upload those
test results to a webpage containing a table of all the vendor results.
These tests will also run on each commit to relevant GitHub repositories
using the integration test suite in the OPI PoC repository.
