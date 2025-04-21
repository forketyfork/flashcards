START
Basic
Front: How do you tell Helm not to uninstall a resource?
Back: 
Add an annotation `helm.sh/resource-policy: keep` to this resource. During `uninstall`, `upgrade` or `rollback` operations, this resource won't be deleted. However, it will become orphaned and not managed by Helm in any way. This may lead to issues if using `helm install --replace` on an uninstalled release that has kept its resources. 

The `helm install --replace` command will re-use the given name, only if that name is an uninstalled release which remains in the history. This is unsafe in production.
<!--ID: 1745135900090-->
END
