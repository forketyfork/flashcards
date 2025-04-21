START
Basic
Front: 
How do Nix overlays modify packages?
Back: 
They reference `prev` for unmodified packages and `final` for the fully applied state. Example:
```nix
final: prev: {
	google-chrome = prev.google-chrome.override {
		commandLineArgs = "--proxy-server='https=127.0.0.1:3128;http=127.0.0.1:3128'";
	};
}
```
<!--ID: 1745224913025-->
END
