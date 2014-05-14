### `nxos_install_rawconfig`

### Synopsis

Install a NX-OS configuration.  This could either be a complete configuration (overrite) or a "snippet" of change.
This module will simply take a template in, render it, and apply to the device(s).

Currently the only supported input option is "plain text", just as it would be in the running-configuration file.  This module uses the file extension to determine the format:

* `.conf` = text

Check-Mode is NOT supported. This module will paste the configuration files via SSH blindly.

### Example Usage

````
  tasks:
    - name: Pushing banner config
      nxos_install_config:
        host={{ inventory_hostname }}
        file=/var/tmp/banner.conf
````

### Options

| parameter 	| required 	| default 	| choices     	| description                                                                                                                                	|
|-----------	|----------	|---------	|-------------	|--------------------------------------------------------------------------------------------------------------------------------------------	|
| host      	| yes      	|         	|             	| This should be set to {{ inventory_hostname }}                                                                                             	|
| user      	| no       	| $USER   	|             	| Login user-name                                                                                                                            	|
| passwd    	| no       	| None    	|             	| Login password.  If not supplied, assumes that ssh-keys are installed and active                                                           	|
| file      	| yes      	| None    	|             	| File on the local server that contains the configuration change.                                                                           	|
| logfile   	| no       	|         	|             	| File on the local server when progress and status is stored                                                                                	|
