# lighthouse-role
它用于配置运行SystemD的操作系统以使用VK Lighthouse

lighthouse_path变量
-存储Lighthouse静态文件的路径

clickhouse_host:-用于查看指标的Clickhouse主机。

clickhosue_port：-用于查看指标的Clickhouse端口。

clickhosue_user：-Clickhouse用户查看指标。

clickhosue_password：-授权Clickhouse用户的密码。

使用示例

- name: Install and configure Lighthouse
  hosts: lighthouse
  become: true
  vars:
    lighthouse_path: "/home/user/lighthouse"
    clickhouse_host: hostvars['clickhouse']['ansible_host']
  roles:
    - lighthouse_role
