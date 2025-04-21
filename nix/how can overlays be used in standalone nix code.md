START
Basic
Front: 
How can overlays be used in standalone Nix code?
Back: 
- In a `shell.nix`:
```nix
let pkgs = import <nixpkgs> { overlays = [ overlay1 overlay2 ]; };
```

- In a Nix flake:
```nix
let pkgs = import nixpkgs { inherit system; overlays = [ overlay1 overlay2 ]; };
```
<!--ID: 1745224913026-->
END
