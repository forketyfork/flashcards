START
Basic
Front: 
What are the correct permissions for the `.ssh` directory and for the private key inside that directory?
Back: 
- `.ssh` directory should only be accessible by the owner (`700`)
- the private key (e.g., the `id_rsa` file) should only be accessible by the owner (`600`), however, even stricter permissions (`400`) are allowed (read-only for the user).
<!--ID: 1745387645243-->
END
