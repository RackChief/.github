# RackChief

**RackChief is a lightweight, self-hosted platform for managing homelab infrastructure, upgrades, projects, and planned purchases.**

It is being built for people who want more structure than a spreadsheet, but less overhead than a full CMDB, ITSM platform, or project-management suite.

RackChief brings physical infrastructure and project planning together in one place, so you can answer questions like:

- What hardware do I have?
- What am I planning to upgrade?
- Which projects affect which systems?
- What parts or equipment do I still need to buy?
- What has already been ordered, received, or completed?
- How much is a project expected to cost?
- What work is still outstanding?

## What RackChief is

RackChief combines a few ideas normally spread across multiple tools:

- **Infrastructure inventory** for servers, storage, networking, racks, UPSes, and other equipment
- **Project planning** for upgrades, migrations, replacements, and other homelab work
- **Purchase tracking** for planned hardware, vendors, pricing, shipping, ordering, and receiving
- **Asset relationships** so projects can be tied directly to the infrastructure they affect
- **API-first access** for integrations, automations, agents, and future MCP tooling

The goal is to keep the system practical and approachable without growing into a full NetBox, Jira, or ITSM replacement.

## Project status

RackChief is currently in **early development**.

The backend is being developed first, with the core inventory and project-planning data model taking shape before the frontend is built out.

Current areas of work include:

- Asset inventory and asset types
- Project planning
- Project-to-asset relationships
- Work and purchase items
- Project history and updates
- REST API and OpenAPI documentation
- Authentication
- Future MCP integration

Networking, rack visualization, component inventory, and additional infrastructure-management features are planned for later iterations.

## Repositories

### [Backend](https://github.com/RackChief/Backend)

The RackChief API and domain layer.

Current stack:

- TypeScript
- Express
- PostgreSQL
- Drizzle ORM
- Supabase Auth
- Zod
- OpenAPI / Swagger

### [Frontend](https://github.com/RackChief/Frontend)

The RackChief web interface.

This repository is currently being prepared while backend development establishes the first stable API surface.

## Design principles

RackChief is being built around a few simple ideas:

**Keep the data useful.**  
Infrastructure, projects, and purchases should be easy to query and automate against.

**Keep the architecture boring.**  
Prefer straightforward, maintainable components over unnecessary complexity.

**Keep the API first-class.**  
The UI should not be the only useful way to interact with RackChief.

**Keep scope under control.**  
RackChief should complement monitoring, configuration management, secrets management, and other specialized tools rather than trying to replace them.

**Make automation easy.**  
A future goal is to expose high-level RackChief capabilities through MCP so assistants and automations can work with project and infrastructure data without direct database access.

## Planned direction

The initial focus is:

```text
Inventory
   +
Projects
   +
Purchases
   +
Automation
