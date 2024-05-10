## Mongo Replication in Redhat os family

This role install mongo in redhat family servers and create replication.

## Requirements

Must have mongodb group in your inventory for servers that you want install mongo in it and have at least 3 server in mongodb group.

**Note: there is on play in playbook file that create keyfile that is required for authentication in replication, Don't remove it because it create keyfile.txt in localhost and copy file in mongodb group servers**

## Role Variables

we have multiple variables in vars/main.yml
- mongo_port: define custome mongo port
- mongo_replicaset: define replication name
- mongo_keyfile_path: define mongo keyfile path for auth in replication
- mongo_user: define custome user for auth in mongo
- mongo_password: define password for custome user
- mongo_user_roles: list of roles that you want to assign to your custome user , mongo_user_roles type is list of dictionary , you can see format in vars/main.yml

## Getting Started

### Run Ansible Playbook
You can see playbook example in playbook.yml and inventory example in inventory.yml
```bash
ansible-playbook -i inventory.yml -b playbook.yml
```

## Author Information

This role created by me 😄 (danial nabiyan)

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## Feedback

If you have any feedback, please reach out to us at danial.nabiyan1382@gmail.com
