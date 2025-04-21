START
Basic
Front: What properties are responsible for the password authentication?
Back: 
- `PasswordAuthentication=yes (default) / no` — whether the password authentication is allowed;
- `KbdInteractiveAuthentication=yes (default) /no` — whether to allow keyboard-interactive authentication;
- `ChallengeResponseAuthentication` — a deprecated alias for `KbdInteractiveAuthentication`;
- `UsePAM=yes / no (default)` — enables the PAM interface, i.e., PAM authentication using `KbdInteractiveAuthentication` and `PasswordAuthentication` in addition to PAM account and session module processing for all auth types. Since PAM keyboard-interactive auth usually serves an equivalent role to the password auth, one of `(KbdInteractiveAuthentication, PasswordAuthentication)` should be disabled. With this setting, you must run sshd as root;
- `PermitRootLogin = yes / prohibit-password (default) / forced-commands-only / no` — whether root can log in with ssh. The `prohibit-password` (or its deprecated alias, `without-password`) value means password and keyboard-interactive auth is disabled for root; forced-commands-only means root can log in with public key only if the command option has been specified (e.g. to take remote backups).
<!--ID: 1745139815767-->
END
