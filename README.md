# 概要
Node.js を利用するための手順です。  
本手順のほかに、install-yarnの手順が必要です。  
- [install-yarn](https://github.com/latonaio/install-yarn)

# how to setup
セットアップのためのコマンドは、node-js.yaml 内にあります。

```
- name: install npm
  become: yes
  apt:
    name: npm

- name: install n package
  become: yes
  shell: npm install -g n 

- name: install latest nodejs using n package
  become: yes
  shell: n latest

- name: update npm
  become: yes
  shell: npm update -g
```

