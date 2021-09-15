# Role Name

This role configures several tasks at the OS level

- installs a host file based (DNS) blocking based upon [energized](https://energized.pro/). The original hosts file is backed up to `/etc/hosts.original` and can be restored by running the role with `hosts_pack: none` again. Have a look at [packs](https://block.energized.pro/) for an overview of available packs and their features.

- installs udev rules for an [Ergodox EZ](https://knowledge.rootknecht.net/ergodox-ez) keyboard

- allows sudo permissions without password

- configures Thinkpad related settings

## Test

Run `molecule test` to test this role via docker

## Requirements

- Sudo permission

## ansible-role-system

| Variable              | Description                                   | default |
| --------------------- | --------------------------------------------- | ------- |
| hosts_pack            | if and which hosts pack to use from energized | false   |
| thinkpad              | Thinkpad specific settings                    | false   |
| ergodox               | enable udev rule for ergodx keyboards         | false   |
| sudo_without_password | Allow sudo withput password                   | false   |

## Dependencies

No dependencies

## Example Playbook

See [converge.yaml](https://github.com/Allaman/ansible-role-system/tree/master/molecule/default/converge.yml)

## License

MIT
