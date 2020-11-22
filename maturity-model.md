<!-- Copy and paste the converted output. -->

<!-----
NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 0.532 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β29
* Sun Nov 22 2020 13:32:25 GMT-0800 (PST)
* Source doc: 2020-11-22 CNCF Landscape Proposal
* Tables are currently converted to HTML tables.
----->



# CNCF Landscape, Trail Map and Maturity Model Proposal

The Cloud Native Landscape and the Trail Map are two useful tools for the CNCF and the wider Cloud Native community.  One plots a way forward, and the other brings the wider ecosystem together within broad categories.  The use of a maturity model will be a useful aid allowing organisations and individuals to build up their core competencies in Cloud Native, and drive up their maturity.

There are at least two different users of the Landscape and Trail Map.  The first use belongs to the persona of an Architect or an end-user organisation wishing to build up skills, and experience in Cloud Native.  This can be described as _maturity_.  This use of the Trail Map and Landscape can be considered the _strategic_ use-case for the two tools.

The second use of the Landscape is a more tactical approach and could be thought of as _what are the projects and products available for my purpose?_  Rather than being focussed on higher-level planning, it can be used to answer questions such as _“I need a service mesh, what are my options?”_  This usage of the Landscape is much more focussed helping to surface the projects and products that might help with a given need by the end user.


### Use-case/Persona 1:  Strategy and plotting maturity


#### The Trail Map

The Trail Map is a useful tool to explain to people where to start on the Cloud Native journey.  It starts with containerisation, then number two we have CI-CD.  Third, we then see Kubernetes, Helm, and afterwards we build on this with domains such as service mesh, storage, as well as security, with CNCF projects clearly illustrated.


#### The Landscape

The Landscape’s advantage is that it illustrates projects and products with simple criteria such as whether it is a CNCF project, what category the tools is in such as _Runtime_, _Orchestration & Management, Serverless _or _Observability and Analysis_.  It also clarifies whether a project is a CNCF member project, and whether the organisation proposing the product is a CNCF member or not, along with the license used by each respective project or product.  Finally it also discloses GitHub stars, funding and market capitalisation.


#### Introducing the Maturity Model

The Trail Map and Landscape lend themselves to a maturity model where the path followed is like that in the Trail Map.  Initially the end-user starts with a traditional infrastructure and applications, and looks to refactor and transform their environment to become Cloud Native.  This follows a maturity process, as the user first steps out with the basic or core requirements for Cloud Native, such as containerisation, initial Kubernetes deployments, and then further iterates this, moving on eventually to declarative deployment with full observability, incorporating service meshes, with all platform and infrastructure needs automated and in code.

