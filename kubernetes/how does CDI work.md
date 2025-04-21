START
Basic
Front: 
How does CDI work?
Back: 
CDI uses JSON or YAML specification files stored in predefined directories (`/etc/cdi` for static specs, `/var/run/cdi` for dynamic specs). The workflow includes:
1. Vendors providing JSON files describing device requirements.
2. Container runtimes reading these files when a CDI device is specified.
3. The runtime validating the device, updating the OCI specification, and launching the container.
<!--ID: 1745222218935-->
END
