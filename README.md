# CMFFMB

## Dependencies

- `youtube-dl` (might switch to `youtube-dlp` soon)
- `ffmpeg`
- a POSIX system

## Usage

To run this:

0. Clone the repository
1. Run `./prepare`
2. Run `./h264`
3. Run `./h265`
4. Make a PR adding your results to the table

## Results

| Machine / CPU     | FFmpeg | Distro, compiler             | Comments                                 | H.264 real time | H.265 real time |
|-------------------|--------|------------------------------|------------------------------------------|-----------------|-----------------|
| A2338 / Apple M1  | 4.4    | Homebrew, Apple clang 12.0.5 | Ideal conditions                         | 81s             | 574s            |
| A2338 / Apple M1  | 4.4    | Homebrew, Apple clang 12.0.5 | Fan locked at 1200rpm (A2337 comparable) | 81s             | 589s            |
| AMD Ryzen 9 3900X | 4.4    | Manjaro, GCC 11.1.0          |                                          | 43s             | 112s            |

The missing NEON support in x265 really hurts ARM chips.

<!-- vim: set wrap! : -->
