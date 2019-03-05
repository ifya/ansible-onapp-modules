# ansible-onapp-modules
Ansible modules to manage OnApp Cloud resources (VS, etc.)

To test this module:
```
cat /tmp/args.json
{
    "ANSIBLE_MODULE_ARGS": {
        "name": "my_virtual_server",
        "new": true
    }
}
# cp libcloud.ini.template ~/.ansible/libcloud.ini
# edit ~/.ansible/libcloud.ini and put your credentials there
>python onapp_vs.py /tmp/args.json
>ANSIBLE_LIBRARY=. ansible-playbook test.yml
```

## Roadmap:
- make module parameters out of CPU/RAM/Storage
- use by default private NIC (assign a private IP)
- refactor result[''] = ... into a function
