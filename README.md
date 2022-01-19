Role Name
=========

This role check the openshift cluster health

Requirements
------------

Not appliable

Role Variables
--------------

- `ocp_cluster_kubeconfig`, path to kubeconfig *defaults* to `""`
- `ocp_clustertest_marketplace_namespace`, marketplace namespace name *defaults* to  `openshift-marketplace`
- `ocp_clustertest_catalogsource_name`, catalogsource name *defaults* to `redhat-operators`
- `ocp_clustertest_skip_olm`, check if the operator index matches the openshift version, *defaults* to `false`, set to `true` if custom images are being used
- `ocp_clustertest_skip_pdb_check`, skip check for PodDisruptionBudget *defaults* to `false`

Dependencies
------------

Not appliable

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

	- name: Check cluster health
	  hosts: localhost
	  connection: local
	  gather_facts: false
	  vars:
	    ocp_cluster_kubeconfig: "~/.kube/config"
	  roles:
	    - openshift_clusterhealth


License
-------

BSD

Author Information
------------------


Rob Mokkink <rob@mokkinksystems.com>
