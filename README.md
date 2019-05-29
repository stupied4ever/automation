# Automation

This history starts long long time ago ([Dec 18, 2013][first-dev-box-commit])
when inspired by [Leandro Facchinetti (leafac)](https://github.com/leafac)
I decided to automate my environment (vim, tmux, linux, etc). To be honest,
I forked leafac's repo removing some tools and includind some other. And
since there a acknowledgement message was written on the very top of this
repo.

After some time, I decided an rewrite was important, (to be honest, I dont
remember why, but probably it was another idea from leafac) and the second
version was available on [dev-box][second-dev-box]. The main difference
from the first version is the removal of puppet. Updating the dev box was
hard and painfull.

tldr;

I am starting the third version of this idea, and the big change this time
is to make the automation fast and simple.
I choosed to use ansible. Thats because I was lazy to do it with Makefile,
but probably in the fourth version this will be the big change.

## Requirements

 - Ansible

## Ansible modules

It uses kewlfft/ansible-aur to install aur packages:

`git clone https://github.com/kewlfft/ansible-aur.git ~/.ansible/plugins/modules/aur`

## Running

`ansible-playbook --ask-become site.yml`

[first-dev-box-commit]: https://github.com/stupied4ever/xxx-dev-box/commit/5c4531b5f0505d7d5444c8883fe384ac9434dbc2
[second-dev-box]: https://github.com/stupied4ever/dev-box

