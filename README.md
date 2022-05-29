# chrissx Media FFMpeg Benchmark

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
5. Run `./versions`
6. Make a PR adding your results to the table

## Results

| Machine / CPU                  | FFmpeg | x264  | x265 | rav1e | Distro   | Compiler           | Comments                                 | x264 | x265 | rav1e  |
| ------------------------------ | ------ | ----- | ---- | ----- | -------- | ------------------ | ---------------------------------------- | ---- | ---- | ------ |
| Apple A2338 / M1               | 4.4    | 0.163 | 3.4  | 0.5.0 | Homebrew | Apple clang 12.0.5 | Ideal conditions                         | 81s  | 574s | 11258s |
| Apple A2338 / M1               | 4.4    | 0.163 | 3.4  |       | Homebrew | Apple clang 12.0.5 | Fan locked at 1200rpm (A2337 comparable) | 81s  | 589s |        |
| Apple A2338 / M1               | 5.0.1  |       | 3.5  |       | Homebrew | Apple clang 13.1.6 | `brew install x265 --HEAD`               |      | 196s |        |
| Apple A2442 / M1 Pro (10 core) | 5.0.1  | 0.163 | 3.4  | 0.5.1 | Homebrew | Apple clang 13.1.6 |                                          | 52s  | 410s | 11002s |
| Apple A2442 / M1 Pro (10 core) | 5.0.1  |       | 3.5  |       | Homebrew | Apple clang 13.1.6 | `brew install x265 --HEAD`               |      | 136s |        |
| Erazer ? / Intel ?             | 4.2.4  | ?     |      |       | Ubuntu   | GCC 9.3.0          | Niklas is very unreliable                | 306s |      |        |
| AMD Ryzen 9 3900X              | 4.4    | 0.161 | 3.5  | 0.4.1 | Manjaro  | GCC 11.1.0         |                                          | 43s  | 112s | 8983s  |

The missing NEON support in x265 3.4 really hurts ARM chips.

<!-- vim: set wrap! : -->
