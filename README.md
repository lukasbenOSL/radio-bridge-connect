# AI Radio Bridge · Connect

Static OAuth relay for the AI Radio Bridge. Systems such as Salesforce only return to `https` addresses after a login;
the bridge runs on `http` in the local network. `callback.html` forwards `code` / `state` to the bridge address named in
`state`, and only to a private network address with the path `/oauth/<system>/callback`. It stores nothing; the code
cannot be used without the PKCE verifier, which never leaves the bridge.
