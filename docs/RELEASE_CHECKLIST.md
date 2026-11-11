# Public ARK release checklist

This repository is **distribution-only**. ARK source code and private build history must not be pushed here.

## Before building
- [ ] Confirm candidate changes are reviewed and the private development tree is clean or explicitly recorded.
- [ ] Confirm release scope and version; complete unit, integration and real desktop smoke tests.
- [ ] Review software dependency licenses, vendored code, model weights and assets for public redistribution rights. Verify CAI and other research-only/noncommercial components separately.
- [ ] Audit API key storage, credentials, secrets, internal URLs and sensitive logs; scan artifacts and release metadata.
- [ ] Prepare a reviewed end-user license and third-party notices.

## Build and security validation
- [ ] Build standalone packages from an isolated, controlled environment.
- [ ] Confirm packages do not contain source maps, internal tests, private environment/configuration files, signing keys, secrets or proprietary code not needed to run.
- [ ] Inspect unpacked binaries and packaged JS/resources to understand what can be extracted or read.
- [ ] Sign platform packages with authorized publisher certificates; notarize macOS builds where applicable.
- [ ] Generate SHA-256 checksums for final packaged assets.
- [ ] Run installation, launch, BYOK setup and uninstall tests on clean supported systems.
- [ ] Verify no unapproved automatic telemetry or remote execution and validate update behavior.

## Publishing gate
- [ ] Obtain explicit owner approval to publish this version.
- [ ] Confirm release notes accurately describe supported functionality and known limitations.
- [ ] Upload installers, checksum file, signed verification material and third-party license notices as appropriate.
- [ ] Publish a GitHub Release with correct version tag and artifacts; verify public downloads and checksums.
- [ ] Retain internal release provenance and rollback instructions.

Never copy files or git history from the private application repository into this public repository. No publish automation should be enabled until it has passed an independent security review.
