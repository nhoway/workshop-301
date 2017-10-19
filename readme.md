This is an "Infrastructure as Code" workshop using:
* [cloud-init](https://cloudinit.readthedocs.io/en/latest/): a configurable boot script manager for cloud instance
* [Terraform](https://www.terraform.io/): a IaaS orchestrator from Hashicorp
* [OVH Public Cloud](http://www.ovh.com/cloud): a IaaS solution based on OpenStack by OVH

# Purpose

You'll run a workshop which present you some **"Infrastructure as Code"** basics. IaC is the art of deploying and managing IT resources using programs and definition files in order to automatize and benefit from all the best practices in the development process like patching, templating, versioning and many others.

There will be 3 environments:
 * Dev: This environment is really simple and flexible, you'll learn here how to use OpenStack CLI and cloud-init script to manage post install configuration
 * Test: This one shows how to use Terraform, an orchestrator tool. You'll manipulate some resources, modules and template definitions with dependences
 * Prod: The last environment uses a versioned code to stabilize the infrastructure. You'll see also how to scale up and down an infrastructure

Broadly speaking, the workshop presents files with missing parts and you'll have to complete its with copy/paste actions. Of course, the interest for you is to pay attention on the code structure and best practices to understand the possibilities you have with IaC.

## Schema

![Test architecture](./content/arch.png)

# Requirements

To start the workshop, you'll need an OVH Account, a new cloud project attached to a vRack.

## OVH account

You can skip this section if you already have one but be sure to be able to run a workshop on it (your company could have some restrictions about that if you plane to use your company's account).

If you run this workshop online and you don't have an account, just [sign up](https://www.ovh.com/fr/support/new_nic.xml) and log in to the web console.

If you run this workshop during a training session, the OVH account creation is not include in the schedule (1h30). Be sure to have it before the session and go directly in to the web console.

## Cloud project

Click on the "Cloud" tab then on "Order" button. Select "Cloud Project" and use your voucher code to apply.

## vRack

Once your cloud project is ready, click on "Enable the vRack" and go through the command process. Wait up to 3 min and go back to the web console in "Dedicated" tab then click on the vRack menu. Here you should see a new vRack named "pn-XXX". Select this vRack and add your cloud project inside using the "Add" button.

## An OpenStack User

Go back to your cloud project and click on "OpenStack" in the left bar, then on "Add a User". 

Now we'll get the configuration file for this user. Click on the small tool icon on the right side of the user line, then on "Download the OpenStack configuration file". Keep the text editor open, we'll copy/paste the content of this file.

## Video

If you need help on that part, please watch those videos:

 * [Open an OVH account and create an OpenStack User](https://www.youtube.com/watch?v=BIMb0iR1YhY)
 * [Activate the private networks](https://www.youtube.com/watch?v=hw2vQPDFQYc)

# Let's Go!

A server is available with a prepared environment.

```bash
ssh bounce@xxx.xxx.xxx.xxx
```

The IP and the password are provided during the workshop. You have to give a unique ID, it can be your desktop ID or your firstname.name (without accent and space). In case of connection lost, just redo the same.

Create a file named credentials and paste the content of the downloaded file on the previous step.

```bash
git clone https://github.com/pilgrimstack/workshop-301.git
cd workshop-301/0.dev
```

Let's go to the [development environment](./0.dev).
