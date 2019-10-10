# Add a module in Odoo

## Modify your file odoo/spec.yaml

Add in odoo/spec.yaml :

```
sale-workflow:
    modules:
	    - sale_isolated_quotation
    src: https://github.com/OCA/sale-workflow.git
```

In this example, the module is 'sale_isolated_quotation', and it belongs to a group 'sale-workflow'.

In case you need to specify a branch :

```
src: https://github.com/OCA/sale-workflow.git 12.0
```
		
In case module you want to install is not in version of your project :

```
sale-workflow-11:
    modules:
	    - sale_isolated_quotation
    src: https://github.com/OCA/sale-workflow.git 11.0
```
## Launch ak build 

In the terminal, go to odoo folder:

```
$ cd odoo
```

And launch :

```
$ ak build
```

This command will:
+ Update odoo/repo.yaml file using git aggregator
+ Download files and repo locally in odoo/external-src
+ Give add_ons to integrate in confid file

Don't forget to come back to root folder to launch docky after.

## Add add_ons paths

You need to add in docker-compose.yml addons_path
This links are given in terminal at the end of ak build

```
services:
	...
  odoo:
    ...
    environment:
			...
      - ADDONS_PATH=/odoo/src/addons,/odoo/src/odoo/addons,/odoo/links,/odoo/local-src
```

## Launch odoo and update app lists

In main folder, launch

```
$ docky run
```

In the console open in the container, you can launch:

```
$ odoo
```

On your browser, you need to activate debug mode and update apps list

Otherwise, you can launch it with this command:

```
$ odoo -u module_name
```

## Install module

Install it by clicking on install and enjoy !

