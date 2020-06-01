# mastering_ansible
advanced execution
    gather_facts: false for those playbooks don't need
    cache_valid_time
    limit
        ansible-playbook site.yml --limit web
    tags
        ansible-playbook site.yml --tags "packages"
        ansible-playbook site.yml --skip-tags "packages"
    changed_when, failed_when
    Pipelining


Troubleshooting , testing and valdation
    ignore_error: true
    ansible-playbook site.yml --step
    ansible-playbook site.yml --list-tasks
    ansible-playbook site.yml --start-at-task "copy demo app source"
    retrying failed host
        ansible-playbook site.yml --limit @/home/marco/ansible/site.retry
    syntax-check , dry run, 
        ansible-playbook --syntax-check site.yml
        ansible-playbook --check site.yml
    debug
        - debug: var=active.stdout_lines