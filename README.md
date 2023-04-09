#lighthouse
=========
安装灯塔

要求
发行版7

角色变量
----------
- **lighthouse_vcs：** - https://github.com/VKCOM/lighthouse.git

- **lighthouse_location_dir：** - /home/lsd/ligthouse

- **lighthouse_access_log_name：** - lighthouse_access

依赖关系
无

示例剧本
包含一个如何使用角色的示例（例如，将变量作为参数传递）对用户来说也是很好的:
--------------------

```yaml
- name: Install and configure Lighthouse
  hosts: lighthouse
  become: true
  vars:
    lighthouse_path: "/home/user/lighthouse"
    clickhouse_host: hostvars['clickhouse']['ansible_host']
  roles:
    - lighthouse_role
```
