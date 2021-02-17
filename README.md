To install the roles required:

`ansible-galaxy install -p roles -r requirements.yml`

There are a lot of comments spreadout throughout the repo.. 

`slurm_cluster_playbook.yml` contains the plays for the head node and the worker nodes..

This is all set up to run on Ubuntu 20.04 LTS. For Centos or RedHat you will have to make some modifications to lots of stuff - mostly get rid of all the Ubuntuisms like `apt` etc... (I use Ubuntu for everything, never used Centos except for my Stratum 1 CVMFS server)

The group_vars/VAULT file was encrypted with: `ansible-vault encrypt group_vars/VAULT`

To edit the file, use: `ansible-vault edit group_vars/VAULT`

I have also encrypted the `files/munge.key` file using the same password as the VAULT.

Hope this helps.
