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

Packer builds images using Templates. Templates have


### Web Server

The Web server has nginx and alot of PHP stuff installed.

### Solr Server



### Deployment Server


# More

Codeship: https://blog.codeship.com/packer-ansible/
