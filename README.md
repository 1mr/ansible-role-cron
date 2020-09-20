# cron

[![Build Status](https://travis-ci.com/1mr/ansible-role-cron.svg?branch=master)](https://travis-ci.com/1mr/ansible-role-cron)

This role helps to configure cron.d files.

## Requirements

This role requires ansible 2.5 or higher.

## Role Variables

* `cron` (default: `[]`)

```yaml
    cron:
      - file: test
        state: present
        record:
          - name: hello
            user: www-data
            minute: "*/5"
            job: echo 'hello'
            state: present
```

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
         - { role: 1mr.cron, tags: cron }

## License

MIT

## Author Information

This role was created by Stas Stavnichuk.
