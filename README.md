# REB-TIC

_**Re**al World **B**enchmarks for **T**asks **I**mportant to **c**hrissx Media_ are a benchmarking suite for all kinds of different machines running POSIX software.

## FFmpeg Benchmark v1

### Dependencies

- `yt-dlp`
- `ffmpeg`
- a POSIX system

### Usage

0. Clone the repository (and ensure `yt-dlp` and `ffmpeg` are installed and up-to-date)
1. Run `./ffmb` (get the svtav1 version from your package manager)
2. Make a PR adding your results to the table

### Results

| Machine / CPU                                   | FFmpeg | x264  | x265 | rav1e | svtav1 | Distro            | Compiler       | Notes                      | x264  | x265   | rav1e  | svtav1 |
| ----------------------------------------------- | ------ | ----- | ---- | ----- | ------ | ----------------- | -------------- | -------------------------- | ----- | ------ | ------ | ------ |
| Apple A2338 / M1 (ARM64 8c/8t)                  | 5.1.2  | 0.164 | 3.5  |       | 1.3.0  | Homebrew Monterey | Apple clang 14 | `brew install x265 --HEAD` | 78s   | 196s   |        | 468s   |
| Apple A2442 / M1 Pro (ARM64 10c/10t)            | 5.1.2  | 0.164 | 3.5  | 0.5.1 | 1.3.0  | Homebrew Ventura  | Apple clang 14 | `brew install x265 --HEAD` | 52s   | 136s   | 10553s | 292s   |
| Apple A2442 / M1 Pro (ARM64 10c/10t)            | 7.0    | 0.164 | 3.6  | 0.7.1 | 2.0.0  | Homebrew Sonoma   | Apple clang 15 |                            | 57s   | 119s   | 4540s  | 75s    |
| Apple A1534 / Intel m7-6Y75 (x86\_64 2c/4t)     | 5.1.2  | 0.164 | 3.4  |       | 1.3.0  | Homebrew Monterey | Apple clang 14 |                            | 395s  | 598s   |        | 267s   |
| AMD Ryzen 9 3900X (x86\_64 12c/24t)             | 5.1.2  | 0.164 | 3.5  | 0.5.1 | 1.3.0  | Manjaro Ruah      | GCC 12         |                            | 44s   | 94s    | 7781s  | 36s    |
| OptiPlex 3020 / Intel i5-4570 (x86\_64 4c/4t)   | 4.4.2  | 0.163 | 3.5  |       |        | Ubuntu Jammy      | GCC 11         |                            | 179s  | 289s   |        |        |
| Lenovo M710s / Intel i5-7500 (x86\_64 4c/4t)    | 4.4.2  | 0.163 | 3.5  |       |        | Ubuntu Jammy      | GCC 11         |                            | 147s  | 236s   |        |        |
| ThinkPad X220 / Intel i5-2540M (x86\_64 2c/4t)  | 5.1.2  | 0.164 | 3.5  |       | 1.3.0  | Manjaro Ruah      | GCC 12         |                            | 498s  | 855s   |        | 534s   |
| ThinkPad T430s / Intel i7-3520M (x86\_64 2c/4t) | 5.1.2  | 0.164 | 3.5  |       | 1.3.0  | Manjaro Ruah      | GCC 12         |                            | 358s  | 596s   |        | 376s   |
| ThinkPad Z60m / Intel M 740 (IA-32 1c/1t)       | 4.3.5  | 0.160 | 3.4  |       |        | Debian Bullseye   | GCC 10         |                            | 3886s | 19231s |        |        |
| Erazer ? / Intel ?                              | 4.2.4  | ?     |      |       |        | Ubuntu            | GCC 9          | Niklas is very unreliable  | 306s  |        |        |        |

<!-- vim: set wrap! : -->
