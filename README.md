# gh-release-mono

gh plugin to automatically release the next numeric version of services based on
the pattern `servicename/r<number>`

install with `gh extension install marcusramberg/gh-release-mono`

## Usage

```sh

Usage: gh release-mono <service>

Create the next numbered release for a service.

Finds the latest release tag matching <service>/r<N>, bumps N by one,
and creates a new release with generated notes.

Example:
    gh release-next myservice
    # finds myservice/r08, creates myservice/r09

Options:
    -h, --help          Show this help message
    -d, --dry-run       Print what would happen without creating the release
    -t, --tag-template  Override the tag pattern (default: r)
    -y, --yes           Skip interactive confirmation
    -w, --wait          Wait for all CI checks on main to pass before releasing

Environment Variables:
    GH_RELEASE_NEXT_DRY_RUN       Set to 'true' for dry-run mode
    GH_RELEASE_NEXT_TAG_TEMPLATE  Set tag prefix (default: 'r')
```
