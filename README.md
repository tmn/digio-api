digio-api
=========

## Installation
```
npm install digio-api
```

## Examples
```javascript
var api = require('digio-api')('<access_token>')

api.droplets.list(function (err, data) {
  console.log('Droplets: ', data);
})
```

## Methods
```javascript
actions.get(<action_id>, callback)
actions.list(callback)

domains.create(<domain>, <ip>, callback)
domains.delete(<domain>, callback)
domains.get(<domain>, callback)
domains.list(callback)
domains.create_record(<domain>, <ip>, <type>, callback)
domains.delete_record(<domain>, <record>, callback)
domains.get_record(<domain>, <record>, callback)
domains.list_records(<domain>, callback)
domains.update_record(<domain>, <record>, <new_name>, callback)

droplets.create(<name>, <region>, <size>, <image>, <ssh_keys>, <backups>, <ipv6>, <private_networking>, callback)
droplets.delete(<droplet_id>, callback)
droplets.get(<droplet_id>, callback)
droplets.list(callback)
droplets.list_droplet_actions(<droplet_id>, callback)
droplets.list_droplet_kernels(<droplet_id>, callback)
droplets.list_droplet_backups(<droplet_id>, callback)
droplets.list_droplet_snapshots(<droplet_id>, callback)
droplets.change_kernel(<droplet_id>, <kernel_id>, callback)
droplets.disable_backups(<droplet_id>, callback)
droplets.enable_ipv6(<droplet_id>, callback)
droplets.enable_priv_net(<droplet_id>, callback)
droplets.get_droplet_action(<droplet_id>, <action_id>, callback)
droplets.password_reset(<droplet_id>, callback)
droplets.power_cycle(<droplet_id>, callback)
droplets.power_off(<droplet_id>, callback)
droplets.power_on(<droplet_id>, callback)
droplets.reboot(<droplet_id>, callback)
droplets.rebuild(<droplet_id>, <image_id>, callback)
droplets.rename(<droplet_id>, <new_name>, callback)
droplets.resize(<droplet_id>, <new_size>, callback)
droplets.restore(<droplet_id>, <image_id>, callback)
droplets.shutdown(<droplet_id>, callback)
droplets.snapshot(<droplet_id>, <name>, callback)

images.delete(<image_id>, callback)
images.get(<image_id>, callback)
images.get_action(<image_id>, <action_id>, callback)
images.list(callback)
images.transfer(<image_id>, <region>, callback)
images.update(<image_id>, <name>, callback)

keys.create(<name>, <public_key>, callback)
keys.delete(<key_id/fingerprint>, callback)
keys.get(<key_id/fingerprint>, callback)
keys.list(callback)
keys.update(<key_id/fingerprint>, <new_name>, callback)

regions.list(callback)

sizes.list(callback)
```
