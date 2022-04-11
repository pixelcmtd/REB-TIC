# CMFFMB

## Dependencies

- `yt-dlp`
- `ffmpeg`
- a POSIX system

## Usage

To run this:

0. Clone the repository
1. Run `./prepare`
2. Run `./x264`
3. Run `./x265`
4. Run `./rav1e`
5. Make a PR adding your results to the table

## Results

| Machine / CPU      | FFmpeg, x264, x265, rav1e | Distro, compiler             | Comments                                 | x264 | x265 | rav1e  |
|--------------------|---------------------------|------------------------------|------------------------------------------|------|------|--------|
| A2338 / Apple M1   | 4.4, 0.163, 3.4, 0.5.0    | Homebrew, Apple clang 12.0.5 | Ideal conditions                         | 81s  | 574s | 11258s |
| A2338 / Apple M1   | 4.4, 0.163, 3.4, 0.5.0    | Homebrew, Apple clang 12.0.5 | Fan locked at 1200rpm (A2337 comparable) | 81s  | 589s | -      |
| Erazer ? / Intel ? | 4.2.4                     | Ubuntu, GCC 9.3.0            |                                          | 306s | TBD  | TBD    |
| AMD Ryzen 9 3900X  | 4.4, 0.161, 3.5, 0.4.1    | Manjaro, GCC 11.1.0          |                                          | 43s  | 112s | 8983s  |

The missing NEON support in x265 really hurts ARM chips.

rav1e only has one A2338 score, because it is currently single-threaded.

<!-- vim: set wrap! : -->
