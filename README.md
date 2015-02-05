# Vagrant + Ansible Machine

### Resources
- postgresql
- imagemagick
- nodejs
- chruby
- ruby
- phantomjs
- redis
- memcached
- mysql
- mongodb

### Set up the environment

1. Install [VirtualBox](https://www.virtualbox.org/)
2. Install [Ansible](http://www.ansible.com/)
3. Clone this repository
4. You must set your workspace directory in `Vagrantfile`. Change the ``"."`` in the following line, to the directory where your refer source code is:

  ```ruby
  config.vm.synced_folder "/Users/wagnerjgoncalves/projects", "/projects", nfs: true
  ```

5. Then run `vagrant up`
