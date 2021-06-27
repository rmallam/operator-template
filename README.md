Red Hat 3Scale
==============

Setup and configuration for Red Hat 3Scale

Example Playbook
----------------

  tasks:
    - name: Establish access to infrastructure
      include_role:
        name: ocp4-tokens

    - name: Deploy Red Hat 3Scale
      include_role:
        name: 3scale
      when:
        - var_3scale_enabled is defined
        - var_3scale_enabled