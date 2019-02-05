# VM Snapshot Age Report

This playbook will request VMs that have snapshots that are older than 90 days and email the owners requesting that they delete them.

The playbook needs the following variables supplied to it:

| variable    | example value             |
|-------------|---------------------------|
| mail_server | mail.company.com          |
| from_email  | cloud_admins@company.com  |