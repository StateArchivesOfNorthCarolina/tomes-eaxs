# Introduction

**EAXS** stands for *Email Account XML Schema*. 

EAXS is designed to store XML-encoded message and attachment data for a single e-mail account. The schema was developed by the [State Archives of North Carolina](https://archives.ncdcr.gov) and the [Smithsonian Institution Archives](https://siarchives.si.edu) circa 2008.

The schema files were move to GitHub in July, 2018 for the TOMES project.

## Namespace Name
The TOMES project namespace name for EAXS is `https://github.com/StateArchivesOfNorthCarolina/tomes-eaxs`.

## XSD Versions
Current and future EAXS XSD files are location in the `./versions` directory.

Each version sub-directory, e.g. `./versions/1`, is intended to contain a persistent version of the schema.

A persistent version can include version-controlled modifications to the schema or documentation files, etc. provided they do not invalidate existing EAXS XML files that adhere to that specific version.

By contrast, changes to Version 1 of the EAXS schema that would invalidate an existing first-version EAXS XML file will require creating a new, hard-coded version of the schema, i.e `./versions/2/eaxs_schema_v2.xsd`.


## Schema Locations
The EAXS XML `schemaLocation` attribute will use the "raw" GitHub view of a given XSD file as its value, e.g. `schemaLocation="https://raw.githubusercontent.com/StateArchivesOfNorthCarolina/tomes-eaxs/master/versions/1/eaxs_schema_v1.xsd"`.

## EAXS as JSON
Version 1 of the EAXS schema includes an experimental but unsupported JSON version. TOMES related tools might support JSON output in the future. 

 