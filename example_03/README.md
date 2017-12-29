# Example with Ansible

The Ansible provisioner comes in two forms

**Ansible-local**

runs ansible playbooks on the machine being built. Therefore it needs to have
Ansible installed on that Machine is done via the shell provisioner before.

It then uploads the playbook and runs it.

### Caveats

Writing Playbook and running them only after the Machine is booted is tedious.
I created myself a testtarget with which i tried and developed the playbooks
befor i actually ran them through packer.

If doing so, dont get confused with the hosts setting in the playbook.
I ended up writing a little static inventory (with the testtarget) and
using thet during playbook development like so

    ansible-playboook -i testtarget playbook.yml

And in the Playbook iteslf give the hosts setting 'all'. This way i could
run the playbook locally for testing and then later during the actually built
without neding to change it. Since the default inventory will alays have 'all'
Hosts. I have yet to further work with it to see how good this works.  
