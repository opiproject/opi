# OPI Blueprint

Framework & FAQ

Prepared by WorldTech IT for the OPI Technical Steering Committee.\
Josh Brooks, Chief Solutions Architect  |  josh\@worldtechit.com

## What is an OPI Blueprint (Intent and Goals)?

An OPI Blueprint is an example architecture that shows how to
operationalize an open source component within the OPI ecosystem. Rather
than presenting raw code, APIs, or RFC specifications, a Blueprint takes an
OPI-supported technology and demonstrates a practical, real-world
deployment pattern that an enterprise customer or systems integrator could
replicate. **The intent is to:** **Accelerate adoption** by bridging the
gap between OPI’s open source projects and production-ready deployments.
Customers don’t buy RFC adoption—they buy outcomes. **Showcase the value of
DPU/IPU technology** in offloading complex networking, security, and
storage functions to dedicated hardware, freeing host CPU cores for
higher-value workloads. **Drive services engagement** by pairing the
Blueprint with the integrator or partner who built it, so that enterprises
interested in deploying the solution have a clear path to professional
services, support, and hardware procurement. **Strengthen the OPI vendor
ecosystem** by demonstrating multi-vendor interoperability across hardware
(Dell, Intel, Marvell), software (F5 BIG-IP Next, NGINX, Red Hat
OpenShift), and infrastructure automation (Terraform, Ansible).

## What constitutes a Blueprint (Deliverables)?

A complete Blueprint should include the following deliverables: **Reference
Architecture Diagram** – A visual topology showing the hardware, software,
and network components and how they interconnect. This should be
understandable by a solutions architect or IT decision-maker, not just a
developer. **Bill of Materials (BOM)** – A list of validated hardware
(e.g., Dell chassis, Intel IPU E2100), software versions (e.g., RHEL 9.x,
BIG-IP Next for K8s), and any licensing requirements. **Deployment Guide**
– Step-by-step documentation covering installation, configuration, and
validation. Should include infrastructure-as-code artifacts (Terraform
modules, Ansible playbooks, Helm charts, YAML manifests) where applicable.
**Use Case Narrative** – A description of the business problem the
Blueprint solves, the target persona (e.g., network architect, platform
engineer, CISO), and why IPU/DPU offload matters for this workload.
**Validation/Test Results** – Evidence that the Blueprint works as
documented. This could include performance benchmarks, screenshots, or
recorded walkthroughs. **Partner/Integrator Attribution** – Clear branding
and contact information for the contributing partner(s), so that
end-customers who want to deploy the solution know exactly who built it and
who can help them operationalize it in their environment.

## How is it different from a Technical Demo?

A Technical Demo proves that a technology works. A Blueprint shows how to
put it into production. **Dimension** **Technical Demo** **Blueprint**
**Audience** Developers, project contributors Solutions architects, IT
decision-makers, enterprise customers **Purpose** Validate that the OPI
API/framework functions correctly on target hardware Show a complete,
deployable solution pattern with real-world applicability **Scope** Single
feature or integration point (e.g., NGINX proxy on a Marvell OCTEON DPU)
End-to-end architecture including HW, OS, orchestration, networking, and
application layers **Depth** Often tied to RFCs, API specs, and low-level
implementation details Focused on operational readiness: how to deploy,
manage, and scale **Output** Working proof-of-concept, often ephemeral or
lab-only Documented reference architecture with IaC artifacts, BOM, and
deployment guide **Reusability** Limited – typically requires deep OPI
expertise to reproduce High – designed so an integrator or customer can
replicate independently **Branding** OPI project branding only OPI \+
contributing partner branding (e.g., WorldTech IT, Dell, Red Hat) *In
short: Technical Demos live in the world of development and validation.
Blueprints live in the world of adoption and services. The Demo answers
“does it work?” The Blueprint answers “how do I deploy this at my
company?”*

## How do Blueprints tie-in to OPI?

Blueprints are the adoption arm of the OPI Project. The OPI Project’s core
mission is to create a vendor-neutral, open source framework of APIs and
tools for managing IPUs and DPUs. That work produces standardized
interfaces, reference implementations, and tested integrations—but it
doesn’t inherently show an enterprise customer how to operationalize those
components. Blueprints close that gap by: **Consuming OPI APIs and tools**
in validated, end-to-end architectures that prove multi-vendor
interoperability. **Providing the “last mile”** between OPI’s open source
projects (opi-api, sztp, DPU Operator) and what a customer actually needs
to stand up in their data center. **Creating a feedback loop** where
real-world deployment patterns surface gaps or enhancements needed in the
OPI framework itself (e.g., the recent TSC discussion around a
supportability audit and DPU/IPU hardware status matrix). **Engaging OPI
member vendor ecosystems** (Dell, Intel, Red Hat, F5, Marvell) by
demonstrating their products working together under the OPI umbrella, which
strengthens the business case for continued investment in the project.