The Trail Map’s usefulness is that it illustrates a path that organisations can start to follow and so is a little prescriptive.  Building on the concept of a _[maturity model](https://martinfowler.com/bliki/MaturityModel.html)_, from Martin Fowler, and the work of Gary Stafford with his Infrastructure Maturity Model [here](https://medium.com/@GaryStafford/infrastructure-as-code-maturity-model-9206b21d5dad), we can consider building a Cloud Native Maturity Model that brings further subtlety and nuance to the various technical categories that the Landscape contributes.  The Trail Map provides a 50,000 foot view, and a maturity model can start to help break it down into detail, and allows for the ability for an organisation or user to _describe_ and understand where they are at.

A proposal for a CNCF maturity model could look like the following:


<table>
  <tr>
   <td>Landscape Categories
   </td>
   <td>Legacy
   </td>
   <td>Traditional
   </td>
   <td>Contemporary
   </td>
   <td>Cloud Native
   </td>
   <td>Cloud Native Future
   </td>
  </tr>
  <tr>
   <td>Provisioning
   </td>
   <td>Manual deployment of applications, inconsistent software packaging. Perimeter based network access alone. Poor security practices posing high degree of risk. Little use of encryption and high barrier to security.
   </td>
   <td>Applications packaged for server and end-user deployment. Physical firewalls and course network zoning. Certificate Authorities in use, but not necessarily widely used.
   </td>
   <td>Release tooling may be used for deployment. Adoption of container registries, and declarative solutions for infrastructure as a service. Microsegmentation in use where necessary with identity and access control. Least trust principle in use, along with auditing. Secure management of secrets
<p>
<strong>CNCF Projects: Harbor</strong>
   </td>
   <td>Full end-to-end CI and CD pipeline with frequent releases and platform/infrastructure code delivered with application code. Immutable infrastructure in use, including eg. Cluster API. Policy prescribed and actively controlled, supply chain integrity assured and runtime security monitoring. Automated application security testing during app integration. Policy-based control for stack (eg. OPA). All stack components able to take advantage of Security and Compliance tooling, including output of observability domain.
<p>
<strong>CNCF Projects: Open Policy Agent, Falco, TUF, Notary</strong>
   </td>
   <td>Wide adoption of eBPF-based tooling for wide scale analysis
   </td>
  </tr>
  <tr>
   <td>Runtime
   </td>
   <td>Single server instances, often platforms do not meet availability requirements with often significant downtime cost.
   </td>
   <td>Hardware infrastructure-based solutions to cater for non-functional requirements. Reliance on proprietary APIs for configuration
   </td>
   <td>IaaS platform with virtual machines and appliances. Increasing adoption of open APIs for configuration. Initial adoption of SDN
<p>
<strong>CNCF Projects: containerd</strong>
   </td>
   <td>Transition to software-based stack with full programmability of platforms and infrastructure. Full use of service meshes and container orchestration
<p>
<strong>CNCF Projects: Kubernetes, Linkerd</strong>
   </td>
   <td>Multicloud mesh
   </td>
  </tr>
  <tr>
   <td>Orchestration and Management
   </td>
   <td>Single server instances, often platforms do not meet availability requirements with often significant downtime cost.
   </td>
   <td>Hardware infrastructure-based solutions to cater for non-functional requirements. Reliance on proprietary APIs for configuration
   </td>
   <td>IaaS platform with virtual machines and appliances. Initial adoption of Kubernetes. Increasing adoption of open APIs for configuration
   </td>
   <td>Full use of software-based stack with full programmability of platforms and infrastructure. Full use of service mesh, and ingress controllers, and scaling out with distributed storage and database.
<p>
<strong>CNCF Projects: Rook, Vitess</strong>
   </td>
   <td>Kubernetes at the edge
   </td>
  </tr>
  <tr>
   <td>Application Development and Definition
   </td>
   <td>Ad-hoc solutions combined with highly proprietary application solutions.
   </td>
   <td>Scaled client-server applications on traditional enterprise infrastructure requring infrastructure solutions to cater for non-funtional requirements
   </td>
   <td>Development of microservice architectures with reducing reliance on traditional infrastructure, reducing centralistation. Adoption of CI by developers for consistent integraton and testing, driving feedback.
   </td>
   <td>GitOps deployment of all applications. Use of service meshes and proxies, along with message streaming and use of operators for continuous operations.
<p>
<strong>CNCF Projects: Flux, ArgoCD, NATS, Envoy, Contour</strong>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Observability and Analysis
   </td>
   <td>Little/piecemeal monitoring and logging
   </td>
   <td>Logging infrastructure in place, along with separate application logging compared to middleware or infrastructure. Scripting for automation
   </td>
   <td>Full monitoring and logging of each layer of the stack.Tracing coded into applications. Adoption of configuration management tooling and version control for operations as well as development
   </td>
   <td>Ability to trace transactions and events through full stack and ability to infer full stack state at a given point in time. Visiblity through dashboards and unified logging.
<p>
<strong>CNCF Projects: Jaeger, Fluentd, Prometheus, OpenTracing</strong>
   </td>
   <td>
   </td>
  </tr>
</table>


We can see legacy designs in the far left, with a cloud-native approach to the right.

The main message is that if we take what the Trail Map has implicit within it, and make it explicit, that Cloud Native is indeed a journey _and has these explicit features_, then this is of great assistance.  Another way of thinking about it is that this takes the single path of the Trail Map and turns it into five more detailed paths.

The model doesn’t incorporate the _Special_ or _CNCF Members_ categories.  Given these are related to relationships rather than explicitly highlighting technology maturation, this isn’t an issue.  However, _Serverless_ is also missing in this example though it might be catered for by starting only in the column headed “Cloud Native”.

This maturity model doesn’t necessarily take away from the Trail Map and need not replace it though where this may happen is through a graphical representation like the trail map, but drawing out the five categories separately. The Trail Map itself could use common labelling for stages that correspond to the categories in the Landscape to further integrate the two together.

The maturity model is also a useful complement to the CNCF Technology Radar.  The Radar is vitally important in setting out what companies are doing now and therefore, in keeping a maturity model fresh, the radar could be vitally important.  Maturity will evolve over time - after all, it is built on skills and experience, with the latter being exactly what the Radar delivers.


### Use-case/Persona 2:  Tactical Needs and Understanding Capabilities

As discussed previously, the Landscape is a tremendous resource for seeing what projects and products are available, but one lack that it has is that it aside from a broad categorisation of a project or product, and a short, perhaps one line description of the item, it gives little information about the actual capabilities of a given product or service.  Although in the case of a query using, for example, **Orchestration & Management → Coordination & Service Discovery** there are just 5 cards listed, when we look at **App Definition and Development → Database** there are 48 separate cards.  Taking the first query as an example however, there is a significant difference between CoreDNS compared to etcd and ZooKeeper.  With the database example above also, there are major differences between how, for example, Apache Ignite and Vitess are used.  They fit into the broad category of database, but their implementations, and crucially, the problems they are designed to solve.

A proposal for the Tactical use-case of the Landscape may be as follows:

Additional attributes could be added to each card.



*   They may be either free-form, listing out keep functionality
    *   Benefit: No overhead for CNCF in managing technology-specific criteria
*   or they may also match a list, allowing further refinement at a third level.
    *   Benefit: Users may have a third level of refinement to filter on.  In the example of databases, if Key-Value store is a technology-specific attribute at the third level down within the Landscape, then Redis and Apache Ignite may match that, but Vitess may not.


### Further Discussion

A question may be asked about why consider a maturity model in the first place.  The thought behind the model is that it allows for measurement, and, by starting with legacy platforms, organisations and individuals can score themselves on the platforms they have right now.  Although perhaps some of the technology and techniques on the left side of the model may seem irrelevant, it is the case that many organisations have still not started down, or progressed far down, their Cloud Native journey.  By simply highlighting things like CI-CD that actively contribute to getting started, this model can help to guide.  Also too, it provides a vendor- and project- non-specific path.  This is vital for providing clarity from an independent foundation such as the CNCF which does have the recognition to back such an initiative.  By following a direction guided by the CNCF stakeholders and those stepping into Cloud Native will be helped by having the confidence that they can follow a structured path without necessarily being overwhelmed.

A criticism of the maturity model could be that it may appear to enforce a top down prescription on an open source community that evolves and iterates solutions quickly.   But this might be the wrong criticism to make here, because contributions to Cloud Native maturity come from groups such as SIG-Security within the Kubernetes project.  Indeed, we see them in recommendations made on days such as the Cloud Native Security Day at KubeCon.  What it can do is specify in a central location the overall picture of what a healthy, mature Cloud Native platform and ecosystem looks like, and importantly in what direction contributors feel it is evolving.  This can only be done by taking into account the input from multiple wide and varied groups and projects within the CNCF.  It can only be like this because the CNCF and its community project are indeed _all about community._

A final note to make is that the discussion outlined here also considers just two perspectives or personas who might use the Landscape and the Trail Map.  These are of the “strategic” architect and the “tactical engineer”.  It omits users who may wish to discover other information such as market cap, funding and GitHub stars.


### Summary

The Cloud Native Landscape and the Trail Map are two useful tools for the CNCF and the wider Cloud Native community.  One plots a way forward, and the other brings the wider ecosystem together within broad categories.  The use of a maturity model will be a useful aid allowing organisations and individuals to build up their core competencies in Cloud Native, and drive up their maturity.

The discussion outlined here also considers just two perspectives or personas who might use the Landscape.  These are of the “strategic” architect and the “tactical engineer”.  It omits users who may wish to discover other information such as market cap, funding and GitHub stars.


### Call To Action

The maturity model illustrated above is a sample.  There is too much emphasis on the left hand side, with major jumps from _Contemporary _to _Cloud Native_.  _Cloud Native_ could be further split out, and a picture for what the future could hold could be put in there.  We know from Liz Rice’s keynote of 22 November 2020 at KubeCon that the following topics are seen as hot by the TOC: Chaos engineering, Kubernetes for the Edge, Service mesh, Web assembly and eBPF, Developer and operator experience.  These could be useful considerations for what _Cloud Native Future_ could look like.
