# Apply Windows Updates to VMware Templates

This playbook is designed to request all VMs and Templates that have the tag "win_auto_update=true" from the ManageIQ / CloudForms REST API.  Then it converts the templates to VMs, powers them on, applies Windows Updates, confirms there are no pending updates, and then it converts back to templates.

To use in your environment, you will need to create the win_auto_update tag and apply it to your templates that you would like automatically updated.

You will need to supply the following variables to the playbook:

| variable                   | value                                                 |
|----------------------------|-------------------------------------------------------|
| win_updates_category_names | ['CriticalUpdates','SecurityUpdates','UpdateRollups'] |
| win_updates_reboot         | true                                                  |

See the Ansible [win_updates](https://docs.ansible.com/ansible/latest/modules/win_updates_module.html) module for all category options.