## I have a Blueprint Idea, what should I do next?

Great—here’s the recommended process: **Draft a one-pager.** Describe the
use case, target audience, which OPI components it exercises, the
hardware/software stack, and who the contributing partner(s) would be. Keep
it concise—this is a pitch, not a design doc. **Bring it to the TSC.**
Present the one-pager during a TSC meeting. The TSC will evaluate whether
it aligns with the project’s priorities, whether the required lab resources
are available, and whether there are any overlaps with existing work. **Get
resource alignment.** Confirm who is contributing engineering time, whether
the OPI Lab has the necessary hardware provisioned (this has historically
been a bottleneck), and agree on a realistic timeline with guard rails
around time commitment. **Build, document, and validate.** Stand up the
solution in the OPI Lab (or a contributing partner’s lab), capture all
deliverables (architecture diagram, BOM, deployment guide, test results),
and ensure branding/attribution is in place. **Publish and present.** Once
validated, the Blueprint gets published to the OPI Lab/repository and can
be showcased at events (OCP Global Summit, GTC, Red Hat Summit, etc.) and
through OPI marketing channels. |

## How can end-customers benefit from the Blueprints?

End-customers benefit in several concrete ways: **Reduced time-to-value.**
Instead of figuring out how to piece together IPU/DPU infrastructure from
scratch, customers can start with a validated reference architecture and
adapt it to their environment. **Vendor-neutral confidence.** Because
Blueprints are built on OPI’s open standards, customers aren’t locked into
a single vendor’s proprietary stack. They can swap components (e.g.,
different DPU hardware) while keeping the same deployment pattern. **Clear
path to professional services.** Each Blueprint identifies the
partner/integrator who built it. If a customer wants help deploying or
customizing the solution, they know exactly who to call. This is especially
valuable for enterprises that need a trusted integrator to handle complex
IPU/DPU deployments. **TCO visibility.** The BOM and architecture diagram
give customers a concrete understanding of what they need to procure and
what the deployment footprint looks like, making it easier to build a
business case internally. **De-risked evaluation.** Blueprints that are
live in the OPI Lab can be demonstrated or even trialed, giving customers a
way to see the solution working before committing budget.

## Where do these Blueprints reside? OPI Lab?

Blueprints have both a physical and digital home: **OPI Lab
(Physical/Virtual).** The Linux Foundation-hosted OPI Lab is the primary
environment where Blueprints are built and validated. This is where the
actual hardware (IPUs, DPUs, servers) lives and where live demonstrations
can be run. Contributing partners may also host complementary lab
environments to accelerate development when OPI Lab provisioning timelines
are a constraint. **OPI GitHub Repository (Digital).** All Blueprint
documentation, IaC artifacts, deployment guides, and architecture diagrams
should be published to the OPI project’s GitHub (e.g., under opi-poc or a
dedicated blueprints repository). This ensures they are version-controlled,
community-accessible, and can be maintained over time. **OPI Website /
Marketing Channels.** High-level summaries and architecture diagrams should
also be published to OPI’s public-facing channels so that potential
adopters can discover them without digging through GitHub. *The key
principle: a Blueprint should be reproducible by anyone with the right
hardware and the published documentation. It should not require access to a
specific lab instance to understand or replicate.*

## Does OPI have a preference for one Blueprint over the other?

OPI does not mandate a ranked priority list, but there are practical
factors that make some Blueprints more strategically valuable than others:
**Multi-vendor interoperability.** Blueprints that demonstrate OPI working
across multiple member vendors’ hardware and software (e.g., Dell chassis
\+ Intel IPU \+ F5 BIG-IP Next \+ Red Hat OpenShift) are highly valued
because they reinforce OPI’s core value proposition of vendor neutrality.
**Actively maintained components.** The TSC is currently working through a
source audit and supportability assessment to understand which OPI
components are actively maintained and on what hardware. Blueprints built
on well-supported components with clear community or vendor backing will be
prioritized. **Customer demand signal.** Blueprints that address use cases
with known enterprise demand—such as zero-touch provisioning, multi-tenant
isolation on IPU/DPU, or Kubernetes-native network function offload—will
naturally get more traction and support. **Partner commitment.** A
Blueprint with a committed contributing partner who will invest engineering
time, maintain the documentation, and stand behind the solution as a
services provider carries more weight than an idea without resourcing.
*Bottom line: the best Blueprint is one that solves a real customer
problem, uses actively maintained OPI components on validated hardware,
involves multiple OPI member vendors, and has a committed partner behind it
ready to support adoption.*
