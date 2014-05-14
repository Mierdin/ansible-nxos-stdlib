### `nxos_shutdown`

### Synopsis

Performs a shutdown or reboot of an NX-OS device.

Check-Mode is NOT supported.

### Example Usage

````
  tasks:
    - name: Reboot NX-OS Switches
      nxos_install_config:
        host={{ inventory_hostname }}
        action=r
````

### Options

| parameter 	| required 	| default 	| choices     	| description                                                                                                                                	|
|-----------	|----------	|---------	|-------------	|--------------------------------------------------------------------------------------------------------------------------------------------	|
| host      	| yes      	|         	|             	| This should be set to {{ inventory_hostname }}                                                                                             	|
| user      	| no       	| $USER   	|             	| Login user-name                                                                                                                            	|
| passwd    	| no       	| None    	|             	| Login password.  If not supplied, assumes that ssh-keys are installed and active                                                           	|
| action    	| yes      	| None    	| s/r         	| Specify either shutdown (s) or reboot (r). If nothing specified, or incorrectly specified, defaults to (r)
| logfile   	| no       	|         	|             	| File on the local server when progress and status is stored                                                                                	|
