# Security policy

## Supported versions

Only the latest release of EuclaseUI receives security fixes.

## Reporting a vulnerability

Please do not publish exploit details in a public issue.

1. Use GitHub private vulnerability reporting: the **Security** tab of this repository, then **Report a vulnerability**.
2. If that option is not available, open an issue titled "Security contact request" without technical details, and a private channel will be arranged.

Expect an acknowledgement within a few days. This is a small project maintained by one person; there is no bug bounty.

## Scope

In scope: out-of-bounds access or integer overflow in the canvas, font, widget and panel code, reachable through public API calls.

## Notes

- The library performs no heap allocation and no I/O of its own. Buffers are owned by the caller; the API validates and clips coordinates.
- CI runs the host tests under AddressSanitizer and UndefinedBehaviorSanitizer.
