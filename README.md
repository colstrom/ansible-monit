# ansible-monit

[monit](https://mmonit.com/monit/) - a small Open Source utility for managing and monitoring Unix systems. Monit conducts automatic maintenance and repair and can execute meaningful causal actions in error situations.

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

## Important

This playbook is no longer maintained. Recommended alternatives:
  * [PM2] for `node.js` applications (eye is a good fit here too, but `PM2` has some nice extras for node)
  * [eye](https://github.com/kostya/eye) for anything else.

## Tunables

* `monit_user` (string) - User to run monit as
* `monit_poll_rate` (integer) - How often to check processes being monitored?
* `monit_log_root` (string) - Directory for logs
* `monit_log_path` (string) - Path for log file

## Dependencies

* [colstrom.logrotate](https://github.com/colstrom/ansible-logrotate/)

## Example Playbook
    - hosts: servers
      roles:
         - role: colstrom.monit
           monit_user: root
           monit_poll_rate: 15

## License

[MIT](https://tldrlegal.com/license/mit-license)

## Contributors

* [Chris Olstrom](https://colstrom.github.io/) | [e-mail](mailto:chris@olstrom.com) | [Twitter](https://twitter.com/ChrisOlstrom)
* Aaron Pederson
