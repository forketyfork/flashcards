
⸻

START
Basic
Front: What does --userns-remap=default do in Docker?
Back: It enables user namespace remapping by mapping container UIDs (like root) to unprivileged UIDs on the host for better security isolation.
<!--ID: 1749631068021-->
END

⸻

START
Basic
Front: Why use --userns-remap=default in Docker?
Back: To reduce the risk of container escape by ensuring processes that appear as root in the container are not root on the host.
<!--ID: 1749631068022-->
END

⸻

START
Basic
Front: What user is typically created when --userns-remap=default is used?
Back: Docker creates a user and group named dockremap to manage UID/GID remapping.
<!--ID: 1749631068023-->
END

⸻

START
Basic
Front: What file controls UID mapping for Docker’s user namespace remap?
Back: /etc/subuid and /etc/subgid define how container UIDs/GIDs map to host UIDs/GIDs.
<!--ID: 1749631068024-->
END

⸻

START
Basic
Front: What is a common issue when using --userns-remap=default with volume mounts?
Back: File permission mismatches, since container UIDs are mapped to different UIDs on the host.
<!--ID: 1749631068025-->
END

⸻

START
Basic
Front: When should you avoid using --userns-remap=default?
Back: When UID/GID mapping complicates file access, or you’re already using other isolation mechanisms like gVisor or AppArmor.
<!--ID: 1749631068026-->
END