Script Run Order:

1. "install-telemetry-rpm"
2. "telemetry-declaration"
3. "common-shared-declaration"


WARNING: If you're already using AS3 code and the /Common/Shared/ partition/tenant, the "common-shared-declaration" will attempt to overwrite it. You'll want to add that code to your existing /Common/Shared code
