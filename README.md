# Amazon Images using Packer and Ansible

I wanted to learn how to produce amazon ami Images using packer and ansible. This
Repository keeps my learnings and experiments for my own reference.

* Packer https://www.packer.io/
* Ansible https://www.ansible.com/
* Amazon Images http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html

You should have at least an idea of what these things are and what they do.
The rest in here might not make sense if you do not.

### I want to

* Built Images for Amazon (production and staging) the same way as i do for my development (Virtualbox)
* Get rid of bash scripts doing magical things (i hardly understand a few weeks after i wrote them)
* Use what i learned in ansible to provision Ami Images that are "ready to run" and dont need alot of time to be built

As far as i can tell, ansible and packer do offer me that. There may be other
solutions for that. If you have an idea of what i could do better then this
please contact me.

# Packer 101

https://www.packer.io/intro/getting-started/install.html

Packer builds images using Templates. Templates are written in JSON and
contain the following elements. For a Detailed explanation of the Structure
see here: https://www.packer.io/docs/templates/index.html

**variables** Defines variables for us in the template

**builders** A list of the builders that this template builds. A single
Template can have multiple builders.https://www.packer.io/docs/templates/builders.html

**provisioners** A list of provisionser that should be run for each(!) builder.
https://www.packer.io/docs/templates/provisioners.html

**post-processors** A list of post-processors that define steps to do with
the built images. https://www.packer.io/docs/templates/provisioners.html

## Provisioning

After the Builders have run the Provisioning is done for each builder.
You can configure to have some provisioners only run on some builders. See docs

Most of them are run on the built image. The shell-local provisioner however
is run on the local machine (the one where packer runs).

Most builders are straight forward. In general just rememer that they are run
after the image was booted the first time to install software and configure
things before the image is created.

## Aws Authentication

Will be pulled fom you cli if you have that installed (and configured).
If not provide enviroment variables.

    AWS_SECRET_ACCESS_KEY='xxx'
    AWS_ACCESS_KEY_ID='xxx'

You can olso have packer ask you for these during build. See packer docs

# More

Codeship: https://blog.codeship.com/packer-ansible/
