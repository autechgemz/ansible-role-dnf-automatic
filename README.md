# ansible-role-dnf-automatic

## Description

DNF Package manager - automated upgrades.

## Requirements

None

## Dependencies

None

## OS Platforms

- AmazonLinux-2023

## Example Playbook

```yaml
- hosts: all
  roles:
    - dnf-automatic
```

## Role Variables

### dnf_automatic_package_ensure: (string)

```yaml
dnf-automatic_package_ensure: present
```

### dnf_automatic_service_name: (string)

```yaml
dnf-automatic_service_name: 'dnf-automatic.timer'
```

### dnf_automatic_service_ensure: (string)

```yaml
dnf-automatic_service_ensure: 'started'
```

### dnf_automatic_service_enable: (bool)

```yaml
dnf-automatic_service_enable: true
```

### dnf_automatic_config_options: (dict)

None

### dnf_automatic_timer_oncalendar: (string)

```yaml
dnf_automatic_timer_oncalendar: '*-*-* 6:00'
```

### dnf_automatic_timer_randomized_delay: (string)

```yaml
dnf_automatic_timer_randomized_delay: '60m'
```

## Example vars

```yaml
dnf_automatic_config_options:
  commands:
     apply_updates: 'yes'
dnf_automatic_timer_oncalendar: 'Fri *-*-* 21:00'
```
