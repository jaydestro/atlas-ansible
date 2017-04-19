# MongoDB Atlas - Launch Cluster via API

---

A simple Ansible playbook to promgramatticaly launch MongoDB Atlas clusters.

You can take the basic features provided in this along with the example `atlas.json` file with requirements for our cluster.


### Prerequisites

* MongoDB Atlas Account
* IP Whitelist configured for API access
* API Key
* Group ID
* Server to launch from
* Ansible 

### Getting Started

After you configure your Atlas account and set up your API key and whitelist, you can fill in the variables at the top of the `create-atlas.yml` file or place them in a separate `vars` file.

```
  vars:
    user: ENTER-MONGODB-ATLAS-USERNAME-HERE
    apikey: ENTER-SECRET-API-KEY-HERE
    groupid: ENTER-GROUPID-HERE
```

`user` requires your Atlas login username, this is not your MongoDB Database user.  This would be the same user you log into your control panel for Atlas with.

`apikey` is generated in the Group Settings section of your Atlas control panel.  Here you can generate a new key.

`groupid` is the ID of your Atlas group which can be found in the URL of your control panel or at the top of the "Group Settings" section.


### Example


```
ansible-playbook  -v create-atlas.yml --diff
```

### TODO
* Write termination method playbook
* find better way to present the connection string after creation.  

