# node-js
Node.js は、Javascript で記述された、主にバックエンドサービスのためのランタイム環境です。  
Node.js は、世界的に汎用なバックエンドコアアーキテクチャとして、グローバル Tech 企業の 様々なシステムやアプリケーションのバックエンドサービスとして採用されています。    
AIONでは、Node.js を、主にエッジコンピューティング環境におけるバックエンドコアのランタイム環境として採用しています。  

# 本レポジトリに含まれるもの  
本レポジトリは、Node.js のセットアップ手順です。  
Node.js を利用するには、本手順のほかに、下記のレポジトリに記載されている、install-yarnの手順が必要です。  
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

