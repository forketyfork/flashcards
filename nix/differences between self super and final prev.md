START
Basic
Front: 
What are the practical differences between `self: super:` and `final: prev:` in Nix Overlays?
Back: 
- Compatibility: `self: super:` works in non-flake environments, while `final: prev:` is required for flakes.
- Readability: `final` and `prev` are more intuitive for newcomers.
- Tooling: Flakes enforce the use of `final: prev:` in some cases.
<!--ID: 1745222218915-->
END
