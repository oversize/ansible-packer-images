# Example Machine



* Shows basic working with packer
* Shows Template Basic Structure

The builders section can have one or more builders. The 'type'
key defines which one is to use. The other keys are configurations
for that particular builder and can be found in the documentation
of each builder.

### Example 01

Is just the basic example you'll get from the
https://www.packer.io/intro/getting-started/install.html guide.

* It uses the ami filter to grab the ubuntu base image.
* Provisons the machine using the Shell provisioner and installs redis


### Example 02

From a certain Amazon AMI Image.

* Find an AMI you want to use and set source_ami
