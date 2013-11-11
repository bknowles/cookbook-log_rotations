LogRotations
============

This cookbook provides an extremely simple way to create log rotations via
attributes. It depends on the logrotate cookbook. Simple example:

```ruby
override_attributes(
  :log_rotations => [
    {:name => 'chef-client', :path => '/var/log/chef/client.log'},
    {:name => 'nginx', :path => '/var/log/nginx/access.log', :frequency => 'daily'}
  ]
)
```

Useful keys within the hash:

* name - required
* path - required
* frequency - defaults to 'daily'
* rotate - defaults to 7
* create - defaults to '640 root root'

Cookbook Info
=============

Original Repo: https://github.com/hw-cookbooks/log_rotations

This version forked from: https://github.com/akatz/cookbook-log_rotations

IRC: Freenode @ #heavywater
