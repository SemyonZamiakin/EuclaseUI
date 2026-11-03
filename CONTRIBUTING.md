# Contributing to QuasarUI

Thanks for your interest. Bug reports, hardware test reports and focused pull requests are welcome.

## Before you start

- For anything larger than a small fix, open an issue first so the approach can be agreed.
- Keep changes focused: one topic per pull request.

## Build and test

```
cmake -S . -B build -DCMAKE_CXX_FLAGS="-Wall -Wextra -fsanitize=address,undefined"
cmake --build build
ctest --test-dir build --output-on-failure
```

The library targets C++11 and must keep working without heap allocation and without Arduino or ESP-IDF headers in the core (`src/qs_*`).

A pull request is expected to keep the build warning-free (`-Wall -Wextra`) and the test suite green. New behaviour needs a test.

Hardware verification (a board, a panel and a photo) is the most valuable contribution right now; see the Status table in the README.

## Style

- Match the surrounding code: naming, formatting and comment density.
- No new third-party dependencies without discussion.
- Do not commit binaries, build output or secrets.

## Commits and pull requests

- Write the commit subject in the imperative mood ("Fix X", "Add Y"), under about 72 characters, with a short body that explains why.
- Describe in the pull request what you tested and on what hardware or OS.

## Reporting results from your hardware

For hardware-dependent behaviour, the most useful report contains: the exact device model, OS version, what you expected, what happened, and logs where available.

## License

By contributing you agree that your contribution is licensed under the MIT license of this repository.
