# Database Version Control Module Documentation
## Overview:

## Resources:
- Version Control Information:
  - URL: git@gitlab.pifsc.gov:centralized-data-tools/database-version-control-module.git
  - Database: 0.2 (git tag: db_vers_ctrl_db_v0.2)
  - Application: 0.13 (git tag: db_vers_ctrl_v0.13)
- [VCM SOP](./DB%20Version%20Control%20Module%20SOP.MD)
- [Database Naming Conventions](./DB%20Version%20Control%20Module%20DB%20Naming%20Conventions.MD)
- [Installing or Upgrading the DB Version Control Module](./Installing%20or%20Upgrading%20the%20DB%20Version%20Control%20Module.MD)
- Documentation Template:
  - This Database Installation/Upgrade template is provided so a given module that has had the Database Version Control Module installed can change the [placeholders](./placeholder_documentation.MD) (defined in enclosing brackets) and reference that document in the main technical document for the module.
    - [Markdown Format](./Template%20-%20Installing%20or%20Upgrading%20the%20Database.MD)
Database Design:  
- Oracle Tables:
  - Each time a database upgrade is applied it will insert a record into the DB_UPGRADE_LOGS table that defines the numeric version and application/module name that was applied
- Oracle Views:
  - The DB_UPGRADE_LOGS_V view can be used to view the upgrade logs for a given database instance
- **Note: detailed object/column comments are defined on each table and view database objects