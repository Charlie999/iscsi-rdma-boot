# iscsi-rdma-boot

A set of initramfs scripts that disables the open-iscsi boot scripts (at runtime) and attempts to log in to the previously configured target using iSER.
If iSER is not available, this will silently fail and log in using TCP as of now.

iscsid is also left running from the initramfs. This is not ideal and I need to fix this.
