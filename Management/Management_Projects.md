# Appendix C - Equinor

## C.1 Image Forus East

![](https://i.imgur.com/mqcXGyY.png)

## C.2 Project Data Questions

URL = https://wiki.equinor.com/wiki/index.php/Inquiring_project_data_questions


1 Project inquiring data questions


1.1 Data types, data landing and access

- What data sources will the project use?
- Are these sources provided with comprehensive data contracts and documentation?
- Are LRAs and data access regimes in place?
- Does the data have enough metadata to handle access?
- Will multiple sources be providing the same data types or overlapping data?
- Is the data tagged with unique primary keys? (See separate data handbook section for more information).
- Who is the owner of the data used and created in the project? Has the owner(s) been informed about the project?

1.2 Data journey mapping from source to end use

- How will the data be used? User requirements can be documented with this template on Github: Consumer requirements
- What data cleansing is planned?
- What data products will the project deliver, and is there a roadmap for maturing these?
- Is this data linked to the work processes where the data is used and created through metadata?
- Has this work process been mapped out with tasks, roles, applications, and data flow?
- Is the work process context of the data stored?
- Will the data be used for performance management?
- Are there other potential applications that are planning on using the data or may use the data in the future?

1.3 Data governance

- Is there a plan for how the project will follow the Equinor data architecture?
- Is the project anchored with any of the Equinor data networks?
- Is a [Information technology architecture contract] established for the project?

1.4 Data standards

- Are there standards for naming the data? Is there a consensus internally in the company about this?
- What standardized data formats are being planned for?
- For subsurface data: What of the data is already defined in the OSDU, and is there potential to propose new OSDU definitions?
- What master and reference data will be used and what needs to be defined?

1.5 Data modelling and provenance

- Is a data model defined for the project?
- Are there data relations and how?
- Will multiple sources be providing the same data types or overlapping data? If so, is this accounted for in  a data model?
- Is this data related to any Enterprise data, and how will these relations be handled when storing the data in Enterprise?
- To what degree has the provenance of the data input to the project been mapped?
- To what degree is storing of provenance of the data created in the project planned? What will it be used for?
- Is sufficient metadata provided so that any workflows can be rerun and produce the same result?

1.6 Data dynamics

- How will the project handle changes in the data and versions?
- How will data dynamics be managed, Events?
- How is API performance accounted for (how quickly does the data need to be delivered, what should the end-user experience be with respect to accepted time for data being in place)?

1.7 Enterprise data

- Is the project developing an application in OMNIA?
- Are other applications exposing the data in OMNIA or elsewhere?
- Are any of these Enterprise APIs be used?
- Is the project storing data which may be interesting for other applications to use?
- Are there any plans to develop Enterprise APIs
- If so, are there data contracts in place for these APIs?
- And what are the plans for running an maintaining these APIs?

1.8 Vendors

- Are vendors involved in defining and delivering data in the project?
- How will the data services be provided by the vendor, and how does this relate to OMNIA?