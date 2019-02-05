# Apply Windows Updates to VMware Templates

This playbook is designed to request all VMs and Templates that have the tag "win_auto_update=true" from the ManageIQ / CloudForms REST API.  Then it converts the templates to VMs, powers them on, applies Windows Updates, confirms there are no pending updates, and then it converts back to templates.

To use in your environment, you will need to create the win_auto_update tag and apply it to your templates that you would like automatically updated.
