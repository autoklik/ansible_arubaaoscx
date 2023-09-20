* This Ansible for Aruba AOSCX switches modules has been tested on Aruba Switches: 6300, 6400, 8320, 8325

* Please follow the guide below on how to configure the Aruba AOSCX collections on RHEL based OS.

* * Install ansible-core
    * Type yum install ansible-core
* Once done
    * Type ansible - -version
* Install re (repeat these steps if new user account has been created and wants to run ansible under that account)
    * Type yum install pip (use sudo if non root)
* Install arubanetworks collections  (do not use sudo)
    * Type ansible-galaxy collection install arubanetworks.aoscx (one line)
    * Go to home directory of the current user: 
        * Type cd /home/ansible/.ansible/collections/ansible_collections/arubanetworks/aoscx
    * Type ansible-galaxy collection list
        *  Collection               Version
        *  ------------------------ -------
        *  ansible.netcommon        2.3.0
        *  ansible.posix            1.1.1
        * ansible.utils            2.3.1
        *  arubanetworks.aos_switch 1.4.0
        *  arubanetworks.aoscx      3.0.1
    * Type ansible-galaxy install -r requirements.yml
    * Type python3 -m pip install -r requirements.txt
* Install ansible-galaxy collection install community.general
    * Type ansible-galaxy collection install community.general (do not use sudo)
* Install ansible-galaxy install arubanetworks.aoscx_role (optional if it is not installed yet)
    * Type ansible-galaxy install arubanetworks.aoscx_role (do not use sudo)
* Change back to working directory to test out 
    * E.g /etc/ansible
