# iscsi-rdma-boot

A set of initramfs scripts that disables the open-iscsi boot scripts (at runtime) and attempts to log in to the previously configured target using iSER.
If iSER is not available (if ibstat detects no RDMA-capable devices), this will fall back to TCP to still allow booting.

iscsid is also left running from the initramfs. This is not ideal and I need to fix this.

.deb packages are available as CI artifacts, they can also be built like so:
`fakeroot dpkg-deb --build iscsi-rdma-root/`
