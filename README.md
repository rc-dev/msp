# MultiWii Serial Protocol (MSP)

This repo is intended to be a project independent source for the latest API specification for MSP, for the projects that are currently sharing a common MSP implementation:
- Betaflight (https://github.com/betaflight/betaflight)
- cleanflight (https://github.com/cleanflight/cleanflight)

## API Version Management Process

As a principle, API versions are always incremented **directly after** a release. This means that whenever the release manager for one of the participating projects publishes a release (RC or stable), after the release has been tagged, a changeset with an increased API version number is pushed (this can be the same changeset that increases the firmware version number for stable releases).
This approach has the benefit that contributors adding new features that require changes in the firmware _and_ in the configurator don't have to worry about the API version. They can write the code (including version gating in configurator) to work with the current API version, and it will work for the next release.
