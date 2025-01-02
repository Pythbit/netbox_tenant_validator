Netbox Custom Validator documentation: https://netboxlabs.com/docs/netbox/en/stable/customization/custom-validation/

Created with Netbox 4.1

How I installed it:

1. Create a folder /opt/netbox/netbox/validators
2. Move files into that folder
3. In /opt/netbox/netbox/netbox/configuration.py add the following:
   CUSTOM_VALIDATORS = {
  'ipam.ipaddress': (
    'validators.ipam.prefixTenantValidator',
  )
}

My intent is for this script to contain any/all ipam validators but do whatever you'd like.
